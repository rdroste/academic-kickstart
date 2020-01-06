---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Self-supervised Representation Learning for Ultrasound Video"
# authors: [admin, yifan, harshita, pierre, lior, aris, alison]
authors: ["Jianbo Jiao", "**Richard Droste**", "Lior Drukker", "Aris Papageorghiou", "J Alison Noble"]
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

abstract: "Recent advances in deep learning have achieved promising performance for medical image analysis, while in most cases ground-truth annotations from human experts are necessary to train the deep model. In practice, such annotations are expensive to collect and can be scarce for medical imaging applications. Therefore, there is significant interest in learning representations from unlabelled raw data. In this paper, we propose a self-supervised learning approach to learn meaningful and transferable representations from medical imaging video without any type of human annotation. We assume that in order to learn such a representation, the model should identify anatomical structures from the unlabelled data. Therefore we force the model to address anatomy-aware tasks with free supervision from the data itself. Specifically, the model is designed to correct the order of a reshuffled video clip and at the same time predict the geometric transformation applied to the video clip. Experiments on fetal ultrasound video show that the proposed approach can effectively learn meaningful and strong representations, which transfer well to downstream tasks like standard plane detection and saliency prediction."

# Summary. An optional shortened abstract.
summary: "IEEE International Symposium on Biomedical Imaging (ISBI) 2020."

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
# links:
# - name: PDF
#   url: https://arxiv.org/pdf/1903.02974.pdf
#   icon_pack: fas
#   icon: file-pdf
# - name: Poster
#   url: files/181_droste-et-al_ultrasound-visual-attention-modelling_v2-7.pdf
#   icon_pack: fas
#   icon: scroll
# - name: DOI
#   url: https://doi.org/10.1007/978-3-030-20351-1_46
#   icon_pack: ai
#   icon: doi
# - name: arXiv
#   url: https://arxiv.org/abs/1903.02974
#   icon_pack: ai
#   icon: arxiv
# - name: ORA
#   url: https://ora.ox.ac.uk/objects/uuid:a27fe42b-3a94-4b0f-bc7d-2173c0348b6f
#   icon_pack: ai
#   icon: open-access
# - name: Springer
#   url: https://link.springer.com/chapter/10.1007/978-3-030-20351-1_46
#   icon_pack: ai
#   icon: springer
# - name: BibTeX
#   icon_pack: fas
#   icon: quote-right
#   url: publication/ipmi2019/#bibtex

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

PDF and aper summary coming soon!

---

<!-- Richard Droste*, Yifan Cai, Harshita Sharma, Pierre Chatelain, Lior Drukker, Aris T. Papageorghiou, J. Alison Noble -->

<!-- # BibTex

```
@InProceedings{
  author={Droste, Richard and Cai, Yifan and Sharma, Harshita and Chatelain, Pierre and Drukker, Lior and Papageorghiou, Aris T. and Noble, J. Alison},
  title={Ultrasound Image Representation Learning by Modeling Sonographer Visual Attention},
  booktitle={Information Processing in Medical Imaging (IPMI)},
  volume=11492,
  series={LNCS},
  year={2019},
  publisher={Springer}
}
```


--- -->

# Acknowledgments

This work is supported by the ERC ([ERC-ADG-2015 694581, project PULSE](https://cordis.europa.eu/project/rcn/205894/factsheet/en)) and the EPSRC (EP/GO36861/1 and EP/MO13774/1).
AP is funded by the NIHR Oxford Biomedical Research Centre.



