---
title: 'SVLearn: a dual-reference machine learning approach enables accurate cross-species
  genotyping of structural variants'
authors:
- Qimeng Yang
- admin
- Xinyu Wang
- Jiong Wang
- Quanzhong Liu
- Jinlong Ru
- Xin Zhang
- Sizhe Wang
- Ran Hao
- Peipei Bian
- Xuelei Dai
- Mian Gong
- Zhuangbiao Zhang
- Ao Wang
- Fengting Bai
- Ran Li
- Yudong Cai
- Yu Jiang
date: '2025-03-11'
publishDate: '2025-03-27T06:24:05.444184Z'
publication_types:
- article-journal
publication: '*Nature Communications*'
doi: 10.1038/s41467-025-57756-z
abstract: Structural variations (SVs) are diverse forms of genetic alterations and
  drive a wide range of human diseases. Accurately genotyping SVs, particularly occurring
  at repetitive genomic regions, from short-read sequencing data remains challenging.
  Here, we introduce SVLearn, a machine-learning approach for genotyping bi-allelic
  SVs. It exploits a dual-reference strategy to engineer a curated set of genomic,
  alignment, and genotyping features based on a reference genome in concert with an
  allele-based alternative genome. Using 38,613 human-derived SVs, we show that SVLearn
  significantly outperforms four state-of-the-art tools, with precision improvements
  of up to 15.61% for insertions and 13.75% for deletions in repetitive regions. On
  two additional sets of 121,435 cattle SVs and 113,042 sheep SVs, SVLearn demonstrates
  a strong generalizability to cross-species genotype SVs with a weighted genotype
  concordance score of up to 90%. Notably, SVLearn enables accurate genotyping of
  SVs at low sequencing coverage, which is comparable to the accuracy at 30× coverage.
  Our studies suggest that SVLearn can accelerate the understanding of associations
  between the genome-scale, high-quality genotyped SVs and diseases across multiple
  species.

tags:
- sequencing

featured: true

links:
- name: Journal website
  url: https://doi.org/10.1038/s41467-025-57756-z
url_pdf: https://doi.org/10.1038/s41467-025-57756-z
url_code: 'https://github.com/yangqimeng99/svlearn'
#url_dataset: '#'
#url_poster: '#'
#url_project: ''
url_slides: 'https://github.com/yangqimeng99/svlearn/wiki/Compare-with-other-tools'
#url_source: '#'
url_video: 'https://github.com/yangqimeng99/svlearn-paper-code'
---


## Prelude

SVlearn is a computational tool for structural variation (SV) genotyping, originally developed using machine learning methods such as Random Forest. While it demonstrated strong predictive capabilities, during the development process we also further explored whether deep learning techniques could enhance its performance. In this post, I would like to briefly present this investigation from a deep learning perspective.

## Behind the paper

https://communities.springernature.com/posts/a-dual-reference-modality-to-effectively-enhance-the-accuracy-of-genotyping-structural-variants-from-short-read-sequencing

## Code source

https://github.com/yangqimeng99/svlearn

## Deep Learning Approach

I used three representative deep learning methods: a convolutional neural network (CNN), a hybrid long short-term memory & CNN model (LSTM-CNN), and a residual network (ResNet). The settings of each method follow those as detailed in [https://doi.org/10.3390/ijms24031878](https://doi.org/10.3390/ijms24031878). Each model was trained. Nine evaluation metrics were used to assess predictive performance, including AUC, AP, Accuracy, Precision, Recall, Matthews Correlation Coefficient (MCC), Jaccard Index, FB-Score, F1-Score

## Results

The dataset used in this study contains tens of thousands of SVs, with features that are highly domain-specific. No signs of overfitting were observed during training (**Figure 1**), indicating effective regularization and data sufficiency.

![](svlearn_dl_epoch.jpg "Figure. 1 Predictive performance of the three deep learning models and their ensemble over training epochs.")

The best-performing model in SVLearn is random forest, which reaches an accuracy of 0.920. I applied [stack generalisation](https://doi.org/10.1016/S0893-6080(05)80023-1) as an ensemble strategy to several traditional machine learning models, including random forest, logistic regression, naive Bayes, k-nearest neighbors, support vector machine, and gradient boosting, which, however, did not result in a performance gain on the independent test set. 

The best-performing single deep learning model achieved an accuracy of 0.924. Using average ensemble predictions to integrate the three deep learning models, the accuracy improved slightly to 0.925 (**Figure 2**). The ROC curve confirms the stable, robust prediction ability of deep learning (**Figure 3**).

![](svlearn_dl_bar.jpg "Figure. 2 Accuracy comparison across the three individual models and the ensemble model.")


![](svlearn_dl_roc.jpg "Figure. 3 ROC curves and corresponding AUC values for each model on the independent test set.")

### Conclusions

In contrast, deep learning models achieved slightly higher predictive accuracy, with 0.924 from the best individual model and 0.925 from the ensemble. Although the improvement is marginal (only 0.1%), it demonstrates the capacity of deep learning to extract more complex patterns, while within diminishing returns due to the already strong data foundation.

It is also worth noting that performance variance among deep learning models was minimal, while traditional machine learning models exhibited greater variability, which further highlights the stability and robustness of deep learning in this context.

Overall, the use of machine learning, particularly deep learning for modeling and predicting structural variation data in sheep, has proven to be a successful and meaningful scientific endeavor. The high quality and richness of the dataset played a critical role in ensuring model generalisability and avoiding overfitting. The results suggest that current deep learning models have likely reached the upper performance bound on this dataset, and offer a reliable and consistent predictive framework for SV genotyping tasks.

## Read the paper

https://doi.org/10.1038/s41467-025-57756-z