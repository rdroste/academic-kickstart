---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Unified Image and Video Saliency Modeling"
# authors: [admin, yifan, harshita, pierre, lior, aris, alison]
authors: ["**Richard Droste***", "Jianbo Jiao*", "J Alison Noble"]
date: 2020-03-12
doi:
draft: false

# Schedule page publish date (NOT publication's date).
publishDate: 2019-03-12

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "arXiv preprint"
publication_short: "arXiv preprint"

abstract: "Visual saliency modeling for images and videos is treated as two independent tasks in recent computer vision literature. On the one hand, image saliency modeling is a well-studied problem and progress on benchmarks like SALICON and MIT300 is slowing. For video saliency prediction on the other hand, rapid gains have been achieved on the recent DHF1K benchmark through network architectures that are optimized for this task. Here, we take a step back and ask: Can image and video saliency modeling be approached via a unified model, with mutual benefit? We find that it is crucial to model the domain shift between image and video saliency data and between different video saliency datasets for effective joint modeling. We identify different sources of domain shift and address them through four novel domain adaptation techniques - Domain-Adaptive Priors, Domain-Adaptive Fusion, Domain-Adaptive Smoothing and Bypass-RNN - in addition to an improved formulation of learned Gaussian priors. We integrate these techniques into a simple and lightweight encoder-RNN-decoder-style network, UNISAL, and train the entire network simultaneously with image and video saliency data. We evaluate our method on the video saliency datasets DHF1K, Hollywood-2 and UCF-Sports, as well as the image saliency datasets SALICON and MIT300. With one set of parameters, our method achieves state-of-the-art performance on all video saliency datasets and is on par with the state-of-the-art for image saliency prediction, despite a 5 to 20-fold reduction in model size and the fastest runtime among all competing deep models. We provide retrospective analyses and ablation studies which demonstrate the importance of the domain shift modeling. The code is available at https://github.com/rdroste/unisal."

# Summary. An optional shortened abstract.
summary: "arXiv preprint. *RD and JJ contributed equally to this work."

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
  url: https://arxiv.org/pdf/2003.05477.pdf
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
  url: https://arxiv.org/abs/2003.05477
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
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/unisal2020/#bibtex

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
@ARTICLE{drostejiao2020,
       author = {{Droste}, Richard and {Jiao}, Jianbo and {Noble}, J. Alison},
        title = "{Unified Image and Video Saliency Modeling}",
      journal = {arXiv e-prints},
     keywords = {Computer Science - Computer Vision and Pattern Recognition, Computer Science - Machine Learning},
         year = 2020,
        month = mar,
          eid = {arXiv:2003.05477},
        pages = {arXiv:2003.05477},
archivePrefix = {arXiv},
       eprint = {2003.05477},
 primaryClass = {cs.CV}
}
```
