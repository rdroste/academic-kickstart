---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Ultrasound Image Representation Learning by Modeling Sonographer Visual Attention"
# authors: [admin, yifan, harshita, pierre, lior, aris, alison]
authors: ["**Richard Droste**", "Yifan Cai", "Harshita Sharma", "Pierre Chatelain", "Lior Drukker", "Aris Papageorghiou", "J Alison Noble"]
date: 2019-03-07
doi:

# Schedule page publish date (NOT publication's date).
publishDate: 2019-03-07

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Information Processing in Medical Imaging (IPMI) 2019"
publication_short: "IPMI 2019"

abstract: "Image representations are commonly learned from class labels, which are a simplistic approximation of human image understanding.
In this paper we demonstrate that transferable representations of images can be learned without manual annotations by modeling human visual
attention.
The basis of our analyses is a unique gaze tracking dataset of sonographers performing routine clinical fetal anomaly screenings.
Models of sonographer visual attention are learned by training a convolutional neural network (CNN) to predict gaze on ultrasound video frames through visual saliency prediction or gaze-point regression.
We evaluate the transferability of the learned representations to the task of ultrasound standard plane detection in two contexts.
Firstly, we perform transfer learning by fine-tuning the CNN with a limited number of labeled standard plane images.
We find that fine-tuning the saliency predictor is superior to training from random initialization, with an average F1-score improvement of 9.6% overall and 15.3% for the cardiac planes.
Secondly, we train a simple softmax regression on the feature activations of each CNN layer in order to evaluate the representations independently of transfer learning hyper-parameters.
We find that the attention models derive strong representations, approaching the precision of a fully-supervised
baseline model for all but the last layer."

# Summary. An optional shortened abstract.
summary: "26th International conference on Information Processing in Medical Imaging (IPMI) 2019"

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
  url: https://arxiv.org/pdf/1903.02974.pdf
  icon_pack: fas
  icon: file-pdf
- name: Poster
  url: files/181_droste-et-al_ultrasound-visual-attention-modelling_v2-7.pdf
  icon_pack: fas
  icon: scroll
- name: DOI
  url: https://doi.org/10.1007/978-3-030-20351-1_46
  icon_pack: ai
  icon: doi
- name: arXiv
  url: https://arxiv.org/abs/1903.02974
  icon_pack: ai
  icon: arxiv
- name: ORA
  url: https://ora.ox.ac.uk/objects/uuid:a27fe42b-3a94-4b0f-bc7d-2173c0348b6f
  icon_pack: ai
  icon: open-access
- name: Springer
  url: https://link.springer.com/chapter/10.1007/978-3-030-20351-1_46
  icon_pack: ai
  icon: springer
- name: BibTeX
  icon_pack: fas
  icon: quote-right
  url: publication/ipmi2019/#bibtex

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



<!-- 
Richard Droste<sup>1</sup>, Yifan Cai<sup>1</sup>, Harshita Sharma<sup>1</sup>, Pierre Chatelain<sup>1</sup>, Lior Drukker<sup>2</sup>, Aris T. Papageorghiou<sup>2</sup>, J. Alison Noble<sup>1</sup>

<sup>1</sup> Department of Engineering Science, University of Oxford, UK  
<sup>2</sup> Nuffield Department of Women's & Reproductive Health, University of Oxford, UK


Accepted at the *26th biennial international conference on Information Processing in Medical Imaging* (IPMI 2019), The Hong Kong University of Science and Technology (HKUST) 

To appear in *Information Processing in Medical Imaging. IPMI 2019. Lecture Notes in Computer Science. Springer*

