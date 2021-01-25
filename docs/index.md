---
layout: default
---

## Abstract

#### Motivation
Deep learning can bring time savings and increased reproducibility to medical image analysis. However, acquiring 
training data is challenging due to the time-intensive nature of labeling and high inter-observer variability 
in annotations. Rather than labeling images, in this work we propose an alternative pipeline where images are 
generated from existing high-quality annotations using generative adversarial networks (GANs).

#### Summary 
Annotations are derived automatically from previously built anatomical models and are transformed into realistic 
synthetic ultrasound images with paired labels using a [CycleGAN](https://junyanz.github.io/CycleGAN/). 
We demonstrate the pipeline by generating 
synthetic 2D echocardiography images to compare with existing deep learning ultrasound segmentation datasets. 
A convolutional neural network is trained to segment the left ventricle and left atrium using only synthetic images.
Networks trained with synthetic images were extensively tested on four different unseen datasets of real images with 
median Dice scores of 91, 90, 88, and 87 for left ventricle segmentation. 
These results match or are better than inter-observer results measured on real ultrasound datasets and are 
comparable to a network trained on a separate set of real images. Results demonstrate the images produced can 
effectively be used in place of real data for training.

#### Conclusion

The proposed pipeline opens the door for automatic generation of training data for many tasks in medical 
imaging as the same process can be applied to other segmentation or landmark detection tasks in any modality. 

## Article

The article is available [online here](https://ieeexplore.ieee.org/document/9324763). 

Citation: 

A. Gilbert, M. Marciniak, C. Rodero, P. Lamata, E. Samset, and K. McLeod, "Generating Synthetic Labeled Data from
Existing Anatomical Models: An Example with Echocardiography Segmentation", *IEEE Trans. Med. Imaging*, 2021. 
doi: 10.1109/TMI.2021.3051806.


## Supplementary Materials

Appendices referenced in the article are [available here](https://github.com/adgilbert/data-generation/blob/main/SupplementaryMaterial.pdf)

## Data

### Anatomical Models

The paper describing the construction of the cardiac anatomical models used in this article is currently under review. 
A link will be provided here once published. 

Articles such as 
[(Strocchi et. al, 2020)](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0235145), 
[(Xu, 2014)](https://iopscience.iop.org/article/10.1088/0031-9155/59/18/R233),
[(Gosselin et. al, 2014)](https://iopscience.iop.org/article/10.1088/0031-9155/59/18/5287), and
[(Petoussi-Henss et. al, 2001)](https://iopscience.iop.org/article/10.1088/0031-9155/47/1/307) 
among numerous others provide links for accessing anatomical cardiac models and/or models of other anatomies. 
Most of these are free for academic use.  


### Echocardiography

Two publicly available echocardiography datasets were used for the evaluation of the pipeline, the 
[Camus dataset](https://www.creatis.insa-lyon.fr/Challenge/camus/) and the 
[EchoNet dataset](https://echonet.github.io/dynamic/). We would like to thank the authors 
[(Leclerc et. al, 2019)](https://ieeexplore.ieee.org/abstract/document/8649738) and 
[(Ouyang et. al, 2020)](https://www.nature.com/articles/s41586-020-2145-8) respectively for making these resources 
available.

[grand-challenge.org](https://grand-challenge.org/challenges/) provides an overview of several other open datasets in 
biomedical imaging.

## Code


The code is divided into four distinct modules which are mostly independent. More information on the structure is
contained [on the Github page](https://github.com/adgilbert/data-generation).


## Authors

Authors: Andrew Gilbert<sup>1,2</sup>, Maciej Marciniak<sup>3</sup>, Cristobal Rodero<sup>3</sup>, 
Pablo Lamata<sup>3</sup>, Eigil Samset<sup>1,2</sup>, Kristin McLeod<sup>1</sup>

1: GE Vingmed Ultrasound, Horten, NO

2: University of Oslo, Oslo, NO

3: King's College London, London, UK
