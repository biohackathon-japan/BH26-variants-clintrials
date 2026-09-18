---
title: 'DBCLS BioHackathon 2026 report: Variant representation in RDF for precision medicine'
title_short: 'BioHackJP26: Variants for precision medicine'
tags:
  - Genomic variants
  - RDF
  - GA4GH VRS
  - Synthetic patient data
authors:
  - name: Núria Queralt-Rosinach
    orcid: 0000-0003-0169-8159
    affiliation: 1
  - name: Daniel Puthawala
    orcid: 0000-0002-1823-7124
    affiliation: 2
affiliations:
  - name: Leiden University Medical Center, The Netherlands
    index: 1
  - name: Nationwide Children's Hospital, USA
    index: 2
date: 18 September 2026
cito-bibliography: paper.bib
event: BH26JP
biohackathon_name: "DBCLS BioHackathon 2026"
biohackathon_url:   "https://2026.biohackathon.org/"
biohackathon_location: "Matsuyama, Japan, 2026"
group: variants-clintrials
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackathon-japan/BH26-variants-clintrials
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: Queralt-Rosinach \emph{et al.}
---


# Abstract
For the life science semantic web community, the provision of genomic variants ready for tools and applications is essential to deliver on the promise of precision medicine. As part of the DBCLS BioHackathon 2026, we here report our efforts on how best to provide variant data in RDF for downstream patient-clinical trial matching applications. 

# Introduction

To match patients to clinical trials is an essential question in rare disease and oncology research. It requires a precise and machine-readable representation of clinical and genomic information to profile patients' specific disease biology and define clinical trials eligibility criteria. This is a follow-up work from prior BioHackathons enriched by the opportunity to have participants directly involved in the development of GA4GH genomic variant standards and RDF datasets for its application. In previous hackathons our focus was how to represent variant data in RDF in a standard and integratable way [@citesAsAuthority:vrsrdfBH2024] using the GA4GH Variant Representation Specification (VRS) [@citesAsAuthority:Wagner2021]. In the DBCLS BioHackathon 2026, we changed to the tools perspective and asked the question how ready is variant data in RDF portals for precision medicine applications such as patient-clinical trial matching.

Objective: We aim to connect genomic variant information from variant datasets in RDF to clinical trials eligibility criteria using the GA4GH VRS standard.

# Method
## Use of Standards
 We adhered to established standards such as GA4GH VRS and Cat-VRS, RDF/OWL, and ShEx to ensure interoperability and semantic consistency.

## Use Case-Driven Approach
 Our methodology was guided by the patient-to-clinical-trial matching use case from the tool application perspective. This approach ensures that our data is ready for downstream application tools.

# Results
## ClinVar RDF dataset
  * Analysed RDFPortal datasets, it provides several datasets about human genomic variant information from biomedical databases such as ClinVar RDF. ClinVar is a well-known knowledge base that organises information about genomic variation and its relationship to human health. The challenge is that its current RDF schema is too complex and its transformation into RDF depends on third parties.
  * Designed a strategy to update the current RDF schema and data transformation pipeline into RDF.

## Clinical Trials RDF dataset  
  * During BH24 we designed a prototype of RDF schema and RDF data converter to provide clinical trials data integrated from different sources such as ClinicalTrials.org. 
  * Designed a strategy to update the current RDF schema to structure and incorporate genomic data extracted from the inclusion criteria text. We plan to incorporate this dataset in RDFPortal.

## Standard and tools for genomic variant representation in RDF
  * Identified mistakes and points for improvement in our current GA4GH VRS RDF schema devoted to align with the current release of the standard.
  * MatchMiner tool (https://matchminer.gitbook.io/) and their patient and clinical trial data models provided a starting point to prioritise the RDF schema modelling and update of VRS focusing on these data model elements. 
  * Designed RDF converter pipelines to develop in future hackathons.

## Synthetic variant data generation using GA4GH Cat-VRS
  * Discussed the idea of leveraging ClinVar RDF and GA4GH Cat-VRS for synthetic variant data generation. We plan to follow-up on this idea in the future.

# Discussion
As part of the DBCLS BioHackathon 2026, we here reported our efforts on how best to provide genomic variant data and tools for RDF data portals to feed downstream patient-clinical trial matching applications. Our approach was to analyse state-of-the-art tools developed for patient-clinical trial matching and their data models to establish a data management strategy for RDF genomic variant data provision from human and clinical trials established databases. Although we designed ideas and just started actual hacking, this work paves the way to develop new RDF data, standards and tools for genomic variant data exploitation. During one week of natural interactions between different stakeholders, provided one more time the ideal venue to identify flaws in initial ideas and current data management plans, and continue-start new projects and collaborations. 

## Acknowledgements
We thank the organizers of the DBCLS BioHackathon 2026 for providing the venue and support for this work. We also acknowledge the developers of GA4GH VRS for providing the foundational model that made this work possible and RDFPortal data managers and developers to share needs and data transformation pipelines. We would like to thank the contributions of Orion Buske, Dawn Chen, Chang Sun, Shuichi Kawashima, Yasunori Yamamoto, Akira R. Kinjo, Priscilla Joanne, Tazro Ohta, Núria Fàbrega and Claude Nanjo who shared their needs, ideas, tools and domain knowledge for all the informative and inspirational discussions maintained along the week.

# References
