# Awesome Pretrained Chinese NLP Models[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

在自然语言处理领域中，预训练语言模型（Pretrained Language Models）已成为非常重要的基础技术，本仓库主要收集了目前网上公开的一些高质量中文预训练模型(感谢分享资源的大佬)，并将持续更新......

**注**: 🤗[huggingface](https://github.com/huggingface/transformers)模型下载地址: 1. [清华大学开源镜像](https://mirror.tuna.tsinghua.edu.cn/hugging-face-models/) 2. [官方地址](https://huggingface.co/models)

# Expand Table of Contents

+ [NLU系列](#NLU系列)
  - [BERT](#BERT)
  - [RoBERTa](#RoBERTa)
  - [ALBERT](#ALBERT)
  - [NEZHA](#NEZHA)
  - [XLNET](#XLNET)
  - [MacBERT](#MacBERT)
  - [ELECTRA](#ELECTRA)
  - [ZEN](#ZEN)
  - [ ERNIE](#ERNIE)
+ [NLG系列](#NLG系列)
  - [GPT](#GPT)
  - [NEZHA-GEN](#NEZHA-GEN)


## NLU系列

### BERT

+ 2018 | BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding | Jacob Devlin, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1810.04805)
+ 2019 | Pre-Training with Whole Word Masking for Chinese BERT | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1906.08101)

| 模型            | 参数大小 | 语料大小                      | TensorFlow                                                   | PyTorch                                                      | 提供者                                                      | 源地址                                                       | 应用领域     | 备注 |
| --------------- | -------- | ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------------- | ------------------------------------------------------------ | ------------ | ---- |
| BERT-Base       | 110M     | 中文维基(词数0.4B)            | [Google Drive](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip) |                                                              | [Google Research](https://github.com/google-research)       | [bert](https://github.com/google-research/bert)              | 通用         |      |
| BERT-wwm        | 110M     | 中文维基(词数0.4B)            | [Google Drive](https://drive.google.com/open?id=1RoTQsXp2hkQ1gSRVylRIJfQxJUgkfJMW) [讯飞云-密码07Xj](http://pan.iflytek.com/#/link/A2483AD206EF85FD91569B498A3C3879) | [Google Drive](https://drive.google.com/open?id=1AQitrjbvCWc51SYiLN-cJq4e0WiNN4KY) | [Yiming Cui](https://github.com/ymcui)                      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用         |      |
| BERT-wwm-ext    | 110M     | 通用语料(词数5.4B)            | [Google Drive](https://drive.google.com/open?id=1buMLEjdtrXE2c4G1rpsNGWEx7lUQ0RHi) [讯飞云-密码4cMG](http://pan.iflytek.com/#/link/653637473FFF242C3869D77026C9BDB5) | [Google Drive](https://drive.google.com/open?id=1iNeYFhCBJWeUsIlnW_2K6SMwXkM4gLb_) | [Yiming Cui](https://github.com/ymcui)                      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用         |      |
| bert-base-民事  |          | 2654万民事文书                | [阿里云](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/ms.zip) |                                                              | [THUNLP](https://github.com/thunlp)                         | [OpenCLaP](https://github.com/thunlp/OpenCLaP)               | 司法         |      |
| bert-base-刑事  |          | 663万刑事文书                 | [阿里云](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/xs.zip) |                                                              | [THUNLP](https://github.com/thunlp)                         | [OpenCLaP](https://github.com/thunlp/OpenCLaP)               | 司法         |      |
| BAAI-JDAI-BERT  |          | 42G电商客服对话数据(词数9B)   | [京东云](https://jdai009.s3.cn-north-1.jdcloud-oss.com/jd-aig/open/models/nlp_baai/20190918/JDAI-BERT.tar.gz?AWSAccessKeyId=86FD402DD0CB693D629F6E62DC11E0E6&Expires=1634304356&Signature=dfnLvSzXeerRPSnMsZXSoEwdmkw%3D) |                                                              | [JDAI](https://github.com/jd-aig)                           | [pretrained_models_and_embeddings](https://github.com/jd-aig/nlp_baai/tree/master/pretrained_models_and_embeddings) | 电商客服对话 |      |
| FinBERT         |          | 400万金融领域数据(词数30亿)   | [Google Drive](https://drive.google.com/file/d/193B4sT63mMeh4zfge0FJbbFY447KiJXp/view?usp=sharing)   [百度网盘-密码1cmp](https://pan.baidu.com/share/init?surl=D-pVJyW6bbJSre5RxotJkA) | [Google Drive](https://drive.google.com/file/d/1qW1YWtw3q9Q28QThrIY-rDU9Gl-SLIKO/view?usp=sharing)   [百度网盘-密码986f](https://pan.baidu.com/share/init?surl=y_O586GBmZZ7g4d2nOF0Vg) | [Value Simplex](https://github.com/valuesimplex)            | [FinBERT](https://github.com/valuesimplex/FinBERT)           | 金融科技领域 |      |
| EduBERT         |          | 2000万教育领域数据(词数3.8亿) | [好未来AI](https://ai.100tal.com/download/TAL-EduBERT.zip)   | [tal-tech](https://github.com/tal-tech)                      | [tal-tech](https://github.com/tal-tech)                     | [edu-bert](https://github.com/tal-tech/edu-bert)             | 教育领域     |      |
| WoBERT          |          | 30通用语料+医学专业词典       | [百度网盘-密码kim2](https://pan.baidu.com/s/1BrdFSx9_n1q2uWBiQrpalw) |                                                              | [natureLanguageQing](https://github.com/natureLanguageQing) | [Medical_WoBERT](https://github.com/natureLanguageQing/Medical_WoBERT) | 医学领域     |      |
| MC-BERT         |          |                               | [Google Drive](https://drive.google.com/open?id=1ccXRvaeox5XCNP_aSk_ttLBY695Erlok) |                                                              | [Alibaba AI Research](https://github.com/alibaba-research)  | [ChineseBLUE](https://github.com/alibaba-research/ChineseBLUE) | 医学领域     |      |
| guwenbert-base  |          | 古代文献语料(词数1.7B)        |                                                              | [百度网盘-密码4jng](https://pan.baidu.com/s/1dw_08p7CVsz0jVj4jd58lQ)  [huggingface](https://huggingface.co/ethanyt/guwenbert-base) | [Ethan](https://github.com/Ethan-yt)                        | [guwenbert](https://github.com/Ethan-yt/guwenbert)           | 古文领域     |      |
| guwenbert-large |          | 古代文献语料(词数1.7B)        |                                                              | [百度网盘-密码m5sz](https://pan.baidu.com/s/1TL9mBIlIv2rSvp61xCkeJQ)  [huggingface](https://huggingface.co/ethanyt/guwenbert-large) | [Ethan](https://github.com/Ethan-yt)                        | [guwenbert](https://github.com/Ethan-yt/guwenbert)           | 古文领域     |      |

**备注**: 

[1] wwm全称为**Whole Word Masking **,一个完整的词的部分WordPiece子词被mask，则同属该词的其他部分也会被mask

[2] ext表示在更多数据集下训练

### RoBERTa

+ 2019 | RoBERTa: A Robustly Optimized BERT Pretraining Approach | Yinhan Liu, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1907.11692.pdf)


| 模型                   | 参数大小 | 语料大小           | TensorFlow                                                   | PyTorch                                                      | 提供者                                      | 源地址                                                       | 应用领域 | 备注 |
| ---------------------- | -------- | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------------------------ | -------- | ---- |
| RoBERTa-tiny-clue      | 7.5M     | 通用语料100G       | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny-clue.zip) | [百度网盘-密码8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [CLUEPretrainedModels](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |      |
| RoBERTa-tiny-pair      | 7.5M     | 通用语料100G       | [google drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny-pair.zip) | [百度网盘-密码8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [CLUEPretrainedModels](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |      |
| RoBERTa-tiny3L768-clue | 38M      | 通用语料100G       | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny3L768-clue.zip) |                                                              | [CLUE](https://github.com/CLUEbenchmark)    | [CLUEPretrainedModels](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |      |
| RoBERTa-tiny3L312-clue | <7.5M    | 通用语料100G       | [google drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny3L312-clue.zip) | [百度网盘-密码8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [CLUEPretrainedModels](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |      |
| RoBERTa-large-pair     | 290M     | 通用语料100G       | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-large-pair.zip) | [百度网盘-密码8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [CLUEPretrainedModels](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |      |
| RoBERTa-large-clue     | 290M     | 通用语料100G       | [google drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-large-clue.zip) | [百度网盘-密码8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [CLUEPretrainedModels](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |      |
| RBTL3                  |          | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/open?id=1Jzn1hYwmv0kXkfTeIvNT61Rn1IbRc-o8) [讯飞云-密码vySW](https://pan.iflytek.com/link/0DD18FAC080BAF75DBA28FB5C0047760) | [Google Drive](https://drive.google.com/open?id=1eHM3l4fMo6DsQYGmey7UZGiTmQquHw25) | [Yiming Cui](https://github.com/ymcui)      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用     |      |
| RBTL4                  |          | 通用语料(词数5.4B) | [讯飞云-密码e8dN](http://pan.iflytek.com/link/7B04C5BF09812DB241BBA973D649824C) |                                                              | [Yiming Cui](https://github.com/ymcui)      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用     |      |
| RBTL6                  |          | 通用语料(词数5.4B) | [讯飞云-密码XNMA](http://pan.iflytek.com/link/B935B1F701A8FD352CAA74614126C4A2) |                                                              | [Yiming Cui](https://github.com/ymcui)      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用     |      |
| RoBERTa-wwm-ext        |          | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/open?id=1jMAKIJmPn7kADgD3yQZhpsqM-IRM1qZt) [讯飞云-密码Xe1p](http://pan.iflytek.com/#/link/98D11FAAF0F0DBCB094EE19CCDBC98BF) | [Google Drive](https://drive.google.com/open?id=1eHM3l4fMo6DsQYGmey7UZGiTmQquHw25) | [Yiming Cui](https://github.com/ymcui)      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用     |      |
| RoBERTa-wwm-ext-large  |          | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/open?id=1dtad0FFzG11CBsawu8hvwwzU2R0FDI94) [讯飞云-密码u6gC](http://pan.iflytek.com/#/link/AC056611607108F33A744A0F56D0F6BE) | [Google Drive](https://drive.google.com/open?id=1-2vEZfIFCdM1-vJ3GD6DlSyKT4eVXMKq) | [Yiming Cui](https://github.com/ymcui)      | [Chinese-BERT-wwm](https://github.com/ymcui/Chinese-BERT-wwm) | 通用     |      |
| RoBERTa-base           |          | 通用语料30G        | [Google Drive](https://drive.google.com/open?id=1ykENKV7dIFAqRRQbZIh0mSb7Vjc2MeFA) [百度网盘](https://pan.baidu.com/s/1hAs7-VSn5HZWxBHQMHKkrg) | [Google Drive](https://drive.google.com/open?id=1H6f4tYlGXgug1DdhYzQVBuwIGAkAflwB)  [百度网盘](https://pan.baidu.com/s/1AGC76N7pZOzWuo8ua1AZfw) | [brightmart](https://github.com/brightmart) | [roberta_zh](https://github.com/brightmart/roberta_zh)       | 通用     |      |
| RoBERTa-Large          |          | 通用语料30G        | [Google Drive](https://drive.google.com/open?id=1W3WgPJWGVKlU9wpUYsdZuurAIFKvrl_Y) [百度网盘](https://pan.baidu.com/s/1Rk_QWqd7-wBTwycr91bmug) | [Google Drive](https://drive.google.com/open?id=1yK_P8VhWZtdgzaG0gJ3zUGOKWODitKXZ) | [brightmart](https://github.com/brightmart) | [roberta_zh](https://github.com/brightmart/roberta_zh)       | 通用     |      |


### ALBERT

+ 2019 | ALBERT: A Lite BERT For Self-Supervised Learning Of Language Representations | Zhenzhong Lan, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1909.11942.pdf)


| 模型             | 参数大小 | 语料大小    | TensorFlow                                                   | PyTorch                                                      | 提供者                                                | 源地址                                               | 应用领域 | 备注 |
| ---------------- | -------- | ----------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------- | ---------------------------------------------------- | -------- | ---- |
| Albert_base_zh   | 12M      | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_zh/albert_base_zh_additional_36k_steps.zip) | [Google Drive](https://drive.google.com/open?id=1HeijHGubWR-ElFnfxUf8IrRx7Ghm1S_Q) | [brightmart](https://github.com/brightmart)           | [albert_zh](https://github.com/brightmart/albert_zh) | 通用     |      |
| Albert_large_zh  |          | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_zh/albert_large_zh.zip) | [Google Drive](https://drive.google.com/open?id=1TAuv7OiFN8qbkT6S_VbfVbhkhg2GUF3q) | [brightmart](https://github.com/brightmart)           | [albert_zh](https://github.com/brightmart/albert_zh) | 通用     |      |
| Albert_xlarge_zh |          | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_zh/albert_xlarge_zh_183k.zip) | [Google Drive](https://drive.google.com/open?id=1kMhogQRX0uGWIGdNhm7-3hsmHlrzY_gp) | [brightmart](https://github.com/brightmart)           | [albert_zh](https://github.com/brightmart/albert_zh) | 通用     |      |
| Albert_base      |          | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_models/albert_base_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [ALBERT](https://github.com/google-research/ALBERT)  | 通用     |      |
| Albert_large     |          | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_models/albert_large_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [ALBERT](https://github.com/google-research/ALBERT)  | 通用     |      |
| Albert_xlarge    |          | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_models/albert_xlarge_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [ALBERT](https://github.com/google-research/ALBERT)  | 通用     |      |
| Albert_xxlarge   |          | 通用语料30G | [Google Drive](https://storage.googleapis.com/albert_models/albert_xxlarge_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [ALBERT](https://github.com/google-research/ALBERT)  | 通用     |      |

### NEZHA

+ 2019 | NEZHA: Neural Contextualized Representation for Chinese Language Understanding | Junqiu Wei, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1909.00204)

| 模型            | 参数大小 | 语料大小                | TensorFlow                                                   | PyTorch                                                      | 提供者                                                      | 源地址                                                       | 应用领域 | 备注 |
| --------------- | -------- | ----------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------------- | ------------------------------------------------------------ | -------- | ---- |
| NEZHA-base      |          |                         | [Google Drive](https://drive.google.com/drive/folders/1tFs-wMoXIY8zganI2hQgDBoDPqA8pSmh?usp=sharing) [百度网盘-密码ntn3](https://pan.baidu.com/s/1UVQjy9v_Sv4cQd1ELdjqww) | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI Noah's Ark Lab](https://github.com/huawei-noah)     | [link](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |      |
| NEZHA-base-WWM  |          |                         | [Google Drive](https://drive.google.com/drive/folders/1bK6WbqAG-B6BX2d9RPprnh2MPK6zL0t_?usp=sharing) [百度网盘-密码f68o](https://pan.baidu.com/s/1-YG8e5V2zKCnR3azsGZT1w) | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI Noah's Ark Lab](https://github.com/huawei-noah)     | [link](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |      |
| NEZHA-large     |          |                         | [Google Drive](https://drive.google.com/drive/folders/1ZPPM5XtTTOrS_CDRak1t2nCBU-LFZ_zs?usp=sharing) [百度网盘-密码7thu](https://pan.baidu.com/s/1R1Ew-Lu8oIP6QhWO6nqp5Q) | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI Noah's Ark Lab](https://github.com/huawei-noah)     | [link](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |      |
| NEZHA-large-WWM |          |                         | [Google Drive](https://drive.google.com/drive/folders/1LOAUc9LXyogC2gmP_q1ojqj41Ez01aga?usp=sharing) [百度网盘-ni4o](https://pan.baidu.com/s/1JK1RLIJd2wpuypku3stt8w) | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI Noah's Ark Lab](https://github.com/huawei-noah)     | [link](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |      |
| NEZHA-Gen       |          |                         | [Google Drive](https://drive.google.com/drive/folders/1B5-jxUlzhoKwFVMQ-nkqqbmJQgr1lRAp?usp=sharing)  [百度网盘-密码ytim](https://pan.baidu.com/s/1me6_BGYHbWFdTi80vRQ2Lg) |                                                              | [HUAWEI Noah's Ark Lab](https://github.com/huawei-noah)     | [link](https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/NEZHA-Gen-TensorFlow) | 通用     |      |
| NEZHA-Gen       |          |                         | [Google Drive](https://drive.google.com/drive/folders/1i4f_8LhaVDNjnGlLXNJ0rNgBP0E4L6V0?usp=sharing)  [百度网盘-密码rb5m](https://pan.baidu.com/s/1Bgle8TpcxHyuUz_jAXOBWw) |                                                              | [HUAWEI Noah's Ark Lab](https://github.com/huawei-noah)     | [link](https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/NEZHA-Gen-TensorFlow) |          |      |
| WoNEZHA         |          | 30通用语料+医学专业词典 | [百度网盘-密码qgkq](https://pan.baidu.com/s/1ABKwUuIiMEEsRXxxlbyKmw) |                                                              | [natureLanguageQing](https://github.com/natureLanguageQing) | [link](https://github.com/natureLanguageQing/Medical_WoBERT) | 医学领域 |      |

### MacBERT

+ 2020 | Revisiting Pre-Trained Models for Chinese Natural Language Processing | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2004.13922.pdf)

| 模型          | 参数大小 | 语料大小           | TensorFlow                                                   | PyTorch | 提供者                                 | 源地址                                   | 应用领域 | 备注 |
| ------------- | -------- | ------------------ | ------------------------------------------------------------ | ------- | -------------------------------------- | ---------------------------------------- | -------- | ---- |
| MacBERT-base  | 102M     | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/file/d/1aV69OhYzIwj_hn-kO1RiBa-m8QAusQ5b/view?usp=sharing) [讯飞云-密码E2cP](http://pan.iflytek.com/#/link/CF2A1F9AEBF859650E8956854A994C1B) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/MacBERT) | 通用     |      |
| MacBERT-large | 324M     | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/file/d/1lWYxnk1EqTA2Q20_IShxBrCPc5VSDCkT/view?usp=sharing) [讯飞云-密码3Yg3](http://pan.iflytek.com/#/link/805D743F3826EC4F4EB5C774D34432AE) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/MacBERT) | 通用     |      |

### XLNET

+ 2019 | XLNet: Generalized Autoregressive Pretraining for Language Understanding | Zhilin Yang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1906.08237)


| 模型           | 参数大小 | 语料大小           | TensorFlow                                                   | PyTorch                                                      | 提供者                                      | 源地址                                         | 应用领域 | 备注 |
| -------------- | -------- | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------- | ---------------------------------------------- | -------- | ---- |
| XLNet-base     | 117M     | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/open?id=1m9t-a4gKimbkP5rqGXXsEAEPhJSZ8tvx) [讯飞云-密码uCpe](http://pan.iflytek.com/#/link/32619C31BDEFAF2D82CB8C7F66F01D5C) | [Google Drive](https://drive.google.com/open?id=1mPDgcMfpqAf2wk9Nl8OaMj654pYrWXaR) | [Yiming Cui](https://github.com/ymcui)      | [link](https://github.com/ymcui/Chinese-XLNet) | 通用     |      |
| XLNet-mid      | 209M     | 通用语料(词数5.4B) | [Google Drive](https://drive.google.com/open?id=1342uBc7ZmQwV6Hm6eUIN_OnBSz1LcvfA) [讯飞云-密码68En](http://pan.iflytek.com/#/link/ED7DF7ED04B871AFE8E4D97704B9134D) | [Google Drive](https://drive.google.com/open?id=1u-UmsJGy5wkXgbNK4w9uRnC0RxHLXhxy) | [Yiming Cui](https://github.com/ymcui)      | [link](https://github.com/ymcui/Chinese-XLNet) | 通用     |      |
| XLNet_zh_Large |          |                    | [百度网盘](https://pan.baidu.com/s/1dy0Z27DoZdMpSmoz1Q4G5A)  |                                                              | [brightmart](https://github.com/brightmart) | [link](https://github.com/brightmart/xlnet_zh) | 通用     |      |

### ELECTRA

+ 2020 | ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators | Kevin Clark, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2003.10555)


| 模型                  | 参数大小 | 语料大小 | TensorFlow                                                   | PyTorch | 提供者                                 | 源地址                                           | 应用领域 | 备注 |
| --------------------- | -------- | -------- | ------------------------------------------------------------ | ------- | -------------------------------------- | ------------------------------------------------ | -------- | ---- |
| ELECTRA-180g-large    |          |          | [Google Drive](https://drive.google.com/file/d/1P9yAuW0-HR7WvZ2r2weTnx3slo6f5u9q/view?usp=sharing) [讯飞云-密码Yfcy](http://pan.iflytek.com/#/link/7605874F5A11CD693C60EAB79005CCF3) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |      |
| ELECTRA-180g-small-ex |          |          | [Google Drive](https://drive.google.com/file/d/1NYJTKH1dWzrIBi86VSUK-Ml9Dsso_kuf/view?usp=sharing) [讯飞云-密码GUdp](http://pan.iflytek.com/#/link/3EFCF909FC5CFEA6F0EA7AA774C64CF0) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |      |
| ELECTRA-180g-base     |          |          | [Google Drive](https://drive.google.com/file/d/1RlmfBgyEwKVBFagafYvJgyCGuj7cTHfh/view?usp=sharing) [讯飞云-密码Xcvm](http://pan.iflytek.com/#/link/38E14C9BDBE8E93F09DFE2198E308489) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |      |
| ELECTRA-180g-small    |          |          | [Google Drive](https://drive.google.com/file/d/177EVNTQpH2BRW-35-0LNLjV86MuDnEmu/view?usp=sharing) [讯飞云-密码qsHj](http://pan.iflytek.com/#/link/D1B8FE678FA5BC31AA43BD99AD09913E) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |      |
| legal-ELECTRA-large   |          |          | [Google Drive](https://drive.google.com/file/d/1jPyVi_t4QmTkFy7PD-m-hG-lQ8cIETzD/view?usp=sharing) [讯飞云-密码7f7b](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |      |
| legal-ELECTRA-base    |          |          | [Google Drive](https://drive.google.com/file/d/12ZLaoFgpqGJxSi_9KiQV-jdVN4XRGMiD/view?usp=sharing) [讯飞云-密码7f7b](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |      |
| legal-ELECTRA-small   |          |          | [Google Drive](https://drive.google.com/file/d/1arQ5qNTNoc1OyMH8wBUKdTMy2QponIFY/view?usp=sharing) [讯飞云-密码7f7b](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759) |         | [Yiming Cui](https://github.com/ymcui) | [link](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |      |

### ZEN

+ 2019 | ZEN: Pre-training Chinese Text Encoder Enhanced by N-gram Representations | Zhilin Yang, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1911.00720.pdf)

| 模型     | 参数大小 | 语料大小 | TensorFlow | PyTorch                                                      | 提供者                                                       | 源地址                                    | 应用领域 | 备注 |
| -------- | -------- | -------- | ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------- | -------- | ---- |
| ZEN-Base |          |          |            | [Google Drive](https://drive.google.com/open?id=1oxNdYMQOpFe3QlttH98bAqg_FQiiVeMr) [百度网盘](https://pan.baidu.com/s/1E2ylFnzGSkwBc8tY_OqZYg) | [Sinovation Ventures AI Institute](https://github.com/sinovation) | [link](https://github.com/sinovation/ZEN) | 通用     |      |

### ERNIE

+ 2019 | ERNIE: Enhanced Representation through Knowledge Integration | Yu Sun, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1904.09223)

+ 2020 | SKEP: Sentiment Knowledge Enhanced Pre-training for Sentiment Analysis | Hao Tian, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2005.05635)

| 模型                    | 参数大小 | 语料大小 | PaddlePaddle                                                 | PyTorch                                                      | 提供者                                          | 源地址                                        | 应用领域 | 备注 |
| ----------------------- | -------- | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------- | --------------------------------------------- | -------- | ---- |
| ernie-1.0-base          |          |          | [link](https://ernie-github.cdn.bcebos.com/model-ernie1.0.1.tar.gz) | [[nghuyong](https://github.com/nghuyong)云盘](http://pan.nghuyong.top/#/s/y7Uz) | [PaddlePaddle](https://github.com/PaddlePaddle) | [link](https://github.com/PaddlePaddle/ERNIE) | 通用     |      |
| ernie_1.0_skep_large_ch |          |          | [link](https://senta.bj.bcebos.com/skep/ernie_1.0_skep_large_ch.tar.gz) |                                                              | [Baidu](https://github.com/baidu)               | [link](https://github.com/baidu/Senta)        | 情感分析 |      |

## NLG系列

### GPT

+ 2019 | Improving Language Understandingby Generative Pre-Training | Alec Radford, et al. | arXiv | [`PDF`](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)

+ 2019 | Language Models are Unsupervised Multitask Learners | Alec Radford, et al. | arXiv | [`PDF`](https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf)

| 模型                | 参数大小 | 语料大小                                                     | TensorFlow | PyTorch                                                      | 提供者                                          | 源地址                                                       | 应用领域 | 备注 |
| ------------------- | -------- | ------------------------------------------------------------ | ---------- | ------------------------------------------------------------ | ----------------------------------------------- | ------------------------------------------------------------ | -------- | ---- |
| GPT2                | 15亿     | 30G                                                          |            | [Google Drive](https://drive.google.com/file/d/1mT_qCQg4AWnAXTwKfsyyRWCRpgPrBJS3) [百度网盘-密码ffz6](https://pan.baidu.com/s/1yiuTHXUr2DpyBqmFYLJH6A) | [Caspar ZHANG](https://github.com/imcaspar)     | [gpt2-ml](https://github.com/imcaspar/gpt2-ml)               |          |      |
| GPT2                | 15亿     | 15G                                                          |            | [Google Drive](https://drive.google.com/file/d/1IzWpQ6I2IgfV7CldZvFJnZ9byNDZdO4n) [百度网盘-密码q9vr](https://pan.baidu.com/s/1TA_3e-u2bXg_hcx_NwVbGw) | [Caspar ZHANG](https://github.com/imcaspar)     | [gpt2-ml](https://github.com/imcaspar/gpt2-ml)               |          |      |
| CDial-GPTLCCC-base  | 95.5M    | LCCC-base                                                    |            | [huggingface]](https://huggingface.co/thu-coai/CDial-GPT_LCCC-base) | [thu-coai](https://github.com/thu-coai)         | [CDial-GPT](https://github.com/thu-coai/CDial-GPT)           |          |      |
| CDial-GPT2LCCC-base | 95.5M    | LCCC-base                                                    |            | [huggingface]](https://huggingface.co/thu-coai/CDial-GPT2_LCCC-base) | [thu-coai](https://github.com/thu-coai)         | [CDial-GPT](https://github.com/thu-coai/CDial-GPT)           |          |      |
| CDial-GPTLCCC-large | 95.5M    | LCCC-large                                                   |            | [huggingface]](https://huggingface.co/thu-coai/CDial-GPT_LCCC-large) | [thu-coai](https://github.com/thu-coai)         | [CDial-GPT](https://github.com/thu-coai/CDial-GPT)           |          |      |
| GPT2-dialogue       |          | [常见中文闲聊](https://github.com/codemayq/chinese_chatbot_corpus) |            | [Google Drive](https://drive.google.com/drive/folders/1Ogz3eapvtvdY4VUcY9AEwMbNRivLKhri?usp=sharing)  [百度网盘-密码osi6](https://pan.baidu.com/s/1qDZ24VKLBU9GKARX9Ev65g) | [yangjianxin1](https://github.com/yangjianxin1) | [GPT2-chitchat](https://github.com/yangjianxin1/GPT2-chitchat) |          |      |
| GPT2-mmi            |          | 50w中文闲聊语料 [百度网盘-密码jk8d](https://pan.baidu.com/s/1mkP59GyF9CZ8_r1F864GEQ) [GoogleDrive](https://drive.google.com/file/d/1nEuew_KNpTMbyy7BO4c8bXMXN351RCPp/view?usp=sharing) |            | [Google Drive](https://drive.google.com/drive/folders/1oWgKXP6VG_sT_2VMrm0xL4uOqfYwzgUP?usp=sharing)  [百度网盘-密码1j88](https://pan.baidu.com/s/1ubXGuEvY8KmwEjIVTJVLww) | [yangjianxin1](https://github.com/yangjianxin1) | [GPT2-chitchat](https://github.com/yangjianxin1/GPT2-chitchat) |          |      |
| GPT2-散文模型       |          | 130MB散文数据集                                              |            | [Google Drive](https://drive.google.com/drive/folders/1rJC4niJKMVwixUQkuL9k5teLRnEYTmUf?usp=sharing)  [百度网盘-密码fpyu](https://pan.baidu.com/s/1nbrW5iw34GRhoTin8uU2tQ) | [Zeyao Du](https://github.com/Morizeyao)        | [GPT2-Chinese](https://github.com/Morizeyao/GPT2-Chinese)    |          |      |
| GPT2-诗词模型       |          | 180MB古诗词数据集                                            |            | [Google Drive](https://drive.google.com/drive/folders/1Z6nF1nrgTkrZcRLHedQHXb4_M9I7yQPN?usp=sharing)  [百度网盘-密码7fev](https://pan.baidu.com/s/1Hy0OQ5xZcTLer9MQZW8o3g) | [Zeyao Du](https://github.com/Morizeyao)        | [GPT2-Chinese](https://github.com/Morizeyao/GPT2-Chinese)    |          |      |
| GPT2-对联模型       |          | 40MB对联数据集                                               |            | [Google Drive](https://drive.google.com/drive/folders/1ZnsvS7oHRVueNKj_SeEhiQt86aze3ojj?usp=sharing)  [百度网盘-密码i5n0](https://pan.baidu.com/s/1j9yVQwjlXZq58wOyXK4lcg) | [Zeyao Du](https://github.com/Morizeyao)        | [GPT2-Chinese](https://github.com/Morizeyao/GPT2-Chinese)    |          |      |
