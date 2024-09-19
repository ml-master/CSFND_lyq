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
   - run the **data_process.ipynb.ipynb**, then you can get the corresponding **trian / valid / test** data

## Pre-trained Model
If you cannot download it online, please download the corresponding pre-trained model through these links.
And then put them in the correct place.
- BERT
  - bert_base_uncased [Link](https://huggingface.co/google-bert/bert-base-uncased)
  - bert_base_chinese [Link](https://huggingface.co/google-bert/bert-base-chinese)
  - bert-base-multilingual-uncased [Link](https://huggingface.co/google-bert/bert-base-multilingual-uncased)
- VGG19 [Link](https://download.pytorch.org/models/vgg19-dcbb9e9d.pth)

## Structure
You need to follow the structure to ensure the project can run normally.
```
├── CSFND
│   └── model
│       ├── bert_base_chinese
│       ├── bert_base_uncased
│       ├── bert-base-multilingual-cased
│       └── vgg19-dcbb9e9d.pth
├── gossipcop_dataset
├── twitter_dataset
├── weibo_dataset
├── myimplement.txt
├── README.md
```

## Running
```
PYTHONUNBUFFERED=1 CUDA_VISIBLE_DEVICES=0 nohup python run.py --dataset=gossipcop_glm_origin
```

## Results

### Main Results
| data_set         | acc    | acc_real | acc\_fake |
| ---------------- | ------ | -------- | --------- |
| gossipcop_origin | 0.6702 | 0.6601   | 0.7028    |
| weibo            | 0.6875 | 0.6264   | 0.7398    |
| twitter          | 0.6932 | 0.5873   | 0.7785    |
| 新twitter        | 0.5831 | 0.4417   | 0.6975    |

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
