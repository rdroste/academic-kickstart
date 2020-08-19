---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Automatic Probe Movement Guidance for Freehand Obstetric Ultrasound"
authors: ["**Richard Droste**", "Lior Drukker", "Aris Papageorghiou", "J Alison Noble"]
date: 2020-07-02
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-07-09T14:53:08+02:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: " 23rd International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI 2020)"
publication_short: "MICCAI 2020"

abstract: "We present the first system that provides real-time probe movement guidance for acquiring standard planes in routine freehand obstetric ultrasound scanning. Such a system can contribute to the worldwide deployment of obstetric ultrasound scanning by lowering the required level of operator expertise. The system employs an artificial neural network that receives the ultrasound video signal and the motion signal of an inertial measurement unit (IMU) that is attached to the probe, and predicts a guidance signal. The network termed US-GuideNet predicts either the movement towards the standard plane position (goal prediction), or the next movement that an expert sonographer would perform (action prediction). While existing models for other ultrasound applications are trained with simulations or phantoms, we train our model with real-world ultrasound video and probe motion data from 464 routine clinical scans by 17 accredited sonographers. Evaluations for 3 standard plane types show that the model provides a useful guidance signal with an accuracy of 88.8% for goal prediction and 90.9% for action prediction."

# Summary. An optional shortened abstract.
summary: "23rd International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI 2020). <span style=\"color: #c28422; font-weight:bold\">Oral Presentation</span>. <span style=\"color: #2a8a80; font-weight:bold\">Early Acceptance</span>"

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
  url: files/droste-et-al_probe-guidance_MICCAI-2020.pdf
  icon_pack: fas
  icon: file-pdf
- name: arXiv
  url: https://arxiv.org/abs/2007.04480
  icon_pack: ai
  icon: arxiv
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/miccai2020/#bibtex

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
  caption: "a) Proposed behavioral cloning framework. b) US-GuideNet architecture."
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
@InProceedings{droste2020miccai,
       author = {Droste, Richard and Drukker, Lior and Papageorghiou, Aris T. and Noble, J. Alison},
        title = "{Automatic Probe Movement Guidance for Freehand Obstetric Ultrasound}",
    booktitle = {International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI)},
         year = {2020}
}
```
