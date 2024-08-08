# CSFND
The implement for Repository "[CSFND_yanjie](https://github.com/ml-master/CSFND_yanjie)"by **lyq**@[LYQ1-ai](https://github.com/LYQ1-ai)
# Quick Start
## Requirements
```shell
$ conda env create -f myimplement.yml
$ pip install pipRequirements.txt
```

### NOTICE
- python == 3.7.9
- pytroch == pytorch=1.11.0=py3.7_cuda11.3_cudnn8.2.0_0
- transformers==4.11.3

## Dataset
For the original data, you can download from these links.
- Weibo & Twitter:    [dataset in MRML](https://github.com/plw-study/MRML)
  
- Gossipcop:    [Gossipcop-LLM](https://github.com/junyachen/Data-examples?tab=readme-ov-file)
   - In this mode, we use the ```gossipcop_v3_origin.json```
   - run the **data_process_mydataset.ipynb**, then you can get the corresponding **trian / valid / test** data

## Pre-trained Model
If you cannot download it online, please download the corresponding pre-trained model through these links.
And then put them in the correct place.
- BERT
  - bert_base_uncased [Link](https://huggingface.co/google-bert/bert-base-uncased)
  - bert_base_chinese [Link](https://huggingface.co/google-bert/bert-base-chinese)
- VGG19 [Link](https://download.pytorch.org/models/vgg19-dcbb9e9d.pth)

## Structure
You need to follow the structure to ensure the project can run normally.
```
├── CSFND
│   └── model
│       ├── bert_base_chinese
│       ├── bert_base_uncased
│       └── vgg19-dcbb9e9d.pth
├── gossipcop_dataset
├── myimplement.txt
├── README.md
├── twitter_dataset
└── weibo_dataset
```

## Running
```
PYTHONUNBUFFERED=1 CUDA_VISIBLE_DEVICES=0 nohup python run.py --dataset=gossipcop_glm_origin
```

## Results

### Main Results
| acc    | acc_real | acc\_fake |
| ------ | -------- | --------- |
| 0.6702 | 0.6601   | 0.7028    |



# Reference
```
@article{PENG2024103564,
title = {Not all fake news is semantically similar: Contextual semantic representation learning for multimodal fake news detection},
journal = {Information Processing & Management},
volume = {61},
number = {1},
pages = {103564},
year = {2024},
issn = {0306-4573},
doi = {https://doi.org/10.1016/j.ipm.2023.103564},
url = {https://www.sciencedirect.com/science/article/pii/S0306457323003011},
author = {Liwen Peng and Songlei Jian and Zhigang Kan and Linbo Qiao and Dongsheng Li},
keywords = {Fake news detection, Multimodal learning, Social network, Representation learning, Deep learning}
}
```
