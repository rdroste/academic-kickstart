---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Discovering Salient Anatomical Landmarks by Predicting Human Gaze"
# authors: [admin, yifan, harshita, pierre, lior, aris, alison]
authors: ["**Richard Droste**", "Pierre Chatelain", "Lior Drukker", "Harshita Sharma", "Aris Papageorghiou", "J Alison Noble"]
date: 2020-01-06
doi:
draft: false

# Schedule page publish date (NOT publication's date).
publishDate: 2019-03-07

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "IEEE International Symposium on Biomedical Imaging (ISBI) 2020"
publication_short: "ISBI 2020"

abstract: "Anatomical landmarks are a crucial prerequisite for many medical imaging tasks. Usually, the set of landmarks for a given task is predefined by experts. The landmark locations for a given image are then annotated manually or via machine learning methods trained on manual annotations. In this paper, in contrast, we present a method to automatically discover and localize anatomical landmarks in medical images. Specifically, we consider landmarks that attract the visual attention of humans, which we term visually salient landmarks. We illustrate the method for fetal neurosonographic images. First, full-length clinical fetal ultrasound scans are recorded with live sonographer gaze-tracking. Next, a convolutional neural network (CNN) is trained to predict the gaze point distribution (saliency map) of the sonographers on scan video frames. The CNN is then used to predict saliency maps of unseen fetal neurosonographic images, and the landmarks are extracted as the local maxima of these saliency maps. Finally, the landmarks are matched across images by clustering the landmark CNN features. We show that the discovered landmarks can be used within affine image registration, with average landmark alignment errors between 4.1% and 10.9% of the fetal head long axis length."

# Summary. An optional shortened abstract.
summary: "IEEE International Symposium on Biomedical Imaging (ISBI) 2020. <span style=\"color: #c28422; font-weight:bold\">Oral presentation</span>. <span style=\"color: #2a8a80; font-weight:bold\">Runner up for Best Paper Award</span>."

tags: []
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
  url: files/droste-et-al_visually-salient-landmarks_ISBI-2020.pdf
  icon_pack: fas
  icon: file-pdf
# - name: Poster
#   url: files/181_droste-et-al_ultrasound-visual-attention-modelling_v2-7.pdf
#   icon_pack: fas
#   icon: scroll
# - name: DOI
#   url: https://doi.org/10.1007/978-3-030-20351-1_46
#   icon_pack: ai
#   icon: doi
- name: arXiv
  url: https://arxiv.org/abs/2001.08188
  icon_pack: ai
  icon: arxiv
# - name: ORA
#   url: https://ora.ox.ac.uk/objects/uuid:a27fe42b-3a94-4b0f-bc7d-2173c0348b6f
#   icon_pack: ai
#   icon: open-access
# - name: Springer
#   url: https://link.springer.com/chapter/10.1007/978-3-030-20351-1_46
#   icon_pack: ai
#   icon: springer
- name: Presentation
  icon_pack: fas
  icon: youtube
  url: https://www.youtube.com/watch?v=XnD2ym5Ywww
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/isbi2020/#bibtex


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
  caption: ""
  focal_point: ""
  preview_only: true

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""


# Optional header image (relative to `static/img/` folder).
header:
  caption: ""
  image: ""
---

Paper summary coming soon!


<!-- Richard Droste*, Yifan Cai, Harshita Sharma, Pierre Chatelain, Lior Drukker, Aris T. Papageorghiou, J. Alison Noble -->

---
# BibTex
```
@InProceedings{
  author={Droste, Richard and Chatelain, Pierre and Drukker, Lior and Sharma, Harshita and Papageorghiou, Aris T. and Noble, J. Alison},
  title={Discovering Salient Anatomical Landmarks by Predicting Human Gaze},
  booktitle={IEEE International Symposium on Biomedical Imaging (ISBI)},
  year={2020}
}
```
---

# Acknowledgments

We acknowledge the ERC ([ERC-ADG-2015 694581, project PULSE](https://cordis.europa.eu/project/rcn/205894/factsheet/en)), the EPSRC (EP/M013774/1), and the NIHR Oxford Biomedical Research Centre.
