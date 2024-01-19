# SegVol: Universal and Interactive Volumetric Medical Image Segmentation
This repo is the official implementation of [SegVol: Universal and Interactive Volumetric Medical Image Segmentation](https://arxiv.org/abs/2311.13385).

**Key words**: 3D medical SAM, volumetric image segmentation

<img src="https://github.com/BAAI-DCAI/SegVol/assets/60123629/3f0c440f-471f-415b-bc07-08ef1e5aeb98" width="100%" height="100%">


## News🚀
(2024.01.03) *A radar map about [**zero-shot experiment**](#jump) has been reported.* 🏆

(2023.12.25) *Our web tool **supports download results** now! You can use it as an online tool.* 🔥🔥🔥

(2023.12.15) *The training code has been uploaded!*

(2023.12.04) ***A web tool of SegVol is [here](https://huggingface.co/spaces/BAAI/SegVol)! Just enjoy it!*** 🔥🔥🔥

(2023.11.28) *Our model and demo case have been open-source at [huggingface/BAAI/SegVol](https://huggingface.co/BAAI/SegVol/tree/main).* 🤗🤗

(2023.11.28) *The usage of pre-trained ViT has been uploaded.* 

(2023.11.24) *You can download weight files of SegVol and ViT(CTs pre-train) from [huggingface/BAAI/SegVol](https://huggingface.co/BAAI/SegVol/tree/main) or [Google Drive](https://drive.google.com/drive/folders/1TEJtgctH534Ko5r4i79usJvqmXVuLf54?usp=drive_link).* 🔥🔥🔥

(2023.11.23) *The brief introduction and instruction have been uploaded.*

(2023.11.23) *The inference demo code has been uploaded.*

(2023.11.22) *The first edition of our paper has been uploaded to arXiv.* 📃


## [Web Tool](https://huggingface.co/spaces/BAAI/SegVol) of SegVol 📽
https://github.com/BAAI-DCAI/SegVol/assets/60123629/242a1578-e418-463c-9d53-a62eeb154c7d


## Introduction

![model_single](https://github.com/BAAI-DCAI/SegVol/assets/60123629/7aca9453-b139-469b-a3de-9401475806bf)



The SegVol is a universal and interactive model for volumetric medical image segmentation. SegVol accepts **point**, **box** and **text** prompt while output volumetric segmentation. By training on 90k unlabeled Computed Tomography (CT) volumes and 6k labeled CTs, this foundation model supports the segmentation of over 200 anatomical categories.

We will release SegVol's **inference code**, **training code**, **model params** and **ViT pre-training params** (pre-training is performed over 2,000 epochs on 96k  CTs). 

<span id="jump"></span>
## Zero-Shot Performance🏆
<img src="https://github.com/BAAI-DCAI/SegVol/assets/60123629/2f3b4683-f4c3-4f61-b108-f21d80ba5904" width="75%" height="75%">


We performed a zero-shot experiment using novel annotated dataset from the [ULS23 Challenge](https://uls23.grand-challenge.org/) (750 + 744 + 124 cases about lesions) and the validation dataset from [Amos22](https://amos22.grand-challenge.org/) (120 cases about organs). SegVol showed strong segmentation abilities compared to other medical SAM methods in accurately segmenting lesions and 15 important organs.

### Visualization🔍

![vis](https://github.com/BAAI-DCAI/SegVol/assets/60123629/d70098ec-d8cf-4b16-8b2b-4233cb992720)


## Usage
### Requirements
The [pytorch v1.11.0](https://pytorch.org/get-started/previous-versions/) (or higher version) is needed first. Following install key requirements using commands:

```
pip install 'monai[all]==0.9.0'
pip install einops==0.6.1
pip install transformers==4.18.0
pip install matplotlib
``` 
### Guideline for training and inference
[How to infer a demo case](https://github.com/BAAI-DCAI/SegVol/blob/main/documents/inference_demo.md).

[How to train SegVol](https://github.com/BAAI-DCAI/SegVol/blob/main/documents/training.md).

[How to use our pre-trained ViT as your model encoder](https://github.com/BAAI-DCAI/SegVol/blob/main/documents/pretrained_vit.md).

## Citation
If you find this repository helpful, please consider citing:
```
@article{du2023segvol,
  title={SegVol: Universal and Interactive Volumetric Medical Image Segmentation},
  author={Du, Yuxin and Bai, Fan and Huang, Tiejun and Zhao, Bo},
  journal={arXiv preprint arXiv:2311.13385},
  year={2023}
}
```

## Acknowledgement
Thanks for the following amazing works:

[HuggingFace](https://huggingface.co/).

[CLIP](https://github.com/openai/CLIP).

[MONAI](https://github.com/Project-MONAI/MONAI).

[Image by brgfx](https://www.freepik.com/free-vector/anatomical-structure-human-bodies_26353260.htm) on Freepik.

[Image by muammark](https://www.freepik.com/free-vector/people-icon-collection_1157380.htm#query=user&position=2&from_view=search&track=sph) on Freepik.