**Full text:** [arXiv](https://arxiv.org/abs/1903.02974) - [BibTex](#bibtex) - [ORA](https://ora.ox.ac.uk/objects/uuid:a27fe42b-3a94-4b0f-bc7d-2173c0348b6f) - [Springer](https://link.springer.com/chapter/10.1007/978-3-030-20351-1_46)
 -->


# Paper Summary

### Table of Contents

[Introduction](#introduction)  
[Representation Learning by Modeling Visual Attention](#representation_learning)  
[Transfer Learning](#transfer_learning)  
[Fixed Feature Extractor](#fixed_feature)  

### Introduction

Humans direct their visual attention towards semantically informative regions when interpreting images
[[Wu et al. 2017](https://www.frontiersin.org/articles/10.3389/fpsyg.2014.00054/full)].
The task of predicting the distribution of gaze points on images or video frames is referred to as visual saliency prediction, and CNNs are currently the most effective method to do so [[Borji 2018](https://arxiv.org/abs/1810.03716)].
While there has been extensive research on designing ever more accurate saliency predictors ([benchmarks](http://saliency.mit.edu/home.html)), little work has been devoted to making them useful for other computer vision tasks (exceptions include [Cornia et al. (2017)](https://ieeexplore.ieee.org/document/8026277) and [Cai et al. (2018)](https://ora.ox.ac.uk/objects/uuid:0198daa3-fcc0-4b5f-817a-ffdf6bd5e6c7)).
Here, we ask the question:
*To what extent can the representations learned purely based on gaze data be transferred to a challenging classification task?*


Specifically, we train a CNN to predict the gaze of sonographers while they perform routine fetal ultrasound scans, and evaluate that model on the task of detecting certain standard planes in the corresponding videos.
We implement two methods for predicting the sonographer gaze:
1. The model predicts the 2D scalar gaze point heat maps, termed saliency maps (usual approach)
2. The model directly regresses the gaze point on each video frame.

We refer to these models as visual attention models (VAMs), i.e., Saliency-VAM and Gaze-VAM.
We pose the task of standard plane detection analogously to [Baumgartner et al. (2016)](https://ieeexplore.ieee.org/document/7974824), and use their trained *SonoNet* model as a baseline.

<!-- 
There is some existing research on utilizing saliency prediction for computer vision tasks.
For example, [Cornia et al. (2017)](https://ieeexplore.ieee.org/document/8026277) use a pre-trained saliency predictor as an attention module within an image captioning architecture.
However, no representations are shared between the saliency predictor and the task-specific architecture.
[Cai et al. (2018)](https://ora.ox.ac.uk/objects/uuid:0198daa3-fcc0-4b5f-817a-ffdf6bd5e6c7) train a multi-task architecture to simultaneously predict class labels and saliency maps, while using the learned saliency predictor as an attention module.
In contrast, we show that transferable representations can be learned without manual annotations via visual attention modeling only.
 -->

Since the gaze data is acquired automatically, our work is related to *self-supervised learning*, which aims at learning representations from data without manual annotations by training on auxiliary prediction tasks.
A good example of self-supervised learning is the work of [Doersch et al. (2017)](https://arxiv.org/abs/1708.07860), who combine multiple auxiliary tasks such as colorization.
To the best of our knowledge, this work is the first attempt to study human visual attention modeling in the context of self-supervised representation learning.




### <a name="representation_learning"></a> Representation Learning by Modeling Visual Attention

<a name="fig1a"></a>
{{< figure src="figure1_3_a.svg" title="Fig. 1 a): Illustration of our framework for learning and evaluating visual attention models (VAMs)">}}


[Fig. 1 a)](#fig1a) illustrates our framework for training and evaluating the visual attention models (VAMs).
On random fetal ultrasound video frames, a dilated CNN is trained to either regress sonographer gaze points or to predict the 2D scalar saliency maps (see [Fig. 2](#fig2)).
Next, the dilations are removed (see [Fig. 1 b)](#fig1b)) and the network is evaluated on standard plane detection.
We evaluate two methods of transferring the learned representations:
1. The model is fine-tuned with a small set of a few hundred standard planes ([transfer learning](#transfer-learning))
2. Simple logistic regressions are fitted to different layers of the models in order to evaluate the features independently of transfer learning hyper-parameters ([fixed feature extractor](#fixed-feature-extractor))





### <a name="transfer_learning"></a> Transfer Learning

Table 3: Standard plane detection results after fine-tuning (mean ± standard deviation [%])
<a name="tab3"></a>

| Metrics 		| Rand. Init.	| Gaze-FT		| Saliency-FT	| SonoNet-FT		|
| ------------- | ------------- | ------------- | ------------- | ----------------- |
| Precision  	| 70.4 ± 2.3	| 67.2 ± 3.4	| 79.5 ± 1.7	| 82.3 ± 1.3 (81)	|
| Recall	  	| 64.9 ± 1.6	| 57.3 ± 4.5	| 75.1 ± 3.4	| 87.3 ± 1.1 (86)	|
| F1-Score  	| 67.0 ± 1.3	| 60.7 ± 3.9	| 76.6 ± 2.6	| 84.5 ± 0.9 (83)	|

<!-- | Standard plane detection results after fine-tuning (mean ± standard deviation [%]) | -->

<!-- The table above shows the standard plane detection scores after fine-tuning the visual attention models (VAMs). -->
The model that learned to regress gaze-points (Gaze-FT) doesn't improve over the model trained from random initialization (Rand. Init.).
The saliency predictor, in contrast, performs significantly better than Rand. Init.
In fact, its performance is closer to that of SonoNet, which had been pre-trained on over 22k labeled standard plane images (compared to 753 for fine-tuning).
The literature SonoNet scores are given in parenthesis.


### <a name="fixed_feature"></a> Fixed Feature Extractor

<a name="fig3a"></a>
{{< figure src="softmax_results_plot10_bg.svg" title="Fig. 3 a): Results of the regression analysis of the fixed-weight attention models, and baselines.">}}

The results of the regression analysis in [Fig. 3 a)](#fig3a) show that, even without fine-tuning, the high-level features of the attention models are predictive for fetal anomaly standard plane detection.
This supports our hypothesis, motivated by [Wu et al. (2017)](https://www.frontiersin.org/articles/10.3389/fpsyg.2014.00054/full), that gaze is a strong prior for semantic information.
At the last layer, the attention models fall behind SonoNet, indicating the task-specificity of that layer.
Rand. Feat. denotes a model with random weights.

<a name="fig3b"></a>
{{< figure src="tsne6.svg" title="Fig. 3 b): [t-SNE](https://lvdmaaten.github.io/tsne/) visualization of the feature embeddings at the respective layers with the highest F1-score (Background class omitted for legibility).">}}

The t-SNE plots in [Fig. 3 b)](#fig3b) confirm that some standard plane classes are separated in the respective feature spaces of the visual attention models (VAMs).
Compared to the fully-supervised model (SonoNet), a significant overlap remains for the standard planes with similar appearance such as the brain views and the cardiac views (4CH, 3VT, LVOT, RVOT), respectively.


---

# More Results

<a name="fig1b"></a>
{{< figure src="figure1_3_b.svg" title="Fig. 1 b): An illustration that a dilated convolution results in the same receptive field than downsampling + non-dilated convolution. We apply this fact to train a dilated network for saliency prediction (higher-resolution output) which is then used as a classifier by introducing downsampling and removing the dilations (faster, lower memory requirements).">}}


<a name="fig2"></a>
{{< figure src="sal_gaze_examples3.svg" title="Fig. 2: Visual saliency and gaze point predictions with corresponding ground truths for representative validation set frames.">}}

<!-- Some results of the saliency prediction model (Saliency-VAM) and the gaze-point regressor (Gaze-VAM). -->


<a name="appendixa"></a>
{{< figure src="confusion_matrix6.svg" title="Appendix A: Confusion matrices of *a)* the fine-tuned saliency model (Saliency-FT) and *b)* the baseline SonoNet model. The Saliency-FT model is pre-trained on random video frames for salieny prediction (no manual annotations) and the SonoNet model is pre-trained with over 22k labeled standard plane images. Then, both models are fine-tuned with 753 standard images.">}}


<a name="appendixb"></a>
{{< figure src="query2.svg" title="Appendix B: Nearest neighbors in the respective feature spaces. The first column shows various query images and the subsequent columns show the two nearest l2 neighbours in the (average-pooled) feature spaces of the last layer of each model.">}}



---

# BibTex
<!-- Richard Droste*, Yifan Cai, Harshita Sharma, Pierre Chatelain, Lior Drukker, Aris T. Papageorghiou, J. Alison Noble -->

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


---

# Acknowledgments

This work is supported by the ERC ([ERC-ADG-2015 694581, project PULSE](https://cordis.europa.eu/project/rcn/205894/factsheet/en)) and the EPSRC (EP/GO36861/1 and EP/MO13774/1).
AP is funded by the NIHR Oxford Biomedical Research Centre.



