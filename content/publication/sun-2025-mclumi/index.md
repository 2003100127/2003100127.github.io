---
title: 'mclUMI: Markov clustering of unique molecular identifiers enables dynamic
  removal of PCR duplicates'
authors:
- Jianfeng Sun
- Shuang Li
- Stefan Canzar
- Adam P Cribbs
date: '2025-01-01'
publishDate: '2025-03-21T15:52:19.769946Z'
publication_types:
- article-journal
publication: '*bioRxiv*'
doi: 10.1101/2025.03.15.643033
abstract: Molecular quantification in high-throughput sequencing experiments relies
  on accurate identification and removal of polymerase chain reaction (PCR) duplicates.
  The use of Unique Molecular Identifiers (UMIs) in sequencing protocols has become
  a standard approach for distinguishing molecular identities. However, PCR artefacts
  and sequencing errors in UMIs present a significant challenge for effective UMI
  collapsing and accurate molecular counting. Current computational strategies for
  UMI collapsing often exhibit limited flexibility, providing invariable deduplicated
  counts that inadequately adapt to varying experimental conditions. To address these
  limitations, we developed mclUMI, a tool employing the Markov clustering algorithm
  to accurately identify original UMIs and eliminate PCR duplicates. Unlike conventional
  methods, mclUMI automates the detection of independent communities within UMI graphs
  by dynamically fine-tuning inflation and expansion parameters, enabling context-dependent
  merging of UMIs based on their connectivity patterns. Through in silico experiments,
  we demonstrate that mclUMI generates dynamically adaptable deduplication outcomes
  tailored to diverse experimental scenarios, particularly best-performing under high
  sequencing error rates. By integrating connectivity-driven clustering, mclUMI enhances
  the accuracy of molecular counting in noisy sequencing environments, addressing
  the rigidity of current UMI deduplication frameworks.Competing Interest StatementA.P.C
  is listed as an inventor on several patents filed by Oxford University Innovations
  concerning single-cell sequencing technologies. The other authors declare that they
  have no known competing financial interests or personal relationships that could
  have appeared to influence the work reported in this paper.
links:
- name: URL
  url: https://www.biorxiv.org/content/early/2025/03/16/2025.03.15.643033
---
