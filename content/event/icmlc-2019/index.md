---
title: ICMLC 2019

event: International Conference on Machine Learning and Cybernetics (ICMLC) 2019
event_url: https://scholar.google.com/citations?user=TfLBR9kAAAAJ&hl=en

location: Kobe Convention Center
address:
  street: 6 Chome
  city: Kobe
  region: Minatojima Nakamachi
  postcode: 650-0046
  country: Japan

summary: Residue-residue contacts prediction using RNN-based LSTM Network
abstract: 'Extracting residue-pair features from unsupervised learning and reconstructing data from high-dimensional input vectors.'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2019-07-09T09:00:00Z'
date_end: '2019-07-11T21:30:00Z'
all_day: true

# Schedule page publish date (NOT talk date).
publishDate: '2023-04-26T00:00:00Z'

authors:
  - admin

tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: **self**'
  focal_point: Right

#links:
#  - icon: twitter
#    icon_pack: fab
#    name: Follow
#    url: https://twitter.com/georgecushen
url_code: 'https://github.com'
url_pdf: ''
url_slides: 'https://slideshare.net'
url_video: 'https://youtube.com'

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
  - example
---

{{% callout note %}}
t-SNE visualisation of features of residue pairs for differentiating contacts or non-contacts.
{{% /callout %}}

At this conference, I focused on only one question: classification effects of contacting and non-contacting residue pairs using dimensionality reduction techniques.

My aim was to evaluate whether the features defined for residue pairs are effective in distinguishing between these two categories. Specifically, I sought to determine if the data could be meaningfully separated in a two-dimensional space. To investigate this, I employed several computational approaches for visualizing the separability of the data.

For the autoencoder, I implemented a deep architecture with four layers each in the encoder and decoder, compressing from 256 hidden neurons down to a 2-dimensional latent space. For PCA and t-SNE, I directly projected the data into two dimensions to facilitate comparison.

Across all three unsupervised methods, I observed that contacting and non-contacting residue pairs could be broadly separated. Notably, the dispersed nature of non-contacting residue pairs became increasingly pronounced in most visualizations. In particular, the t-SNE results revealed a clearer separation, with residue pairs forming two distinct clusters.

![](icmlc2019_tsne_1chd.jpg "Caption: Visualisation of differentiation between contacting and non-contacting residue pairs using t-distributed Stochastic Neighbor Embedding (t-SNE)")