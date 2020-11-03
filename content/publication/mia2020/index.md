---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Spatio-Temporal Visual Attention Modelling of Standard Biometry Plane-Finding Navigation"
authors: ["Yifan Cai", "**Richard Droste**", "Harshita Sharma", "Pierre Chatelain", "Lior Drukker", "Aris Papageorghiou", "J Alison Noble"]
date: 2020-07-01
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-07-02

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "Medical Image Analysis 2020"
publication_short: "MIA 2020"

abstract: "We present a novel multi-task neural network called Temporal SonoEyeNet (TSEN) with a primary task to describe the visual navigation process of sonographers by learning to generate visual attention maps of ultrasound images around standard biometry planes of the fetal abdomen, head (trans-ventricular plane) and femur. TSEN has three components: a feature extractor, a temporal attention module (TAM), and an auxiliary video classification module (VCM). A soft dynamic time warping (sDTW) loss function is used to improve visual attention modelling. Variants of the model are trained on a dataset of 280 video clips, each containing one of the three biometry planes and lasting 3–7 seconds, with corresponding real-time recorded gaze tracking data of an experienced sonographer. We report the performances of the different variants of TSEN for visual attention prediction at standard biometry plane detection. The best model performance is achieved using bi-directional convolutional long-short term memory (biCLSTM) in both TAM and VCM, and it outperforms a previous spatial model on all static and dynamic saliency metrics. As an auxiliary task to validate the clinical relevance of the visual attention modelling, the predicted visual attention maps were used to guide standard biometry plane detection in consecutive US video frames. All spatio-temporal TSEN models achieve higher scores compared to a spatial-only baseline; the best performing TSEN model achieves F1 scores on these standard biometry planes of 83.7%, 89.9% and 81.1%, respectively."

# Summary. An optional shortened abstract.
summary: "Medical Image Analysis (2020)."

tags: ["paper"]
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
- name: Elsevier
  url: https://www.sciencedirect.com/science/article/pii/S1361841520301262#absh0002
  icon_pack: ai
  icon: elsevier
# - name: PDF
#   url: files/droste-et-al_probe-guidance_MICCAI-2020.pdf
#   icon_pack: fas
#   icon: file-pdf
# - name: arXiv
#   url: https://arxiv.org/abs/2007.04480
#   icon_pack: ai
#   icon: arxiv
- name: DOI
  url: https://doi.org/10.1016/j.media.2020.101762
  icon_pack: ai
  icon: doi
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/mia2020/#bibtex

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
  caption: "Graphical abstract"
  focal_point: ""
  preview_only: false

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
---

Paper summary coming soon!


<!-- Richard Droste*, Yifan Cai, Harshita Sharma, Pierre Chatelain, Lior Drukker, Aris T. Papageorghiou, J. Alison Noble -->

---
# BibTex

```
@article{cai2020mia,
  author = {Cai, Yifan and Droste, Richard and Sharma, Harshita and Chatelain, Pierre and Drukker, Lior and Papageorghiou, Aris T. and Noble, J. Alison},
  title = {Spatio-Temporal Visual Attention Modelling of Standard Biometry Plane-Finding Navigation},
  journal = {Medical Image Analysis},
  volume = {65},
  year = {2020},
  doi = {https://doi.org/10.1016/j.media.2020.101762},
  url = {https://www.sciencedirect.com/science/article/pii/S1361841520301262#absh0002},
}
```
