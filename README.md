# Awesome Pretrained Chinese NLP Models[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

在自然语言处理领域中，预训练语言模型（Pretrained Language Models）已成为非常重要的基础技术，本仓库主要收集了目前公开的一些高质量中文预训练模型，并将持续更新......

**注**: 🤗[huggingface](https://github.com/huggingface/transformers)模型下载地址: 1. [清华大学开源镜像](https://mirror.tuna.tsinghua.edu.cn/hugging-face-models/) 2. [官方地址](https://huggingface.co/models)

## BERT系列

### BERT

+ 2018 | BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding | Jacob Devlin, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1810.04805)

+ 2019 | Pre-Training with Whole Word Masking for Chinese BERT | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1906.08101)

>模型: BERT-Base
>
>参数大小: 110M
>
>语料大小: 中文维基(词数0.4B)
>
>TensorFlow: [Google Drive](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip)
>
>PyTorch:
>
>提供者: [Google Research](https://github.com/google-research)
>
>源地址: [bert](https://github.com/google-research/bert)
>
>应用领域: 通用

>模型: BERT-Base
>
>参数大小: 110M
>
>语料大小: 中文维基(词数0.4B)
>
>TensorFlow: [Google Drive](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip)
>
>PyTorch:
>
>提供者: [Google Research](https://github.com/google-research)
>
>源地址: [bert](https://github.com/google-research/bert)
>
>应用领域: 通用
**备注**: 

> [1]wwm全称为**Whole Word Masking **,一个完整的词的部分WordPiece子词被mask，则同属该词的其他部分也会被mask
>
> [2]ext表示在更多数据集下训练
