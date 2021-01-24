# Awesome Pretrained Chinese NLP Models[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

在自然语言处理领域中，预训练语言模型（Pretrained Language Models）已成为非常重要的基础技术，本仓库主要收集了目前公开的一些高质量中文预训练模型，并将持续更新......

**注**: 🤗[huggingface](https://github.com/huggingface/transformers)模型下载地址: 1. [清华大学开源镜像](https://mirror.tuna.tsinghua.edu.cn/hugging-face-models/) 2. [官方地址](https://huggingface.co/models)

## BERT系列

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

> [1]wwm全称为**Whole Word Masking **,一个完整的词的部分WordPiece子词被mask，则同属该词的其他部分也会被mask
>
> [2]ext表示在更多数据集下训练
