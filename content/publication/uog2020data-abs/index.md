---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "OC10.11: The data science of obstetric ultrasound: automatic analysis of full‐length anomaly scans using machine learning algorithms"
authors: ["Lior Drukker", "Harshita Sharma", "**Richard Droste**", "J Alison Noble", "Aris Papageorghiou"]
date: 2020-10-14
doi: ""
draft: false

# Schedule page publish date (NOT publication's date).
publishDate: 2019-09-30

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["0"]

# Publication name and optional abbreviated publication name.
publication: "Ultrasound in Obstetrics & Gynecology"
publication_short: "Ultrasound Obstet Gynecol"

abstract: "
**Objectives**:
The clinical workflow of the second trimester anomaly scan is not well studied and holds potential for efficiency improvement. We aimed to create a model for automatic anatomical description of full‐length fetal anomaly scan videos using artificial intelligence.

**Methods**:
We prospectively recorded routine full‐length second trimester anomaly scans, extracted short clips of important scan events by detecting video freeze, and image/clip save. For machine learning, we created a training dataset by manually labelling 12% of the scan events to one of 23 principal anatomical structures, trained a deep spatiotemporal neural network with the training dataset, cross‐validated and applied the model to automatically label the rest of the scans. Finally, we retrospectively labelled a test dataset (48 scans) to compare with the automatically labelled scans. We report the model precision and workflow metrics.

**Results**:
518 scans performed by 14 operators were analysed. The mean scan duration was 26.7 ± 15 minutes, and the mean number of scan events was 23.5 ± 14.4. The manual vs. automatic clips labelling agreement was 74.5%, ranging from 34% for placenta to 89% for heart. The brain, heart and spine were most often the first structure to be evaluated, in 18.8%, 17.6% and 17% of the scans, respectively. On average, 15% of the scan duration was dedicated to cardiac scanning, 10% to brain, and 7% to the spine (figure 1).

**Conclusions**:
Using big data, we present a model that describes how expert sonographers perform anomaly scans in a data science fashion. Understanding how operators scan and being able to measure the different operator elements will inform a better understanding of how to train operators, monitor learning progress, and enhance scanning workflow."

# Summary. An optional shortened abstract.
summary: "ISUOG World Congress 2020. <span style=\"color: #c28422; font-weight:bold\">Oral presentation</span>."

tags: ["clinical_abstract"]
categories: []
featured: true

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter
links:
- name: PDF
  url: https://obgyn.onlinelibrary.wiley.com/doi/epdf/10.1002/uog.22275
  icon_pack: fas
  icon: file-pdf
- name: DOI
  url: https://doi.org/10.1002/uog.22275
  icon_pack: ai
  icon: doi
# - name: ORA
#   url: https://ora.ox.ac.uk/objects/uuid:a14df633-3dc5-4918-ba90-09dda3f51363
#   icon_pack: ai
#   icon: open-access
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/uog2020data-abs/#bibtex

url_pdf:
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Figure 1"
  focal_point: "Left"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
# projects: [ipmi2019]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

---
# BibTex

```
@article{doi:10.1002/uog.22275,
author = {Drukker, L. and Sharma, H. and Droste, R. and Noble, J.A. and Papageorghiou, A.T.},
title = {OC10.11: The data science of obstetric ultrasound: automatic analysis of full-length anomaly scans using machine learning algorithms},
journal = {Ultrasound in Obstetrics \& Gynecology},
volume = {56},
number = {S1},
pages = {31-31},
doi = {10.1002/uog.22275},
url = {https://obgyn.onlinelibrary.wiley.com/doi/abs/10.1002/uog.22275},
eprint = {https://obgyn.onlinelibrary.wiley.com/doi/pdf/10.1002/uog.22275},
year = {2020}
}
```
