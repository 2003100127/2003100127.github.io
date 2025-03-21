---
title: 'PSRR: A Web Server for Predicting the Regulation of miRNAs Expression by Small
  Molecules'
authors:
- Fanrong Yu
- Bihui Li
- Jianfeng Sun
- Jing Qi
- Rudy Leon De Wilde
- Luz Angela la Roche
- Cheng Li
- Sajjad Ahmad
- Wenjie Shi
- Xiqing Li
- Zihao Chen
date: '2022-01-01'
publishDate: '2025-03-21T15:52:19.575603Z'
publication_types:
- article-journal
publication: '*Frontiers in Molecular Biosciences*'
doi: 10.3389/fmolb.2022.817294
abstract: 'Background: MicroRNAs (miRNAs) play key roles in a variety of pathological
  processes by interacting with their specific target mRNAs for translation repression
  and may function as oncogenes (oncomiRs) or tumor suppressors (TSmiRs). Therefore,
  a web server that could predict the regulation relations between miRNAs and small
  molecules is expected to achieve implications for identifying potential therapeutic
  targets for anti-tumor drug development.Methods: Upon obtaining positive/known small
  molecule-miRNA regulation pairs from SM2miR, we generated a multitude of high-quality
  negative/unknown pairs by leveraging similarities between the small molecule structures.
  Using the pool of the positive and negative pairs, we created the Dataset1 and Dataset2
  datasets specific to up-regulation and down-regulation pairs, respectively. Manifold
  machine learning algorithms were then employed to construct models of predicting
  up-regulation and down-regulation pairs on the training portion of pairs in Dataset1
  and Dataset2, respectively. Prediction abilities of the resulting models were further
  examined by discovering potential small molecules to regulate oncogenic miRNAs identified
  from miRNA sequencing data of endometrial carcinoma samples.Results: The random
  forest algorithm outperformed four machine-learning algorithms by achieving the
  highest AUC values of 0.911 for the up-regulation model and 0.896 for the down-regulation
  model on the testing datasets. Moreover, the down-regulation and up-regulation models
  yielded the accuracy values of 0.91 and 0.90 on independent validation pairs, respectively.
  In a case study, our model showed highly-reliable results by confirming all top
  10 predicted regulation pairs as experimentally validated pairs. Finally, our predicted
  binding affinities of oncogenic miRNAs and small molecules bore a close resemblance
  to the lowest binding energy profiles using molecular docking. Predictions of the
  final model are freely accessible through the PSRR web server at <ext-link ext-link-type=\"uri\"
  xmlns:xlink=\"http://www.w3.org/1999/xlink\" xlink:href=\"https://rnadrug.shinyapps.io/PSRR/\">https://rnadrug.shinyapps.io/PSRR/</ext-link>.Conclusion:
  Our study provides a novel web server that could effectively predict the regulation
  of miRNAs expression by small molecules.'
links:
- name: URL
  url: https://www.frontiersin.org/article/10.3389/fmolb.2022.817294
---
