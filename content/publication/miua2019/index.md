---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Towards Capturing Sonographic Experience: Cognition-Inspired Ultrasound Video Saliency Prediction"
# authors: [admin, yifan, harshita, pierre, aris, alison]
authors: ["**Richard Droste**", "Yifan Cai", "Harshita Sharma", "Pierre Chatelain", "Aris Papageorghiou", "J Alison Noble"]
date: 2019-07-25
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2019-07-25

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Medical Image Analysis and Understanding 2019"
publication_short: "MIUA 2019"

abstract: "For visual tasks like ultrasound (US) scanning, experts direct their gaze towards regions of task-relevant information. Therefore,
learning to predict the gaze of sonographers on US videos captures the
spatio-temporal patterns that are important for US scanning. The spatial
distribution of gaze points on video frames can be represented through
heat maps termed saliency maps. Here, we propose a temporally bidirectional model for video saliency prediction (BDS-Net), drawing inspiration
from modern theories of human cognition. The model consists of a convolutional neural network (CNN) encoder followed by a bidirectional gated-
recurrent-unit recurrent convolutional network (GRU-RCN) decoder. The
temporal bidirectionality mimics human cognition, which simultaneously
reacts to past and predicts future sensory inputs. We train the BDS-Net
alongside spatial and temporally one-directional comparative models on
the task of predicting saliency in videos of US abdominal circumference
plane detection. The BDS-Net outperforms the comparative models on
four out of five saliency metrics. We present a qualitative analysis on
representative examples to explain the model’s superior performance."

# Summary. An optional shortened abstract.
summary: "23rd Conference on Medical Image Understanding and Analysis (MIUA) 2019. **Oral presentation**. **Best paper award**."

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
  url: files/MIUA-2019_droste-et-al.pdf
  icon_pack: fas
  icon: file-pdf
- name: Slides
  icon_pack: fas
  icon: file-powerpoint
  url: https://drive.google.com/file/d/1Fwdz_oJunSDszcUxBwDkznQsxThJ1dFY/view?usp=sharing
- name: DOI
  url: https://doi.org/10.1007/978-3-030-39343-4_15
  icon_pack: ai
  icon: doi
- name: ORA
  url: https://ora.ox.ac.uk/objects/uuid:a14df633-3dc5-4918-ba90-09dda3f51363
  icon_pack: ai
  icon: open-access
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/miua2019/#bibtex

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
projects: [ipmi2019]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---



# BibTex

```
@InProceedings{
  author={Droste, Richard and Cai, Yifan and Sharma, Harshita and Chatelain, Pierre and Papageorghiou, Aris T. and Noble, J. Alison},
  title={Towards Capturing Sonographic Experience: Cognition-Inspired Ultrasound Video Saliency Prediction},
  booktitle={Medical Image Understanding and Analysis (MIUA)},
  series={CCIS},
  year={2019},
  publisher={Springer}
}
```


---

# Acknowledgments

This work is supported by the ERC ([ERC-ADG-2015 694581, project PULSE](https://cordis.europa.eu/project/rcn/205894/factsheet/en)) and the EPSRC (EP/GO36861/1 and EP/MO13774/1).
AP is funded by the NIHR Oxford Biomedical Research Centre.