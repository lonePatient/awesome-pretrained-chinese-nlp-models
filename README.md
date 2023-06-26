# Awesome Pretrained Chinese NLP Models[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

![](/resources/LLMS.png)
<div align="center"> 图片来自于论文: [A Survey of Large Language Models](https://arxiv.org/pdf/2303.18223.pdf) </div>

在自然语言处理领域中，预训练语言模型（Pretrained Language Models）已成为非常重要的基础技术，本仓库主要收集目前网上公开的一些高质量中文预训练模型(感谢分享资源的大佬)，并将持续更新......

# Expand Table of Contents
+ [更新日志](#更新)

+ [基础大模型](#LLM)

+ [对话大模型](#ChatLLM)

+ [多模态对话大模型](#MultiModal-ChatLLM)

+ [大模型评估基准](#大模型评估基准)

+ [在线体验大模型](#在线体验大模型)

+ [开源模型库平台](#开源模型库平台)

+ [开源数据集库](#开源数据集库)

+ [开源中文指令数据集](#中文指令数据集)

+ <details><summary>NLU系列</summary>
  
  - [BERT](#BERT)
  - [RoBERTa](#RoBERTa)
  - [ALBERT](#ALBERT)
  - [NEZHA](#NEZHA)
  - [XLNET](#XLNET)
  - [MacBERT](#MacBERT)
  - [WoBERT](#WoBERT)
  - [ELECTRA](#ELECTRA)
  - [ZEN](#ZEN)
  - [ERNIE](#ERNIE)
  - [ERNIE3](#ERNIE3)
  - [RoFormer](#RoFormer)
  - [StructBERT](#StructBERT)
  - [Lattice-BERT](#Lattice-BERT)
  - [Mengzi-BERT](#Mengzi-BERT)
  - [ChineseBERT](#ChineseBERT)
  - [TaCL](#TaCL) 
  - [MC-BERT](#MC-BERT)
  - [二郎神](#二郎神)
  - [PERT](#PERT)
  - [MobileBERT](#MobileBERT)
  - [GAU-α](#GAU-α)
  - [DeBERTa](#DeBERTa)
  - [GlyphBERT](#GlyphBERT)
  - [CKBERT](#CKBERT)
  - [LERT](#LERT)
  - [RoCBert](#RoCBert)
  - [m3e](#M3E)
  - [LEALLA](#LEALLA)
  

</details>

+ <details><summary>NLG系列</summary>
  
  - [GPT](#GPT)
  - [GPT-3](#GPT-3)
  - [NEZHA-GEN](#NEZHA-GEN)
  - [CPM-Generate](#CPM-Generate)
  - [T5](#T5)
  - [T5-PEGASUS](#T5-PEGASUS)
  - [Mengzi-T5](#Mengzi-T5)
  - [盘古α](#PanGu-Alpha)
  - [EVA](#EVA)
  - [BART](#BART)
  - [闻仲](#闻仲)
  - [余元](#余元)
  - [RWKV](#RWKV)
  - [Bloom](#Bloom)
  - [PromptCLUE](#PromptCLUE)
  - [ChatYuan](#ChatYuan)
  - [SkyText](#SkyText)
  - [ProphetNet](#ProphetNet)
  

</details>

+ <details><summary>NLU-NLG系列</summary>
  
  - [UniLM](#UniLM)
  - [Simbert](#Simbert)
  - [RoFormer-sim](#RoFormer-sim)
  - [CPM-2](#CPM-2)
  - [CPT](#CPT)
  - [周文王](#周文王)
  - [GLM](#GLM)
  - [PLUG](#PLUG)
  - [OPD](#OPD)
</details>

+ <details><summary>Multi-Modal</summary>
  
  - [WenLan](#WenLan)
  - [CogView](#CogView)
  - [紫东太初](#紫东太初)
  - [Mengzi-oscar](#Mengzi-oscar)
  - [R2D2](#R2D2)
  - [Chinese-CLIP](#Chinese-CLIP)
  - [TaiYi-CLIP](#TaiYi-CLIP)
  - [AltCLIP](#AltCLIP)
  - [AltDiffusion](#AltDiffusion)
  - [Taiyi-Stable-Diffusion](#Taiyi-Stable-Diffusion)
  - [wukong](#wukong)
  - [OFA](#OFA)
  - [QA-CLIP](#QA-CLIP)
  

</details>

+ <details><summary>Table</summary>
  
  - [SDCUP](#SDCUP)
  

</details>


## LLM

> 大规模基础模型：表格中只罗列出参数量`大于7B`以上模型。
> ND:  Non-Causal Decoder or Prefix LM
> CD:  Causal Decoder
> ED:  Encoder-Decoder

|         模型         | 大小 | 时间    | 语言 | 领域 |                             下载                             |                           项目地址                           |                          机构/个人                           | 架构 |                             文献                             | 备注 |
| :------------------: | :--: | ------- | :--: | ---- | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :--: | :----------------------------------------------------------: | ---- |
|     Baichuan-7B      |  7B  | 2023-06 | 中英 | 通用 |   [ckpt](https://huggingface.co/baichuan-inc/baichuan-7B)    | [baichuan-7B](https://github.com/baichuan-inc/baichuan-7B)![Star](https://img.shields.io/github/stars/baichuan-inc/baichuan-7B.svg?style=social&label=Star) |         [百川智能](https://github.com/baichuan-inc)          |  CD  |                                                              |      |
|  Chinese-Falcon-7B   |  7B  | 2023-06 | 中英 | 通用 |  [ckpt](https://huggingface.co/Linly-AI/Chinese-Falcon-7B)   | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) |    [深圳大学计算机视觉研究所](https://github.com/CVI-SZU)    |  CD  |        [Blog](https://zhuanlan.zhihu.com/p/636994073)        |      |
|      AtomGPT_8k      | 13B  | 2023-06 | 中英 | 通用 |     [ckpt](https://huggingface.co/AtomEchoAI/AtomGPT_8k)     | [AtomGPT](https://github.com/AtomEcho/AtomGPT)![Star](https://img.shields.io/github/stars/AtomEcho/AtomGPT.svg?style=social&label=Star) |           [原子回声](https://github.com/AtomEcho)            |  CD  |                                                              |      |
|   AquilaCode-7B-NV   |  7B  | 2023-06 | 中英 | 代码 |     [ckpt](https://model.baai.ac.cn/model-detail/100099)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)![Star](https://img.shields.io/github/stars/FlagAI-Open/FlagAI.svg?style=social&label=Star) |          [智源研究院](https://huggingface.co/BAAI)           |  CD  |                                                              |      |
|   AquilaCode-7B-TS   |  7B  | 2023-06 | 中英 | 代码 |     [ckpt](https://model.baai.ac.cn/model-detail/100099)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)![Star](https://img.shields.io/github/stars/FlagAI-Open/FlagAI.svg?style=social&label=Star) |          [智源研究院](https://huggingface.co/BAAI)           |  CD  |                                                              |      |
|      Aquila-7B       |  7B  | 2023-06 | 中英 | 通用 |     [ckpt](https://model.baai.ac.cn/model-detail/100098)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)![Star](https://img.shields.io/github/stars/FlagAI-Open/FlagAI.svg?style=social&label=Star) |          [智源研究院](https://huggingface.co/BAAI)           |  CD  |                                                              |      |
|  Chinese-LLaMA-33B   | 33B  | 2023-06 | 中英 | 通用 | [ckpt](https://huggingface.co/ziqingyang/chinese-llama-lora-33b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)![Star](https://img.shields.io/github/stars/ymcui/Chinese-LLaMA-Alpaca.svg?style=social&label=Star) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |      |
|   TigerBot-7b-base   |  7B  | 2023-06 | 多语 | 通用 | [ckpt](https://huggingface.co/TigerResearch/tigerbot-7b-base) | [TigerBot](https://github.com/TigerResearch/TigerBot)![Star](https://img.shields.io/github/stars/TigerResearch/TigerBot.svg?style=social&label=Star) |         [虎博科技](https://github.com/TigerResearch)         |  CD  |                                                              |      |
|  Panda-OpenLLaMA-7B  |  7B  | 2023-05 | 中英 | 通用 | [ckpt](https://huggingface.co/chitanda/panda-7b-open-llama-preview-300pt) | [pandallm](https://github.com/dandelionsllm/pandallm)![Star](https://img.shields.io/github/stars/dandelionsllm/pandallm.svg?style=social&label=Star) |      [dandelionsllm](https://github.com/dandelionsllm)       |  CD  |                                                              |      |
|      Panda-13B       | 13B  | 2023-05 | 中英 | 通用 | [ckpt](https://huggingface.co/chitanda/llama-panda-zh-13b-delta) | [pandallm](https://github.com/dandelionsllm/pandallm)![Star](https://img.shields.io/github/stars/dandelionsllm/pandallm.svg?style=social&label=Star) |      [dandelionsllm](https://github.com/dandelionsllm)       |  CD  |                                                              |      |
|       Panda-7B       |  7B  | 2023-05 | 中英 | 通用 | [ckpt](https://huggingface.co/chitanda/llama-panda-zh-7b-delta) | [pandallm](https://github.com/dandelionsllm/pandallm)![Star](https://img.shields.io/github/stars/dandelionsllm/pandallm.svg?style=social&label=Star) |      [dandelionsllm](https://github.com/dandelionsllm)       |  CD  |                                                              |      |
|    OpenLLaMA-13B     | 13B  | 2023-05 | 中英 | 通用 |    [ckpt](https://huggingface.co/Linly-AI/OpenLLaMA-13B)     | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) |    [深圳大学计算机视觉研究所](https://github.com/CVI-SZU)    |  CD  |                                                              |      |
|      LaWGPT-7B       |  7B  | 2023-05 | 中英 | 法律 |    [ckpt](https://huggingface.co/entity303/legal-lora-7b)    | [LawGPT](https://github.com/pengxiao-song/LaWGPT)![Star](https://img.shields.io/github/stars/pengxiao-song/LaWGPT.svg?style=social&label=Star) |      [Pengxiao Song](https://github.com/pengxiao-song)       |  CD  |                                                              |      |
|     BiLLa-7B-LLM     |  7B  | 2023-05 | 中英 | 通用 |    [ckpt](https://huggingface.co/Neutralzz/BiLLa-7B-LLM)     | [BiLLa](https://github.com/Neutralzz/BiLLa)![Star](https://img.shields.io/github/stars/Neutralzz/BiLLa.svg?style=social&label=Star) |          [Zhongli Li](https://github.com/Neutralzz)          |  CD  |                                                              |      |
| Ziya-LLaMA-7B-Reward |  7B  | 2023-05 | 中英 | 通用 | [ckpt](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-7B-Reward) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM)![Star](https://img.shields.io/github/stars/IDEA-CCNL/Fengshenbang-LM.svg?style=social&label=Star) |          [IDEA研究院](https://github.com/IDEA-CCNL)          |  CD  |                                                              |      |
|        YuYan         | 11B  | 2023-04 | 中文 | 通用 |        [ckpt](https://huggingface.co/FUXI/yuyan-11b)         |                              /                               |           [网易伏羲](https://huggingface.co/FUXI)            |  CD  |   [Paper](https://aclanthology.org/2022.naacl-industry.8/)   |      |
|  Chinese-LLaMA-33B   | 33B  | 2023-04 | 中文 | 通用 | [ckpt](https://huggingface.co/P01son/Linly-Chinese-LLaMA-33b-hf) | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) |    [深圳大学计算机视觉研究所](https://github.com/CVI-SZU)    |  CD  |        [Blog](https://zhuanlan.zhihu.com/p/616748134)        |      |
|  Chinese-LLaMA-13B   | 13B  | 2023-04 | 中文 | 通用 |  [ckpt](https://huggingface.co/Linly-AI/Chinese-LLaMA-13B)   | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) |    [深圳大学计算机视觉研究所](https://github.com/CVI-SZU)    |  CD  |        [Blog](https://zhuanlan.zhihu.com/p/616748134)        |      |
|   Chinese-LLaMA-7B   |  7B  | 2023-04 | 中文 | 通用 |  [ckpt](https://huggingface.co/Linly-AI/Chinese-LLaMA-7B/)   | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) |    [深圳大学计算机视觉研究所](https://github.com/CVI-SZU)    |  CD  |        [Blog](https://zhuanlan.zhihu.com/p/616748134)        |      |
|   OpenChineseLLaMA   |  7B  | 2023-04 | 中英 | 通用 | [ckpt](https://huggingface.co/openlmlab/open-chinese-llama-7b-patch) | [OpenChineseLLaMA](https://github.com/OpenLMLab/OpenChineseLLaMA)![Star](https://img.shields.io/github/stars/OpenLMLab/OpenChineseLLaMA.svg?style=social&label=Star) |          [OpenLMLab](https://github.com/OpenLMLab)           |  CD  |                                                              |      |
|       MOSS-003       | 16B  | 2023-04 | 中英 | 通用 |    [ckpt](https://huggingface.co/fnlp/moss-moon-003-base)    | [MOSS](https://github.com/OpenLMLab/MOSS)![Star](https://img.shields.io/github/stars/OpenLMLab/MOSS.svg?style=social&label=Star) |           [复旦大学](https://github.com/OpenLMLab)           |  CD  |                                                              |      |
|    BBT-2-13B-Text    | 13B  | 2023-04 | 中文 | 通用 |       [申请下载](https://bbt.ssymmetry.com/model.html)       | [BBT-FinCUGE-Applications](https://github.com/ssymmetry/BBT-FinCUGE-Applications)![Star](https://img.shields.io/github/stars/ssymmetry/BBT-FinCUGE-Applications.svg?style=social&label=Star) |        [超对称](https://bbt.ssymmetry.com/model.html)        |  CD  |        [Paper](https://bbt.ssymmetry.com/thesis.html)        |      |
|    BBT-2-12B-Text    | 12B  | 2023-04 | 中文 | 通用 |       [申请下载](https://bbt.ssymmetry.com/model.html)       | [BBT-FinCUGE-Applications](https://github.com/ssymmetry/BBT-FinCUGE-Applications)![Star](https://img.shields.io/github/stars/ssymmetry/BBT-FinCUGE-Applications.svg?style=social&label=Star) |        [超对称](https://bbt.ssymmetry.com/model.html)        |  CD  |        [Paper](https://bbt.ssymmetry.com/thesis.html)        |      |
|  Chinese-LLaMA-13B   | 13B  | 2023-04 | 中英 | 通用 | [ckpt](https://huggingface.co/ziqingyang/chinese-llama-lora-13b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)![Star](https://img.shields.io/github/stars/ymcui/Chinese-LLaMA-Alpaca.svg?style=social&label=Star) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |      |
|       flan-ul2       | 20B  | 2023-03 | 多语 | 通用 |   [ckpt](https://huggingface.co/google/flan-ul2/tree/main)   | [ul2](https://github.com/google-research/google-research/tree/master/ul2) |            [Google](https://ai.google/research/)             |  ED  |       [Paper](https://arxiv.org/pdf/2205.05131v3.pdf)        |      |
|       CPM-Bee        | 10B  | 2023-01 | 中英 | 通用 | [ckpt-10B](https://huggingface.co/openbmb/cpm-bee-10b) [ckpt-5B](https://huggingface.co/openbmb/cpm-bee-5b) | [CPM-Bee](https://github.com/OpenBMB/CPM-Bee)![Star](https://img.shields.io/github/stars/OpenBMB/CPM-Bee.svg?style=social&label=Star) |             [OpenBMB](https://live.openbmb.org/)             |  CD  |                                                              |      |
|        BLOOM         | 176B | 2022-11 | 多语 | 通用 |    [ckpt-95000](https://huggingface.co/bigscience/bloom)     | [Megatron-DeepSpeed](https://github.com/bigscience-workshop/Megatron-DeepSpeed) |     [BigScience](https://github.com/bigscience-workshop)     |  CD  |        [Paper](https://arxiv.org/pdf/2211.05100.pdf)         |      |
|       *BLOOMZ*       | 176B | 2022-11 | 多语 | 通用 |     [ckpt-498](https://huggingface.co/bigscience/bloomz)     | [Megatron-DeepSpeed](https://github.com/bigscience-workshop/Megatron-DeepSpeed) |     [BigScience](https://github.com/bigscience-workshop)     |  CD  |            [Paper](https://arxiv.org/abs/2211.01)            |      |
|     flan-t5-xxl      | 11B  | 2022-11 | 多语 | 通用 |      [ckpt](https://huggingface.co/google/flan-t5-xxl)       |        [t5x](https://github.com/google-research/t5x)         |            [Google](https://ai.google/research/)             |  ED  |        [paper](https://arxiv.org/pdf/2210.11416.pdf)         |      |
|       CPM-Ant+       | 10B  | 2022-10 | 中英 | 通用 | [ckpt](http://openbmb.oss-cn-hongkong.aliyuncs.com/model_center/cpm-ant-plus-10b/cpm-ant-plus-10b.zip) |       [CPM-Live](https://github.com/OpenBMB/CPM-Live)        |             [OpenBMB](https://live.openbmb.org/)             |  CD  | [blog](https://www.openbmb.org/community/blogs/blogpage?id=98afef2ce45f4fe9a4bc15a66d7ccb92) |      |
|         GLM          | 130B | 2022-10 | 中英 | 通用 | [申请下载](https://docs.google.com/forms/d/e/1FAIpQLSehr5Dh_i3TwACmFFi8QEgIVNYGmSPwV0GueIcsUev0NEfUug/viewform) | [GLM-130B](https://github.com/THUDM/GLM-130B)![Star](https://img.shields.io/github/stars/THUDM/GLM-130B.svg?style=social&label=Star) |             [清华大学](https://github.com/THUDM)             |  ND  |           [paper](http://arxiv.org/abs/2210.02414)           |      |
|       CPM-Ant        | 10B  | 2022-09 | 中文 | 通用 | [ckpt](https://openbmb.oss-cn-hongkong.aliyuncs.com/model_center/cpmlive-10b/cpm_live_10B.zip) |       [CPM-Live](https://github.com/OpenBMB/CPM-Live)        |             [OpenBMB](https://live.openbmb.org/)             |  CD  | [blog](https://www.openbmb.org/community/blogs/blogpage?id=98afef2ce45f4fe9a4bc15a66d7ccb92) |      |
|         GLM          | 10B  | 2022-09 | 中文 | 通用 | [ckpt](https://lfs.aminer.cn/misc/cogview/glm-10b-chinese.zip) |             [GLM](https://github.com/THUDM/GLM)              |             [清华大学](https://github.com/THUDM)             |  ND  |          [paper](https://arxiv.org/abs/2103.10360)           |      |
|       CodeGeeX       | 13B  | 2022-06 | 多语 | 代码 | [申请下载](https://models.aminer.cn/codegeex/download/request) |        [CodeGeeX](https://github.com/THUDM/CodeGeeX)         |             [清华大学](https://github.com/THUDM)             |  CD  |       [blog](https://models.aminer.cn/codegeex/blog/)        |      |
|        源1.0         | 245B | 2021-09 | 中文 | 通用 |            [API申请](https://air.inspur.com/home)            |     [Yian-1.0](https://github.com/Shawn-Inspur/Yuan-1.0)     |             [浪潮](https://air.inspur.com/home)              |  CD  |          [paper](https://arxiv.org/abs/2110.04725)           |      |
|        CPM-2         | 11B  | 2021-06 | 中文 | 通用 | [申请下载](https://resource.wudao.baai.ac.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [CPM](https://github.com/TsinghuaAI/CPM)![Star](https://img.shields.io/github/stars/TsinghuaAI/CPM.svg?style=social&label=Star) |            [智源研究院](https://www.baai.ac.cn/)             |  ED  |          [paper](https://arxiv.org/abs/2106.10715)           |      |
|        CPM-2         | 10B  | 2021-06 | 中英 | 通用 | [申请下载](https://resource.wudao.baai.ac.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [CPM](https://github.com/TsinghuaAI/CPM)![Star](https://img.shields.io/github/stars/TsinghuaAI/CPM.svg?style=social&label=Star) |            [智源研究院](https://www.baai.ac.cn/)             |  ED  |          [paper](https://arxiv.org/abs/2106.10715)           |      |
|        CPM-2         | 200B | 2021-06 | 中英 | 通用 | [申请下载](https://resource.wudao.baai.ac.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [CPM](https://github.com/TsinghuaAI/CPM)![Star](https://img.shields.io/github/stars/TsinghuaAI/CPM.svg?style=social&label=Star) |            [智源研究院](https://www.baai.ac.cn/)             |  ED  |          [paper](https://arxiv.org/abs/2106.10715)           |      |
|     PanGu-Alpha      | 13B  | 2021-05 | 中文 | 通用 | [ckpt](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha) | [PanGu-Alpha](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha) | [鹏城实验室](https://openi.pcl.ac.cn/PCL-Platform.Intelligence) |  CD  |        [paper](https://arxiv.org/pdf/2104.12369.pdf)         |      |
|     PanGu-Alpha      | 200B | 2021-05 | 中文 | 通用 |                            待发布                            | [PanGu-Alpha](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha) | [鹏城实验室](https://openi.pcl.ac.cn/PCL-Platform.Intelligence) |  CD  |        [paper](https://arxiv.org/pdf/2104.12369.pdf)         |      |
|         PLUG         | 27B  | 2021-04 | 中文 | 通用 |       [申请下载](https://www.alice-mind.com/portal#/)        |      [AliceMind](https://github.com/alibaba/AliceMind)       |       [阿里巴巴](https://www.alice-mind.com/portal#/)        |  ED  |                                                              |      |
|        GPT-3         | 13B  | 2021-04 | 中文 | 通用 |                            待发布                            | [GPT-3](https://modelscope.cn/models/damo/nlp_gpt3_text-generation_13B/summary) |      [达摩院](https://modelscope.cn/organization/damo)       |  CD  |                                                              |      |
|        GPT-3         | 30B  | 2021-04 | 中文 | 通用 |                            待发布                            | [GPT-3](https://modelscope.cn/models/damo/nlp_gpt3_text-generation_30B/summary) |      [达摩院](https://modelscope.cn/organization/damo)       |  CD  |                                                              |      |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## ChatLLM

> 具备问答和对话等功能的大型语言模型。
>
> ND:  Non-Causal Decoder or Prefix LM
> CD:  Causal Decoder
> ED:  Encoder-Decoder

|           模型           |  大小   | 时间    | 语言 |     领域     |                             下载                             |                           项目地址                           |                       机构/个人                        |      结构      |                             文献                             |
| :----------------------: | :-----: | ------- | :--: | :----------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------: | :------------: | :----------------------------------------------------------: |
| CoLLaMA | 7B | 2023-06 | 中英 | 代码 | [ckpt](https://huggingface.co/DaliahX/CoLLaMA-7b) | [CoLLaMA](https://github.com/Denilah/CoLLaMA)![Star](https://img.shields.io/github/stars/Denilah/CoLLaMA.svg?style=social&label=Star) | [Denilah](https://github.com/Denilah) | CD |  |
| ChatGLM2-6B |  6B  | 2023-06 | 中英 | 通用 | [ckpt](https://huggingface.co/THUDM/chatglm2-6b) | [ChatGLM2-6B](https://github.com/THUDM/ChatGLM2-6B)![Star](https://img.shields.io/github/stars/THUDM/ChatGLM2-6B.svg?style=social&label=Star) | [清华大学](https://github.com/THUDM) | ND |      |
|         TechGPT          |   7B    | 2023-06 | 中英 |     教育     |       [ckpt](https://huggingface.co/neukg/TechGPT-7B)        | [TechGPT](https://github.com/neukg/TechGPT)![Star](https://img.shields.io/github/stars/neukg/TechGPT.svg?style=social&label=Star) |          [东北大学](https://github.com/neukg)          |    CD    |                                                              |
|           Yayi           |   7B    | 2023-06 | 中英 | 安全、舆情等 |    [ckpt](https://huggingface.co/wenge-research/yayi-7b)     | [Yayi](https://github.com/wenge-research/YaYi)![Star](https://img.shields.io/github/stars/wenge-research/YaYi.svg?style=social&label=Star) |     [中科闻歌](https://github.com/wenge-research)      |    CD   |                                                              |
|       BayLing-13B        |   13B   | 2023-06 | 中英 |     通用     |    [ckpt](https://huggingface.co/ICTNLP/bayling-13b-diff)    | [BayLing](https://github.com/ictnlp/BayLing)![Star](https://img.shields.io/github/stars/ictnlp/BayLing.svg?style=social&label=Star) |        [中国科学院](https://github.com/ictnlp)         |    CD   |                                                              |
|        BayLing-7B        |   7B    | 2023-06 | 中英 |     通用     |    [ckpt](https://huggingface.co/ICTNLP/bayling-7b-diff)     | [BayLing](https://github.com/ictnlp/BayLing)![Star](https://img.shields.io/github/stars/ictnlp/BayLing.svg?style=social&label=Star) |        [中国科学院](https://github.com/ictnlp)         |    CD   |                                                              |
|          MeChat          |   6B    | 2023-06 | 中文 |     医学     |      [ckpt](https://huggingface.co/qiuhuachuan/MeChat)       | [smile](https://github.com/qiuhuachuan/smile)![Star](https://img.shields.io/github/stars/qiuhuachuan/smile.svg?style=social&label=Star) |     [qiuhuachuan](https://github.com/qiuhuachuan)      | ND |                                                              |
|     ziya-13b-medical     |   13b   | 2023-06 | 中英 |     医学     | [ckpt](https://huggingface.co/shibing624/ziya-llama-13b-medical-lora) | [MedicalGPT](https://github.com/shibing624/MedicalGPT)![Star](https://img.shields.io/github/stars/shibing624/MedicalGPT.svg?style=social&label=Star) |        [Ming Xu](https://github.com/shibing624)        |    CD   |                                                              |
|      ZhiXi-13B-Diff      |   13B   | 2023-06 | 中英 |     通用     |     [ckpt](https://huggingface.co/zjunlp/zhixi-13b-diff)     | [KnowLLM](https://github.com/zjunlp/KnowLM)![Star](https://img.shields.io/github/stars/zjunlp/KnowLM.svg?style=social&label=Star) |         [浙江大学](https://github.com/zjunlp)          |    CD   |                                                              |
|          Anima           |   33B   | 2023-06 | 中文 |     通用     |       [ckpt](https://huggingface.co/lyogavin/Anima33B)       | [Anima](https://github.com/lyogavin/Anima)![Star](https://img.shields.io/github/stars/lyogavin/Anima.svg?style=social&label=Star) |        [Gavin Li](https://github.com/lyogavin)         |    CD   |                                                              |
|  OpenLLaMA-Chinese-13B   |   13B   | 2023-06 | 中文 |     通用     | [ckpt](https://huggingface.co/FittenTech/openllama-chinese-13b) | [OpenLLaMA-Chinese](https://github.com/FittenTech/OpenLLaMA-Chinese)![Star](https://img.shields.io/github/stars/FittenTech/OpenLLaMA-Chinese.svg?style=social&label=Star) |      [FittenTech](https://github.com/FittenTech)       |    CD   |                                                              |
|   OpenLLaMA-Chinese-3B   |   3B    | 2023-06 | 中文 |     通用     | [ckpt](https://huggingface.co/FittenTech/openllama-chinese-3b) | [OpenLLaMA-Chinese](https://github.com/FittenTech/OpenLLaMA-Chinese)![Star](https://img.shields.io/github/stars/FittenTech/OpenLLaMA-Chinese.svg?style=social&label=Star) |      [FittenTech](https://github.com/FittenTech)       |    CD   |                                                              |
|   OpenLLaMA-Chinese-7B   |   7B    | 2023-06 | 中文 |     通用     | [ckpt](https://huggingface.co/FittenTech/openllama-chinese-7b) | [OpenLLaMA-Chinese](https://github.com/FittenTech/OpenLLaMA-Chinese)![Star](https://img.shields.io/github/stars/FittenTech/OpenLLaMA-Chinese.svg?style=social&label=Star) |      [FittenTech](https://github.com/FittenTech)       |    CD   |                                                              |
|          Taoli           |   7B    | 2023-06 | 中英 |     教育     |                          [待开源]()                          | [taoli](https://github.com/blcuicall/taoli)![Star](https://img.shields.io/github/stars/blcuicall/taoli.svg?style=social&label=Star) |      [北京语言大学](https://github.com/blcuicall)      |    CD   |                                                              |
|       Lawyer-llama       |   13B   | 2023-06 | 中英 |     法律     | [ckpt](https://huggingface.co/pkupie/lawyer-llama-13b-beta1.0) | [lawyer-llama](https://github.com/AndrewZhe/lawyer-llama)![Star](https://img.shields.io/github/stars/AndrewZhe/lawyer-llama.svg?style=social&label=Star) |      [Quzhe Huang](https://github.com/AndrewZhe)       |    CD   |                                                              |
|     QiZhen-CaMA-13B      |   13B   | 2023-06 | 中英 |     医学     | [ckpt-3600](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) [ckpt-6000](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) | [QiZhenGPT](https://github.com/CMKRG/QiZhenGPT)![Star](https://img.shields.io/github/stars/CMKRG/QiZhenGPT.svg?style=social&label=Star) |          [浙江大学](https://github.com/CMKRG)          |    CD   |                                                              |
|         扁鹊-2.0         |   6B    | 2023-06 | 中文 |     医学     |       [ckpt](https://huggingface.co/scutcyr/BianQue-2)       | [BianQue](https://github.com/scutcyr/BianQue)![Star](https://img.shields.io/github/stars/scutcyr/BianQue.svg?style=social&label=Star) |       [华南理工大学](https://github.com/scutcyr)       | ND |                                                              |
|         SoulChat         |   6B    | 2023-06 | 中文 |     心理     |       [ckpt](https://huggingface.co/scutcyr/SoulChat)        | [SoulChat](https://github.com/scutcyr/SoulChat)![Star](https://img.shields.io/github/stars/scutcyr/SoulChat.svg?style=social&label=Star) |       [华南理工大学](https://github.com/scutcyr)       | ND |                                                              |
| openbuddy-falcon-7b-v1.5 |   7B    | 2023-06 | 多语 |     通用     | [ckpt](https://huggingface.co/OpenBuddy/openbuddy-falcon-7b-v1.5-fp16) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy)![Star](https://img.shields.io/github/stars/OpenBuddy/OpenBuddy.svg?style=social&label=Star) |       [OpenBuddy](https://github.com/OpenBuddy)        |    CD   |                                                              |
|     AtomGPT_8k_chat      |   13B   | 2023-06 | 中英 |     通用     |  [ckpt](https://huggingface.co/AtomEchoAI/AtomGPT_8k_chat)   | [AtomGPT](https://github.com/AtomEcho/AtomGPT)![Star](https://img.shields.io/github/stars/AtomEcho/AtomGPT.svg?style=social&label=Star) |        [原子回声](https://github.com/AtomEcho)         |    CD   |                                                              |
|      AquilaChat-7B       |   7B    | 2023-06 | 中英 |     通用     |     [ckpt](https://model.baai.ac.cn/model-detail/100101)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)![Star](https://img.shields.io/github/stars/FlagAI-Open/FlagAI.svg?style=social&label=Star) |       [智源研究院](https://huggingface.co/BAAI)        |    CD   |                                                              |
|      YuLan-Chat-65B      |   65B   | 2023-06 | 中英 |     通用     | [lora-ckpt](https://huggingface.co/RUCAIBox/YuLan-Chat-65b-delta) | [YuLan-Chat](https://github.com/RUC-GSAI/YuLan-Chat)![Star](https://img.shields.io/github/stars/RUC-GSAI/YuLan-Chat.svg?style=social&label=Star) |      [中国人民大学](https://github.com/RUC-GSAI)       |    CD   |                                                              |
|      YuLan-Chat-13B      |   13B   | 2023-06 | 中英 |     通用     | [lora-ckpt](https://huggingface.co/RUCAIBox/YuLan-Chat-13b-delta) | [YuLan-Chat](https://github.com/RUC-GSAI/YuLan-Chat)![Star](https://img.shields.io/github/stars/RUC-GSAI/YuLan-Chat.svg?style=social&label=Star) |      [中国人民大学](https://github.com/RUC-GSAI)       |    CD   |                                                              |
|    Chinese-Alpaca-33B    |   33B   | 2023-06 | 中文 |     通用     | [lora-ckpt](https://huggingface.co/ziqingyang/chinese-alpaca-lora-33b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)![Star](https://img.shields.io/github/stars/ymcui/Chinese-LLaMA-Alpaca.svg?style=social&label=Star) |         [Yiming Cui](https://github.com/ymcui)         |    CD   |                                                              |
|       TigerBot-sft       |  180B   | 2023-06 | 多语 |     通用     | [ckpt](https://huggingface.co/TigerResearch/tigerbot-180b-research) | [TigerBot](https://github.com/TigerResearch/TigerBot)![Star](https://img.shields.io/github/stars/TigerResearch/TigerBot.svg?style=social&label=Star) |      [虎博科技](https://github.com/TigerResearch)      |    CD   |                                                              |
|       TigerBot-sft       |   7B    | 2023-06 | 多语 |     通用     | [ckpt](https://huggingface.co/TigerResearch/tigerbot-7b-sft) | [TigerBot](https://github.com/TigerResearch/TigerBot)![Star](https://img.shields.io/github/stars/TigerResearch/TigerBot.svg?style=social&label=Star) |      [虎博科技](https://github.com/TigerResearch)      |    CD   |                                                              |
|       ChatYuan-7B        |   7B    | 2023-06 | 中英 |     通用     |   [ckpt](https://huggingface.co/tiansz/ChatYuan-7B-merge)    |    [ChatYuan-7B](https://github.com/clue-ai/ChatYuan-7B)     |          [ClueAI](https://github.com/clue-ai)          |    CD   |                                                              |
|    Panda-Instruct-13B    |   13B   | 2023-05 | 中英 |     通用     | [ckpt](https://huggingface.co/chitanda/llama-panda-zh-13b-coig-delta) | [pandallm](https://github.com/dandelionsllm/pandallm)![Star](https://img.shields.io/github/stars/dandelionsllm/pandallm.svg?style=social&label=Star) |   [dandelionsllm](https://github.com/dandelionsllm)    |    CD   |                                                              |
|    Panda-Instruct-7B     |   7B    | 2023-05 | 中英 |     通用     | [ckpt](https://huggingface.co/chitanda/llama-panda-zh-coig-7b-delta) | [pandallm](https://github.com/dandelionsllm/pandallm)![Star](https://img.shields.io/github/stars/dandelionsllm/pandallm.svg?style=social&label=Star) |   [dandelionsllm](https://github.com/dandelionsllm)    |    CD   |                                                              |
|       BiLLa-7B-SFT       |   7B    | 2023-05 | 中英 |     通用     |    [ckpt](https://huggingface.co/Neutralzz/BiLLa-7B-SFT)     | [BiLLa](https://github.com/Neutralzz/BiLLa)![Star](https://img.shields.io/github/stars/Neutralzz/BiLLa.svg?style=social&label=Star) |       [Zhongli Li](https://github.com/Neutralzz)       |    CD   |                                                              |
|    QiZhen-ChatGLM-6B     |   6B    | 2023-05 | 中英 |     医学     | [ckpt-2500](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) | [QiZhenGPT](https://github.com/CMKRG/QiZhenGPT)![Star](https://img.shields.io/github/stars/CMKRG/QiZhenGPT.svg?style=social&label=Star) |          [浙江大学](https://github.com/CMKRG)          |    CD   |                                                              |
| QiZhen-Chinese-LLaMA-7B  |   7B    | 2023-05 | 中英 |     医学     | [ckpt-3500](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) [ckpt-6000](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) | [QiZhenGPT](https://github.com/CMKRG/QiZhenGPT)![Star](https://img.shields.io/github/stars/CMKRG/QiZhenGPT.svg?style=social&label=Star) |          [浙江大学](https://github.com/CMKRG)          |    CD   |                                                              |
|     ChatMed-Consult      |   7B    | 2023-05 | 中英 |     医学     |  [ckpt](https://huggingface.co/michaelwzhu/ChatMed-Consult)  | [ChatMed](https://github.com/michael-wzhu/ChatMed)![Star](https://img.shields.io/github/stars/michael-wzhu/ChatMed.svg?style=social&label=Star) |    [michael-wzhu](https://github.com/michael-wzhu)     |    CD   |                                                              |
|    LaWGPT-7B-beta1.1     |   7B    | 2023-05 | 中英 |     法律     |  [ckpt](https://huggingface.co/entity303/lawgpt-lora-7b-v2)  | [LawGPT](https://github.com/pengxiao-song/LaWGPT)![Star](https://img.shields.io/github/stars/pengxiao-song/LaWGPT.svg?style=social&label=Star) |   [Pengxiao Song](https://github.com/pengxiao-song)    |    CD   |                                                              |
|    LaWGPT-7B-beta1.0     |   7B    | 2023-05 | 中英 |     法律     | [ckpt](https://huggingface.co/entity303/lawgpt-legal-lora-7b) | [LawGPT](https://github.com/pengxiao-song/LaWGPT)![Star](https://img.shields.io/github/stars/pengxiao-song/LaWGPT.svg?style=social&label=Star) |   [Pengxiao Song](https://github.com/pengxiao-song)    |    CD   |                                                              |
|        Cornucopia        |   7B    | 2023-05 | 中英 |     金融     | [ckpt-linly-llama](https://huggingface.co/yuyangmu125/lora-llama-fin-Linly-zh) | [Cornucopia-LLaMA-Fin-Chinese](https://github.com/jerry1993-tech/Cornucopia-LLaMA-Fin-Chinese)![Star](https://img.shields.io/github/stars/jerry1993-tech/Cornucopia-LLaMA-Fin-Chinese.svg?style=social&label=Star) |     [yuyangmu](https://github.com/jerry1993-tech)      |    CD   |                                                              |
|        Cornucopia        |   7B    | 2023-05 | 中英 |     金融     | [ckpt-ori-fb](https://huggingface.co/yuyangmu125/lora-llama-fin-ori-fb) | [Cornucopia-LLaMA-Fin-Chinese](https://github.com/jerry1993-tech/Cornucopia-LLaMA-Fin-Chinese)![Star](https://img.shields.io/github/stars/jerry1993-tech/Cornucopia-LLaMA-Fin-Chinese.svg?style=social&label=Star) |     [yuyangmu](https://github.com/jerry1993-tech)      |    CD   |                                                              |
|        HuatuoGPT         |   7B    | 2023-05 | 中文 |     医学     | [ckpt](https://huggingface.co/FreedomIntelligence/HuatuoGPT-v1) | [HuatuoGPT](https://github.com/FreedomIntelligence/HuatuoGPT) | [香港中文大学](https://github.com/FreedomIntelligence) |    CD   |        [Paper](https://arxiv.org/pdf/2305.15075.pdf)         |
|         LexiLaw          |   6B    | 2023-05 | 中文 |     法律     |         [ckpt](https://github.com/CSHaitao/LexiLaw)          |        [LexiLaw](https://github.com/CSHaitao/LexiLaw)        |        [Haitao Li](https://github.com/CSHaitao)        |    ND    |          [Paper](https://arxiv.org/abs/2305.12002)           |
|         XuanYuan         |  176B   | 2023-05 | 中文 |     金融     |    [申请下载](https://huggingface.co/xyz-nlp/XuanYuan2.0)    | [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan)![Star](https://img.shields.io/github/stars/Duxiaoman-DI/XuanYuan.svg?style=social&label=Star) |       [度小满](https://github.com/Duxiaoman-DI)        |    CD   |          [Paper](https://arxiv.org/abs/2305.12002)           |
|    Ziya-LLaMA-13B-v1     |   13B   | 2023-05 | 中英 |     通用     |  [ckpt](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1)  | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM)![Star](https://img.shields.io/github/stars/IDEA-CCNL/Fengshenbang-LM.svg?style=social&label=Star) |       [IDEA研究院](https://github.com/IDEA-CCNL)       |    CD   |  [Blog](https://mp.weixin.qq.com/s/IeXgq8blGoeVbpIlAUCAjA)   |
|      BLOOMChat V1.0      |  176B   | 2023-05 | 多语 |     通用     | [ckpt](https://huggingface.co/sambanovasystems/BLOOMChat-176B-v1) |     [bloomchat](https://github.com/sambanova/bloomchat)      |       [SambaNova Systems](https://sambanova.ai/)       |    CD   | [Blog](https://sambanova.ai/blog/introducing-bloomchat-176b-the-multilingual-chat-based-llm/) |
|          BiLLa           |   7B    | 2023-05 | 中英 |     通用     |          [ckpt](https://github.com/Neutralzz/BiLLa)          | [BiLLa](https://github.com/Neutralzz/BiLLa)![Star](https://img.shields.io/github/stars/Neutralzz/BiLLa.svg?style=social&label=Star) |       [Zhongli Li](https://github.com/Neutralzz)       |    CD   |                                                              |
|        Bactrian-X        |   13B   | 2023-05 | 多语 |     通用     | [lora-ckpt](https://huggingface.co/MBZUAI/bactrian-x-13b-lora) | [bactrian-x](https://github.com/mbzuai-nlp/bactrian-x)![Star](https://img.shields.io/github/stars/mbzuai-nlp/bactrian-x.svg?style=social&label=Star) |        [MBZUAI](https://github.com/mbzuai-nlp)         |    CD   |                                                              |
|        Bactrian-X        |   7B    | 2023-05 | 多语 |     通用     | [lora-ckpt](https://huggingface.co/MBZUAI/bactrian-x-llama-7b-lora) | [bactrian-x](https://github.com/mbzuai-nlp/bactrian-x)![Star](https://img.shields.io/github/stars/mbzuai-nlp/bactrian-x.svg?style=social&label=Star) |        [MBZUAI](https://github.com/mbzuai-nlp)         |    CD   |                                                              |
|       Bactrian-ZH        |   7B    | 2023-05 | 中文 |     通用     |        [lora-ckpt](https://huggingface.co/haonan-li)         | [bactrian-x](https://github.com/mbzuai-nlp/bactrian-x)![Star](https://img.shields.io/github/stars/mbzuai-nlp/bactrian-x.svg?style=social&label=Star) |        [MBZUAI](https://github.com/mbzuai-nlp)         |    CD   |                                                              |
|          LawGPT          |   6B    | 2023-05 | 中文 |     法律     |      [lora-ckpt](https://github.com/LiuHC0428/LAW-GPT)       | [LAW-GPT](https://github.com/LiuHC0428/LAW-GPT)![Star](https://img.shields.io/github/stars/LiuHC0428/LAW-GPT.svg?style=social&label=Star) |      [hongchengliu](https://github.com/LiuHC0428)      | ND |                                                              |
|       ChatFlow-13B       |   13B   | 2023-05 | 中英 |     通用     |     [ckpt](https://huggingface.co/Linly-AI/ChatFlow-13B)     | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) | [深圳大学计算机视觉研究所](https://github.com/CVI-SZU) |    CD   |                                                              |
|       ChatFlow-7B        |   7B    | 2023-05 | 中英 |     通用     |     [ckpt](https://huggingface.co/Linly-AI/ChatFlow-7B)      | [Linly](https://github.com/CVI-SZU/Linly)![Star](https://img.shields.io/github/stars/CVI-SZU/Linly.svg?style=social&label=Star) | [深圳大学计算机视觉研究所](https://github.com/CVI-SZU) |    CD   |                                                              |
|        OpenBuddy         |   7B    | 2023-05 | 多语 |     通用     | [ckpt](https://github.com/OpenBuddy/OpenBuddy/blob/main/models.md) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy)![Star](https://img.shields.io/github/stars/OpenBuddy/OpenBuddy.svg?style=social&label=Star) |       [OpenBuddy](https://github.com/OpenBuddy)        |    CD   |                                                              |
|        OpenBuddy         |   13B   | 2023-05 | 多语 |     通用     | [ckpt](https://huggingface.co/OpenBuddy/openbuddy-13b-v1.3-fp16) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy)![Star](https://img.shields.io/github/stars/OpenBuddy/OpenBuddy.svg?style=social&label=Star) |       [OpenBuddy](https://github.com/OpenBuddy)        |    CD   |                                                              |
|      YuYan-dialogue      |   11B   | 2023-04 | 中文 |     通用     | [ckpt](https://huggingface.co/FUXI/yuyan-dialogue/tree/main) |                              /                               |        [网易伏羲](https://huggingface.co/FUXI)         |    CD   |   [paper](https://aclanthology.org/2022.naacl-industry.8/)   |
|         扁鹊-1.0         |  0.7B   | 2023-04 | 中文 |     医学     |      [ckpt](https://huggingface.co/scutcyr/BianQue-1.0)      |        [BianQue](https://github.com/scutcyr/BianQue)         |         [scutcyr](https://github.com/scutcyr)          | ED |                                                              |
| Moss-moon-003-sft-plugin |   16B   | 2023-04 | 中英 |     通用     | [ckpt](https://huggingface.co/fnlp/moss-moon-003-sft-plugin) | [MOSS](https://github.com/OpenLMLab/MOSS)![Star](https://img.shields.io/github/stars/OpenLMLab/MOSS.svg?style=social&label=Star) |        [复旦大学](https://github.com/OpenLMLab)        |    CD   |                                                              |
|    moss-moon-003-sft     |   16B   | 2023-04 | 中英 |     通用     |    [ckpt](https://huggingface.co/fnlp/moss-moon-003-sft)     | [MOSS](https://github.com/OpenLMLab/MOSS)![Star](https://img.shields.io/github/stars/OpenLMLab/MOSS.svg?style=social&label=Star) |        [复旦大学](https://github.com/OpenLMLab)        |    CD   |                                                              |
|       RWKV-4-Raven       | 3/7/14B | 2023-04 | 中英 |     通用     | [ckpt](https://huggingface.co/BlinkDL/rwkv-4-raven/tree/main) | [ChatRWKV](https://github.com/BlinkDL/ChatRWKV)![Star](https://img.shields.io/github/stars/BlinkDL/ChatRWKV.svg?style=social&label=Star) |         [BlinkDL](https://github.com/BlinkDL)          |      RNN       |        [Blog](https://zhuanlan.zhihu.com/p/618011122)        |
|   Phoenix-inst-chat-7b   |   7B    | 2023-04 | 中文 |     通用     | [ckpt](https://huggingface.co/FreedomIntelligence/phoenix-inst-chat-7b) | [LLMZoo](https://github.com/FreedomIntelligence/LLMZoo)![Star](https://img.shields.io/github/stars/FreedomIntelligence/LLMZoo.svg?style=social&label=Star) | [香港中文大学](https://github.com/FreedomIntelligence) |    CD   |                                                              |
|     Phoenix-chat-7b      |   7B    | 2023-04 | 中文 |     通用     | [ckpt](https://huggingface.co/FreedomIntelligence/phoenix-chat-7b) | [LLMZoo](https://github.com/FreedomIntelligence/LLMZoo)![Star](https://img.shields.io/github/stars/FreedomIntelligence/LLMZoo.svg?style=social&label=Star) | [香港中文大学](https://github.com/FreedomIntelligence) |    CD   |                                                              |
|         ChatPLUG         |  3.7B   | 2023-04 | 中文 |     通用     | [ckpt](https://modelscope.cn/models/damo/ChatPLUG-3.7B/summary) | [ChatPLUG](https://github.com/X-PLUG/ChatPLUG)![Star](https://img.shields.io/github/stars/X-PLUG/ChatPLUG.svg?style=social&label=Star) |         [阿里巴巴](https://github.com/X-PLUG)          | ED |        [Paper](https://arxiv.org/pdf/2304.07849.pdf)         |
|         ChatPLUG         |  240M   | 2023-04 | 中文 |     通用     | [ckpt](https://modelscope.cn/models/damo/ChatPLUG-240M/summary) | [ChatPLUG](https://github.com/X-PLUG/ChatPLUG)![Star](https://img.shields.io/github/stars/X-PLUG/ChatPLUG.svg?style=social&label=Star) |         [阿里巴巴](https://github.com/X-PLUG)          | ED |        [Paper](https://arxiv.org/pdf/2304.07849.pdf)         |
|       ChatGLM-Med        |   6B    | 2023-04 | 中文 |     医学     | [ckpt](https://drive.google.com/drive/folders/1ZQSN56DloRGQ-Qj7IwzY4jV3ZHKMe9Bc) | [Med-ChatGLM](https://github.com/SCIR-HI/Med-ChatGLM)![Star](https://img.shields.io/github/stars/SCIR-HI/Med-ChatGLM.svg?style=social&label=Star) |      [哈尔滨工业大学](https://github.com/SCIR-HI)      | ED |                                                              |
|         BenTsao          |   7B    | 2023-04 | 中文 |     医学     | [lora-ckpt](https://huggingface.co/thinksoso/lora-llama-med) | [Huatuo-Llama-Med-Chinese](https://github.com/SCIR-HI/Huatuo-Llama-Med-Chinese)![Star](https://img.shields.io/github/stars/SCIR-HI/Huatuo-Llama-Med-Chinese.svg?style=social&label=Star) |      [哈尔滨工业大学](https://github.com/SCIR-HI)      |     CD     |                                                              |
|        DoctorGLM         |   6B    | 2023-04 | 中文 |     医学     |                          [待更新]()                          | [DoctorGLM](https://github.com/xionghonglin/DoctorGLM)![Star](https://img.shields.io/github/stars/xionghonglin/DoctorGLM.svg?style=social&label=Star) |    [xionghonglin](https://github.com/xionghonglin)     | ND |                                                              |
|       Firefly-7b1        |   7B    | 2023-04 | 中文 |     文化     | [ckpt](https://huggingface.co/YeungNLP/firefly-bloom-7b1-qlora-sft) | [Firefly](https://github.com/yangjianxin1/Firefly)![Star](https://img.shields.io/github/stars/yangjianxin1/Firefly.svg?style=social&label=Star) |    [Yang JianXin](https://github.com/yangjianxin1)     |    CD   |                                                              |
|       Firefly-2b6        |   2B    | 2023-04 | 中文 |     文化     |     [ckpt](https://huggingface.co/YeungNLP/firefly-2b6)      | [Firefly](https://github.com/yangjianxin1/Firefly)![Star](https://img.shields.io/github/stars/yangjianxin1/Firefly.svg?style=social&label=Star) |    [Yang JianXin](https://github.com/yangjianxin1)     |    CD   |                                                              |
|       firefly-1b4        |   1B    | 2023-04 | 中文 |     文化     |     [ckpt](https://huggingface.co/YeungNLP/firefly-1b4)      | [Firefly](https://github.com/yangjianxin1/Firefly)![Star](https://img.shields.io/github/stars/yangjianxin1/Firefly.svg?style=social&label=Star) |    [Yang JianXin](https://github.com/yangjianxin1)     |    CD   |                                                              |
|    Chinese-Alpaca-13B    |   13B   | 2023-04 | 中文 |     通用     | [lora-ckpt](https://huggingface.co/ziqingyang/chinese-alpaca-lora-13b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)![Star](https://img.shields.io/github/stars/ymcui/Chinese-LLaMA-Alpaca.svg?style=social&label=Star) |         [Yiming Cui](https://github.com/ymcui)         |    CD   |                                                              |
|    BELLE-LLAMA-13B-2M    |   13B   | 2023-04 | 中文 |     通用     | [ckpt](https://huggingface.co/BelleGroup/BELLE-LLAMA-13B-2M) | [BELLE](https://github.com/LianjiaTech/BELLE)![Star](https://img.shields.io/github/stars/LianjiaTech/BELLE.svg?style=social&label=Star) |         [贝壳](https://github.com/LianjiaTech)         |    CD   |                                                              |
|     LLaMA-65B-tuned      |   65B   | 2023-04 | 中文 |     通用     |                          [待更新]()                          | [LMFlow](https://github.com/OptimalScale/LMFlow)![Star](https://img.shields.io/github/stars/OptimalScale/LMFlow.svg?style=social&label=Star) |    [香港科技大学](https://github.com/OptimalScale)     |    CD   |                                                              |
|     LLaMA-33B-tuned      |   33B   | 2023-04 | 中文 |     通用     | [ckpt](https://drive.google.com/file/d/1IqgqLHwNkWQ7BffheZnqD6a-8Zul1bk6/view?usp=share_link) | [LMFlow](https://github.com/OptimalScale/LMFlow)![Star](https://img.shields.io/github/stars/OptimalScale/LMFlow.svg?style=social&label=Star) |    [香港科技大学](https://github.com/OptimalScale)     |    CD   |                                                              |
|     LLaMA-13B-tuned      |   13B   | 2023-04 | 中文 |     通用     | [ckpt](https://drive.google.com/file/d/1m_rpe6rNpN59kWvjJ3GfKeEmS-68TRYr/view?usp=share_link) | [LMFlow](https://github.com/OptimalScale/LMFlow)![Star](https://img.shields.io/github/stars/OptimalScale/LMFlow.svg?style=social&label=Star) |    [香港科技大学](https://github.com/OptimalScale)     |    CD   |                                                              |
|      LLaMA-7B-tuned      |   7B    | 2023-04 | 中文 |     通用     | [ckpt](https://drive.google.com/file/d/1x5JLae3akVkfFeDhSe3TEyUbPn_GNFyb/view?usp=share_link) | [LMFlow](https://github.com/OptimalScale/LMFlow)![Star](https://img.shields.io/github/stars/OptimalScale/LMFlow.svg?style=social&label=Star) |    [香港科技大学](https://github.com/OptimalScale)     |    CD   |                                                              |
|      Chinese-Vicuna      |   13B   | 2023-03 | 中文 |     通用     | [ckpt](https://huggingface.co/Chinese-Vicuna/Chinese-Vicuna-lora-13b-belle-and-guanaco) | [Chinese-Vicuna](https://github.com/Facico/Chinese-Vicuna)![Star](https://img.shields.io/github/stars/Facico/Chinese-Vicuna.svg?style=social&label=Star) |          [Facico](https://github.com/Facico)           |    CD   |                                                              |
|      Chinese-Vicuna      |   7B    | 2023-03 | 中文 |     通用     | [ckpt](https://huggingface.co/Chinese-Vicuna/Chinese-Vicuna-lora-7b-belle-and-guanaco) | [Chinese-Vicuna](https://github.com/Facico/Chinese-Vicuna)![Star](https://img.shields.io/github/stars/Facico/Chinese-Vicuna.svg?style=social&label=Star) |          [Facico](https://github.com/Facico)           |    CD   |                                                              |
|       ChatYuan-V2        |  0.7B   | 2023-03 | 中英 |     通用     | [ckpt](https://huggingface.co/ClueAI/ChatYuan-large-v2/tree/main) | [ChatYuan](https://github.com/clue-ai/ChatYuan)![Star](https://img.shields.io/github/stars/clue-ai/ChatYuan.svg?style=social&label=Star) |         [元语智能](https://github.com/clue-ai)         | ED |                                                              |
|    Chinese-Alpaca-7B     |   7B    | 2023-03 | 中文 |     通用     | [lora-ckpt](https://huggingface.co/ziqingyang/chinese-alpaca-lora-7b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca)![Star](https://img.shields.io/github/stars/ymcui/Chinese-LLaMA-Alpaca.svg?style=social&label=Star) |         [Yiming Cui](https://github.com/ymcui)         |    CD   |                                                              |
|          Luotuo          |   7B    | 2023-03 | 中文 |     通用     | [ckpt](https://huggingface.co/silk-road/luotuo-lora-7b-0.3)  | [Chinese-alpaca-lora](https://github.com/LC1332/Chinese-alpaca-lora) |                      华中师范大学                      |    CD   |                                                              |
|       BELLE-LLAMA        |   7B    | 2023-03 | 中英 |     通用     | [ckpt](https://huggingface.co/BelleGroup/BELLE-LLAMA-7B-2M)  | [BELLE](https://github.com/LianjiaTech/BELLE)![Star](https://img.shields.io/github/stars/LianjiaTech/BELLE.svg?style=social&label=Star) |         [贝壳](https://github.com/LianjiaTech)         |    CD   |                                                              |
|       BELLE-BLOOM        |   7B    | 2023-03 | 中英 |     通用     |    [ckpt](https://huggingface.co/BelleGroup/BELLE-7B-2M)     | [BELLE](https://github.com/LianjiaTech/BELLE)![Star](https://img.shields.io/github/stars/LianjiaTech/BELLE.svg?style=social&label=Star) |         [贝壳](https://github.com/LianjiaTech)         |    CD   |                                                              |
|        ChatGLM-6B        |   6B    | 2023-03 | 中英 |     通用     |       [ckpt](https://huggingface.co/THUDM/chatglm-6b)        | [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)![Star](https://img.shields.io/github/stars/THUDM/ChatGLM-6B.svg?style=social&label=Star) |          [清华大学](https://github.com/THUDM)          | ND |                                                              |
|         ChatRWKV         |   7B    | 2023-01 | 中英 |     小说     | [ckpt](https://huggingface.co/BlinkDL/rwkv-4-pile-7b/tree/main) | [ChatRWKV](https://github.com/BlinkDL/ChatRWKV)![Star](https://img.shields.io/github/stars/BlinkDL/ChatRWKV.svg?style=social&label=Star) |         [BlinkDL](https://github.com/BlinkDL)          |      RNN       |        [Blog](https://zhuanlan.zhihu.com/p/609154637)        |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## MultiModal-ChatLLM

> 收集包含中文的多模态大模型，具备对话等功能。

|           模型           | 大小 |  时间   |                           语言模型                           |                       视觉模型                        | 语言 | 领域 |                             下载                             |                           项目地址                           |                        机构/个人                         |                   文献                    |
| :----------------------: | :--: | :-----: | :----------------------------------------------------------: | :---------------------------------------------------: | :--: | :--: | :----------------------------------------------------------: | :----------------------------------------------------------: | :------------------------------------------------------: | :---------------------------------------: |
| SEEChat | 6B | 2023-06 | [ChatGLM](https://github.com/THUDM/ChatGLM-6B) |                 CLIP-ViT                  | 中文 |  /   | [ckpt](https://github.com/360CVGroup/SEEChat) | [SEEChat](https://github.com/360CVGroup/SEEChat)![Star](https://img.shields.io/github/stars/360CVGroup/SEEChat.svg?style=social&label=Star) |       [360](https://github.com/360CVGroup)       |                                               |
| Ziya-BLIP2-14B-Visual-v1 | 14B  | 2023-06 | [LLaMA-13B](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1) |                         BLIP2                         | 中英 | 通用 | [ckpt](https://huggingface.co/IDEA-CCNL/Ziya-BLIP2-14B-Visual-v1) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM)![Star](https://img.shields.io/github/stars/IDEA-CCNL/Fengshenbang-LM.svg?style=social&label=Star) |        [IDEA研究院](https://github.com/IDEA-CCNL)        |                                           |
|    Video-LLaMA-BiLLA     |  7B  | 2023-05 | [BiLLa-7B]([BiLLa-7B](https://huggingface.co/Neutralzz/BiLLa-7B-SFT)) | [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4) | 中英 | 通用 | [ckpt](https://huggingface.co/DAMO-NLP-SG/Video-LLaMA-Series/resolve/main/finetune-billa7b-zh.pth) | [Video-LLaMA](https://github.com/DAMO-NLP-SG/Video-LLaMA)![Star](https://img.shields.io/github/stars/DAMO-NLP-SG/Video-LLaMA.svg?style=social&label=Star) |    [达摩院多语言NLP](https://github.com/DAMO-NLP-SG)     | [Paper](https://arxiv.org/abs/2306.02858) |
|     Video-LLaMA-Ziya     | 13B  | 2023-05 | [Ziya-13B](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1) | [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4) | 中英 | 通用 | [ckpt](https://huggingface.co/DAMO-NLP-SG/Video-LLaMA-Series/resolve/main/finetune-ziya13b-zh.pth) | [Video-LLaMA](https://github.com/DAMO-NLP-SG/Video-LLaMA)![Star](https://img.shields.io/github/stars/DAMO-NLP-SG/Video-LLaMA.svg?style=social&label=Star) |    [达摩院多语言NLP](https://github.com/DAMO-NLP-SG)     | [Paper](https://arxiv.org/abs/2306.02858) |
|         XrayGLM          |  6B  | 2023-05 |      [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)       |   [BLIP2-Qformer](https://arxiv.org/abs/2301.12597)   | 中英 | 医学 | [ckpt-300](https://huggingface.co/wangrongsheng/XrayGLM-300) [ckpt-3000](https://huggingface.co/wangrongsheng/XrayGLM-3000) | [XrayGLM](https://github.com/WangRongsheng/XrayGLM)![Star](https://img.shields.io/github/stars/WangRongsheng/XrayGLM.svg?style=social&label=Star) | [澳门理工大学](https://www.mpu.edu.mo/esca/zh/index.php) |                                           |
|  X-LLM  |      | 2023-05 | [ChatGLM](https://github.com/THUDM/ChatGLM-6B) | [ViT-g](https://arxiv.org/abs/2106.04560) | 中文 |  /   | [TODO]() | [X-LLM](https://github.com/phellonchen/X-LLM)![Star](https://img.shields.io/github/stars/phellonchen/X-LLM.svg?style=social&label=Star) | [中科院自动化所](https://github.com/phellonchen) | [Paper](https://arxiv.org/pdf/2305.04160.pdf) |
|       VisualGLM-6B       |  6B  | 2023-05 |      [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)       |   [BLIP2-Qformer](https://arxiv.org/abs/2301.12597)   | 中英 | 通用 |      [ckpt](https://huggingface.co/THUDM/visualglm-6b)       | [VisualGLM-6B](https://github.com/THUDM/VisualGLM-6B)![Star](https://img.shields.io/github/stars/THUDM/VisualGLM-6B.svg?style=social&label=Star) |           [清华大学](https://github.com/THUDM)           |                                           |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 中文指令数据集

> 收集包含中文的指令数据集，用于微调语言模型。

|            名称            | 大小  | 时间    | 语言 |                             下载                             |                           项目地址                           |                             作者                             |                     备注                      |
| :------------------------: | :---: | ------- | :--: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :-------------------------------------------: |
|       chatgpt-corpus       |  3M   | 2023-06 | 中文 |     [dataset](https://github.com/PlexPt/chatgpt-corpus)      |  [chatgpt-corpus](https://github.com/PlexPt/chatgpt-corpus)  |              [plex](https://github.com/PlexPt)               |                                               |
|           Simle            | 350k  | 2023-06 | 中文 | [dataset](https://github.com/qiuhuachuan/smile/tree/main/data) |        [smile](https://github.com/qiuhuachuan/smile)         |        [qiuhuachuan](https://github.com/qiuhuachuan)         |                   心理健康                    |
|           QiZhen           |  20k  | 2023-06 | 中文 | [dataset](https://github.com/CMKRG/QiZhenGPT/blob/main/data/train/sft-20k.json) |       [QiZhenGPT](https://github.com/CMKRG/QiZhenGPT)        |             [浙江大学](https://github.com/CMKRG)             |                     医学                      |
|         BayLing-80         |  80   | 2023-06 | 中英 | [dataset](https://github.com/ictnlp/BayLing/blob/main/data/BayLing-80) |         [BayLing](https://github.com/ictnlp/BayLing)         |           [中国科学院](https://github.com/ictnlp)            |                   多轮指令                    |
|      Tigerbot-dataset      | 120k  | 2023-06 | 中英 |     [dataset](https://github.com/TigerResearch/TigerBot)     |    [TigerBot](https://github.com/TigerResearch/TigerBot)     |         [虎博科技](https://github.com/TigerResearch)         |                                               |
|        lawyer-llama        |   /   | 2023-05 | 中文 | [dataset](https://github.com/AndrewZhe/lawyer-llama/tree/main/data) |  [lawyer-llama](https://github.com/AndrewZhe/lawyer-llama)   |         [Quzhe Huang](https://github.com/AndrewZhe)          |                     法律                      |
|         Bactrian-X         |  67K  | 2023-05 | 多语 | [dataset](https://huggingface.co/datasets/MBZUAI/Bactrian-X) |    [bactrian-x](https://github.com/mbzuai-nlp/bactrian-x)    |           [MBZUAI](https://github.com/mbzuai-nlp)            |                                               |
|      CrimeKgAssitant       |  52k  | 2023-05 | 中文 |       [dataset](https://github.com/LiuHC0428/LAW-GPT)        |       [LAW-GPT](https://github.com/LiuHC0428/LAW-GPT)        |         [hongchengliu](https://github.com/LiuHC0428)         |                     法律                      |
|     moss-002-sft-data      | 1.1M  | 2023-04 | 中英 | [dataset](https://huggingface.co/datasets/fnlp/moss-002-sft-data) |          [MOSS](https://github.com/OpenLMLab/MOSS)           |           [复旦大学](https://github.com/OpenLMLab)           |                                               |
|     moss-003-sft-data      | 1.1M  | 2023-04 | 中英 | [dataset](https://github.com/OpenLMLab/MOSS/tree/main/SFT_data/conversations/conversation_without_plugins) |          [MOSS](https://github.com/OpenLMLab/MOSS)           |           [复旦大学](https://github.com/OpenLMLab)           |                                               |
|  moss-003-sft-plugin-data  | 300K  | 2023-04 | 中英 | [dataset](https://github.com/OpenLMLab/MOSS/tree/main/SFT_data/conversations/conversation_with_plugins) |          [MOSS](https://github.com/OpenLMLab/MOSS)           |           [复旦大学](https://github.com/OpenLMLab)           |                                               |
|       Safety-Prompts       | 100K  | 2023-04 | 中文 |    [dataset](https://github.com/thu-coai/Safety-Prompts)     | [Safety-Prompts](https://github.com/thu-coai/Safety-Prompts) |           [清华大学](https://github.com/thu-coai)            |   [评测平台](http://115.182.62.166:18000/)    |
|           OASST1           |   /   | 2023-04 | 多语 | [dataset](https://huggingface.co/datasets/OpenAssistant/oasst1) | [Open-Assistant](https://github.com/LAION-AI/Open-Assistant) |    [OpenAssistant](https://huggingface.co/OpenAssistant)     |                                               |
|         ShareChat          |  90K  | 2023-04 | 中英 |     [dataset](https://paratranz.cn/projects/6725/files)      |       [ShareChat](https://paratranz.cn/projects/6725)        |         [czhko](https://paratranz.cn/projects/6725)          |                                               |
|         GPT-4-LLM          |  52K  | 2023-04 | 中文 | [dataset](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM/blob/main/data/alpaca_gpt4_data_zh.json) | [GPT-4-LLM](https://github.com/Instruction-Tuning-with-GPT-4/GPT-4-LLM) | [Instruction-Tuning-with-GPT-4](https://github.com/Instruction-Tuning-with-GPT-4) |   [paper](https://arxiv.org/abs/2304.03277)   |
|            COIG            | 200K  | 2023-04 | 中文 |     [dataset](https://huggingface.co/datasets/BAAI/COIG)     |   [FlagInstruct](https://github.com/FlagOpen/FlagInstruct)   |             [BAAI](https://huggingface.co/BAAI)              | [paper](https://arxiv.org/pdf/2304.07987.pdf) |
|           RedGPT           |  50k  | 2023-04 | 中文 |       [dataset](https://github.com/ziliwangnlp/RedGPT)       |       [RedGPT](https://github.com/ziliwangnlp/RedGPT)        |          [MiniGPT](https://github.com/ziliwangnlp)           |                                               |
|        shareGPT_cn         |  20k  | 2023-04 | 中文 | [dataset](https://huggingface.co/datasets/shareAI/shareGPT_cn) | [shareGPT_cn](https://huggingface.co/datasets/shareAI/shareGPT_cn) |          [shareAI](https://huggingface.co/shareAI)           |                                               |
|    generated_chat_0.4M     | 0.4M  | 2023-04 | 中文 | [dataset](https://huggingface.co/datasets/BelleGroup/generated_chat_0.4M) |        [BELLE](https://github.com/LianjiaTech/BELLE)         |      [Ke Technologies](https://github.com/LianjiaTech)       |                   角色对话                    |
|    multiturn_chat_0.8M     | 0.8M  | 2023-04 | 中文 | [dataset](https://huggingface.co/datasets/BelleGroup/multiturn_chat_0.8M) |        [BELLE](https://github.com/LianjiaTech/BELLE)         |      [Ke Technologies](https://github.com/LianjiaTech)       |                   多轮任务                    |
|     school_math_0.25M      | 0.25M | 2023-04 | 中文 | [dataset](https://huggingface.co/datasets/BelleGroup/school_math_0.25M) |        [BELLE](https://github.com/LianjiaTech/BELLE)         |      [Ke Technologies](https://github.com/LianjiaTech)       |                    数学题                     |
|         Zhihu-KOL          |   /   | 2023-03 | 中文 | [ dataset](https://huggingface.co/datasets/wangrui6/Zhihu-KOL) |      [Zhihu-KOL](https://github.com/wangrui6/Zhihu-KOL)      |         [Rui Wang](https://huggingface.co/wangrui6)          |                                               |
|      InstructionWild       | 104k  | 2023-03 | 中英 | [dataset](https://github.com/XueFuzhao/InstructionWild/tree/main/data) | [InstructionWild](https://github.com/XueFuzhao/InstructionWild) |          [Xue Fuzhao](https://github.com/XueFuzhao)          |                                               |
|         Alpaca-CoT         |  /.   | 2023-03 | 中英 | [dataset](https://huggingface.co/datasets/QingyiSi/Alpaca-CoT/tree/main) |    [Alpaca-CoT](https://github.com/PhoebusSi/Alpaca-CoT)     |         [Qingyi Si](https://huggingface.co/QingyiSi)         |                                               |
|       GuanacoDataset       |   /   | 2023-03 | 多语 | [dataset](https://huggingface.co/datasets/JosephusCheung/GuanacoDataset) |      [guanaco-model](https://guanaco-model.github.io/)       |         [Guanaco](https://github.com/Guanaco-Model)          |                                               |
| Traditional-Chinese-alpaca |  52K  | 2023-03 | 中文 | [dataset](https://github.com/ntunlplab/traditional-chinese-alpaca/tree/main/data) | [Traditional-Chinese Alpaca](https://github.com/ntunlplab/traditional-chinese-alpaca) |         [NTU NLP Lab](https://github.com/ntunlplab)          |                    gpt翻译                    |
|   alpaca_chinese_dataset   |   /   | 2023-03 | 中文 |                         [dataset]()                          | [alpaca_chinese_dataset](https://github.com/hikariming/alpaca_chinese_dataset) |            [akou](https://github.com/hikariming)             |                   人工校验                    |
|   alpaca-chinese-dataset   |   /   | 2023-03 | 中文 | [dataset](https://github.com/carbonz0/alpaca-chinese-dataset) | [alpaca-chinese-dataset](https://github.com/carbonz0/alpaca-chinese-dataset) |            [carbonz](https://github.com/carbonz0)            |                   机器翻译                    |
|        train_2M_CN         |  2M   | 2023-03 | 中文 | [dataset](https://huggingface.co/datasets/BelleGroup/train_2M_CN) |        [BELLE](https://github.com/LianjiaTech/BELLE)         |      [Ke Technologies](https://github.com/LianjiaTech)       |                                               |
|        train_1M_CN         |  1M   | 2023-03 | 中文 | [dataset](https://huggingface.co/datasets/BelleGroup/train_1M_CN) |        [BELLE](https://github.com/LianjiaTech/BELLE)         |      [Ke Technologies](https://github.com/LianjiaTech)       |                                               |
|       train_0.5M_CN        | 0.5M  | 2023-03 | 中文 | [dataset](https://huggingface.co/datasets/BelleGroup/train_0.5M_CN) |        [BELLE](https://github.com/LianjiaTech/BELLE)         |      [Ke Technologies](https://github.com/LianjiaTech)       |                                               |
|   HC3 人类-ChatGPT 问答    |   /   | 2023-03 | 中文 | [dataset](https://www.modelscope.cn/datasets/simpleai/HC3-Chinese/summary) | [chatgpt-comparison-detection](https://github.com/Hello-SimpleAI/chatgpt-comparison-detection) |        [SimpleAI](https://github.com/Hello-SimpleAI)         |                                               |
|     firefly-train-1.1M     | 1.1M  | 2023-03 | 中文 | [dataset](https://huggingface.co/datasets/YeungNLP/firefly-train-1.1M) |      [Firefly](https://github.com/yangjianxin1/Firefly)      |       [Jianxin Yang](https://github.com/yangjianxin1)        |                                               |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 大模型评估基准

### 1. C-Eval ![Star](https://img.shields.io/github/stars/SJTU-LIT/ceval.svg?style=social&label=Star)

C-Eval 是一个全面的中文基础模型评估套件。它包含了13948个多项选择题，涵盖了52个不同的学科和四个难度级别，查看[论文](https://arxiv.org/abs/2305.08322)了解更多细节。

[[官方网站](https://cevalbenchmark.com/)]   [[Github](https://github.com/SJTU-LIT/ceval)]  [[论文](https://arxiv.org/abs/2305.08322)] 

### 2. FlagEval ![Star](https://img.shields.io/github/stars/FlagOpen/FlagEval.svg?style=social&label=Star)

FlagEval是一个面向AI基础模型的评测工具包。我们的目标是探索和集合科学、公正、开放的基础模型评测基准、方法及工具，对多领域（如语言、语音、视觉及多模态）的基础模型进行多维度（如准确性、效率、鲁棒性等）的评测。我们希望通过对基础模型的评测，加深对基础模型的理解，促进相关的技术创新及产业应用。

[[官方网站](https://cevalbenchmark.com/)]   [[Github](https://github.com/FlagOpen/FlagEval)] 

### 3. SuperCLUElyb ![Star](https://img.shields.io/github/stars/CLUEbenchmark/SuperCLUElyb.svg?style=social&label=Star)

SuperCLUE琅琊榜，这是一个中文通用大模型对战评价基准，它以众包的方式提供匿名、随机的对战。在本文中，我们发布了初步的结果和基于Elo评级系统的排行榜，Elo评级是国际象棋和其他竞技游戏中广泛使用的评级系统。我们邀请整个社区加入这项工作，贡献新的模型，并通过提问和投票选出你最喜欢的答案来评估它们。

[[官方网站](https://www.superclueai.com/)]   [[Github](https://github.com/CLUEbenchmark/SuperCLUElyb)]

### 4. XiezhiBenchmark ![Star](https://img.shields.io/github/stars/mikegu721/xiezhibenchmark.svg?style=social&label=Star)

该基准包括来自13个不同学科的516个学科的220,000个多项选择题，以及15,000个来自单一学科和多个学科的问题。我们对47个最新的大型语言模型在Xiezhi上进行了评估，结果表明在科学、工程、农学、医学和艺术等领域，大型语言模型的表现超过了人类的平均水平，但在经济学、法学、教育学、文学、历史和管理学等领域，人类的表现仍然远远超过了大型语言模型。

[[官方网站]()]   [[Github](https://github.com/mikegu721/xiezhibenchmark)] [[论文](https://arxiv.org/abs/2306.05783)]

### 5. Open LLM Leaderboard

由HuggingFace组织的一个LLM评测榜单，目前已评估了较多主流的开源LLM模型，以英文为主。主要目标是跟踪、排名和评估最新的大语言模型和聊天机器人，让所有人方便的观察到开源社区的进展和评估这些模型。这个排行榜有一个关键优势，社区中的任何成员都可以提交模型，并在 Hugging Face 的 GPU 集群上自动评估。

[[官方网站](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)] 

### 6. 中文大模型安全评测平台 ![Star](https://img.shields.io/github/stars/thu-coai/Safety-Prompts.svg?style=social&label=Star)

大模型安全测评依托于一套系统的安全评测框架，涵盖了仇恨言论、偏见歧视言论、犯罪违法、隐私、伦理道德等八大类别，包括细粒度划分的40余个二级安全类别。

[[官方网站](http://coai.cs.tsinghua.edu.cn/leaderboard/)]   [[Github](https://github.com/thu-coai/Safety-Prompts)] [[论文](https://arxiv.org/abs/2304.10436)]

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 在线体验大模型

> **注**：需要申请或者注册方可体验

### 1. ChatGPT--OpenAI

OpenAI所提出的GPT相关模型，也是目前最火的大语言模型，发布版本已经到了4.0.

[[官方网站](https://chat.openai.com/chat)] 

### 2. New bing--微软

NewBing是微软在2023年3月推出的一款全新的搜索引擎，它基于OpenAI的大型语言模型（LLM），并结合了ChatGPT和DALL·E的技术，为用户提供了一个AI驱动的网络助手。

[[官方网站](https://www.bing.com/)] 

### 3. 文心一言--百度

百度全新一代知识增强大语言模型，文心大模型家族的新成员，能够与人对话互动，回答问题，协助创作，高效便捷地帮助人们获取信息、知识和灵感。

[[官方网站](https://yiyan.baidu.com/welcome)] 

### 4. 通义大模型--阿里

阿里大模型统一品牌，覆盖语言、听觉、多模态等领域致力于实现接近人类智慧的通用智能，让AI从“单一感官”到“五官全开”

[[官方网站](https://tongyi.aliyun.com/)] 

### 5. 星火认知大模型--科大讯飞

科大讯飞推出的新一代认知智能大模型，拥有跨领域的知识和语言理解能力，能够基于自然对话方式理解与执行任务。从海量数据和大规模知识中持续进化，实现从提出、规划到解决问题的全流程闭环。

[[官方网站](https://xinghuo.xfyun.cn/)] 

### 6. Claude--Anthropic

Claude，是人工智能初创公司Anthropic 发布的一款类似ChatGPT的产品。

[[官方网站](https://www.anthropic.com/product)] 

### 7. ChatGLM--智谱AI

基于千亿基座模型 GLM-130B，注入代码预训练，通过有监督微调等技术实现人类意图对齐，具备问答、多轮对话、代码生成功能的中英双语大模型。

[[官方网站](https://chatglm.cn/)] 

### 8. 天工大模型--昆仑万维

天工作为一款大型语言模型，拥有强大的自然语言处理和智能交互能力，能够实现智能问答、聊天互动、文本生成等多种应用场景，并且具有丰富的知识储备，涵盖科学、技术、文化、艺术、历史等领域。

[[官方网站](https://tiangong.kunlun.com/)] 

### 9. 序列猴子大模型--出门问问

序列猴子大模型是一个具有长序列、多模态、单模型、大数据等特点的超大规模语言模型，基于其通用的表示能力与推理能力，能够进行多轮交互，打造更便捷流畅的用户体验，极大地提高了生产效率和数据处理能力，被广泛应用于问答系统、自然语言处理、机器翻译、文本摘要等领域。

[[官方网站](https://openapi.mobvoi.com/largemodel-introduce)] 

### 10. MOSS--复旦大学

MOSS是复旦大学自然语言处理实验室发布的国内第一个对话式大型语言模型

[[官方网站](https://moss.fastnlp.top/)] 

### 11. 360智脑大模--360

360智脑的生成与创作、多轮对话、代码能力、阅读理解、逻辑与推理、多模态等十大核心能力可覆盖大模型全部应用场景。

[[官方网站](https://ai.360.cn/)] 

### 12. 曹植GPT大语言模型--达观数据

达观数据积极探索大语言模型LLM的实践，研发国产版GPT“曹植”系统，作为垂直、专用、自主可控的国产版ChatGPT模型，不仅实现专业领域的AIGC智能化应用，且可内置在客户各类业务系统中提供专用服务

[[官方网站](http://www.datagrand.com/products/aigc/)] 

### 13. 日日新--商汤

商汤“日日新SenseNova”大模型体系，正式问世

不仅展示了大模型体系下的语言大模型，还展示了AI文生图创作、2D/3D数字人生成、大场景/小物体生成等一系列生成式AI模型及应用，还揭开了依托商汤AI大装置SenseCore实现“大模型+大算力”融合创新的研发体系。

[[官方网站](https://techday.sensetime.com/list)] 

### 14. 天燕大模型--APUS

天燕大模型是APUS公司自研的多模态大模型（LMM），具备对文本、图像、视频、音频的理解和生成能力（视频和音频的能力即将推出）。

[[官方网站](https://www.apusai.com/#/)] 

### 15. 元乘象--智子引擎

图文机器人

[[官方网站](https://chatimg.aixiaoqingxu.com/)] 

### 16. 西湖大模型--西湖心辰

[[官方网站](https://xinchenai.com/)] 

### 17. Dongni--深思考

AI多模态搜索引擎

[[官方网站](https://www.dongni.ai/#/)] 

### 18. 山海大模型--云知声

只需一次对话即可获取信息、知识和灵感，解决需求。是每个人身边的助理、朋友和专家。

[[官方网站](https://shanhai.unisound.com/)] 

### 19. MiniMax大模型--MiniMax

MiniMax 最新一代的中文大语言模型帮助人类高效写作、激发创意、获取知识、做出决策现已对企业开放API体验

[[官方网站](https://api.minimax.chat/)] 

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 开源模型库平台

1. 🤗[huggingface](https://huggingface.co/): The AI community building the future.
* 模型下载地址: [https://huggingface.co/models](https://huggingface.co/models)

2. [ModelScope](https://modelscope.cn/home): ModelScope平台是以模型为中心的模型开源社区
* 模型下载地址:[https://modelscope.cn/models](https://modelscope.cn/models)

3. [flagopen](https://flagopen.baai.ac.cn/#/home): flagopen飞智大模型技术开源体系
* 模型下载地址: [https://model.baai.ac.cn/models](https://model.baai.ac.cn/models)

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 开源数据集库

1. huggfaceing数据集仓库: [https://huggingface.co/datasets](https://huggingface.co/datasets)
* 包含了自然语言处理、计算机视觉、语音、多模态等数据集，内置100多个多语言公共数据集下载

2. ModelScope数据集仓库:[https://modelscope.cn/datasets](https://modelscope.cn/datasets)
* 提供了覆盖自然语言处理、计算机视觉、语音、多模态等数据集，更有阿里巴巴集团贡献的专业领域数据集，

3. flagopen数据集仓库: [https://data.baai.ac.cn/data](https://data.baai.ac.cn/data)
* 内置公共数据集下载，可下200G大规模预训练语料[WuDaoCorpora](https://data.baai.ac.cn/details/WuDaoCorporaText)

4. cluebenchmarks数据集仓库：[https://www.cluebenchmarks.com/dataSet_search.html](https://www.cluebenchmarks.com/dataSet_search.html)
* 多个中英文NLP数据集，并可申请下载100GB的高质量中文预训练语料[CLUECorpus2020](https://github.com/CLUEbenchmark/CLUECorpus2020)

5. [MNBVC](https://github.com/esbatmop/MNBVC): Massive Never-ending BT Vast Chinese corpus
* 超大规模中文语料集

6. OpenDataLab数据集仓库: [https://opendatalab.com/](https://opendatalab.com/)
* OpenDataLab 是有影响力的数据开源开放平台，公开数据集触手可及。

7. [OSCAR](https://oscar-project.org/): Open Super-large Crawled Aggregated coRpus, 多语言数据集
* 最新版本包含1.4T的中文语言数据集

<p align="right">[<a href="#top">Back to Top</a>]</p>

## NLU系列

### BERT

+ 2018 | BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding | Jacob Devlin, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1810.04805)
+ 2019 | Pre-Training with Whole Word Masking for Chinese BERT | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1906.08101)

| 模型            | 版本  | TensorFlow                                                   | PyTorch                                                      | 作者                                                  | 源地址                                                       | 应用领域     |
| --------------- | ----- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------- | ------------------------------------------------------------ | ------------ |
| BERT-Base       | base  | [Google Drive](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip) |                                                              | [Google Research](https://github.com/google-research) | [github](https://github.com/google-research/bert)            | 通用         |
| BERT-wwm        | base  | <p>[Google Drive](https://drive.google.com/open?id=1RoTQsXp2hkQ1gSRVylRIJfQxJUgkfJMW)<br>[讯飞云-07Xj](http://pan.iflytek.com/#/link/A2483AD206EF85FD91569B498A3C3879)</p> | [Google Drive](https://drive.google.com/open?id=1AQitrjbvCWc51SYiLN-cJq4e0WiNN4KY) | [Yiming Cui](https://github.com/ymcui)                | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用         |
| BERT-wwm-ext    | base  | <p>[Google Drive](https://drive.google.com/open?id=1buMLEjdtrXE2c4G1rpsNGWEx7lUQ0RHi)<br>[讯飞云-4cMG](http://pan.iflytek.com/#/link/653637473FFF242C3869D77026C9BDB5)</p> | [Google Drive](https://drive.google.com/open?id=1iNeYFhCBJWeUsIlnW_2K6SMwXkM4gLb_) | [Yiming Cui](https://github.com/ymcui)                | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用         |
| bert-base-民事  | base  | [阿里云](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/ms.zip) |                                                              | [THUNLP](https://github.com/thunlp)                   | [github](https://github.com/thunlp/OpenCLaP)                 | 司法         |
| bert-base-刑事  | base  | [阿里云](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/xs.zip) |                                                              | [THUNLP](https://github.com/thunlp)                   | [github](https://github.com/thunlp/OpenCLaP)                 | 司法         |
| BAAI-JDAI-BERT  | base  | [京东云](https://jdai009.s3.cn-north-1.jdcloud-oss.com/jd-aig/open/models/nlp_baai/20190918/JDAI-BERT.tar.gz?AWSAccessKeyId=86FD402DD0CB693D629F6E62DC11E0E6&Expires=1634304356&Signature=dfnLvSzXeerRPSnMsZXSoEwdmkw%3D) |                                                              | [JDAI](https://github.com/jd-aig)                     | [github](https://github.com/jd-aig/nlp_baai/tree/master/pretrained_models_and_embeddings) | 电商客服对话 |
| FinBERT         | base  | <p>[Google Drive](https://drive.google.com/file/d/193B4sT63mMeh4zfge0FJbbFY447KiJXp/view?usp=sharing)<br>[百度网盘-1cmp](https://pan.baidu.com/share/init?surl=D-pVJyW6bbJSre5RxotJkA)</p> | <p>[Google Drive](https://drive.google.com/file/d/1qW1YWtw3q9Q28QThrIY-rDU9Gl-SLIKO/view?usp=sharing)<br>[百度网盘-986f](https://pan.baidu.com/share/init?surl=y_O586GBmZZ7g4d2nOF0Vg)</p> | [Value Simplex](https://github.com/valuesimplex)      | [github](https://github.com/valuesimplex/FinBERT)            | 金融科技领域 |
| EduBERT         | base  | [好未来AI](https://ai.100tal.com/download/TAL-EduBERT-TF.zip) | [好未来AI](https://ai.100tal.com/download/TAL-EduBERT.zip)   | [tal-tech](https://github.com/tal-tech)               | [github](https://github.com/tal-tech/edu-bert)               | 教育领域     |
| guwenbert-base  | base  |                                                              | <p>[百度网盘-4jng](https://pan.baidu.com/s/1dw_08p7CVsz0jVj4jd58lQ)<br>[huggingface](https://huggingface.co/ethanyt/guwenbert-base)</p> | [Ethan](https://github.com/Ethan-yt)                  | [github](https://github.com/Ethan-yt/guwenbert)              | 古文领域     |
| guwenbert-large | large |                                                              | <p>[百度网盘-m5sz](https://pan.baidu.com/s/1TL9mBIlIv2rSvp61xCkeJQ)<br>[huggingface](https://huggingface.co/ethanyt/guwenbert-large)</p> | [Ethan](https://github.com/Ethan-yt)                  | [github](https://github.com/Ethan-yt/guwenbert)              | 古文领域     |
| BERT-CCPoem     | small |                                                              | [thunlp](https://thunlp.oss-cn-qingdao.aliyuncs.com/BERT_CCPoem_v1.zip) | [THUNLP-AIPoet](https://github.com/THUNLP-AIPoet)     | [github](https://github.com/THUNLP-AIPoet/BERT-CCPoem)       | 古典诗歌     |

备注: 

> wwm全称为**Whole Word Masking **,一个完整的词的部分WordPiece子词被mask，则同属该词的其他部分也会被mask

> ext表示在更多数据集下训练

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ChineseBERT

+ 2021 | ChineseBERT: Chinese Pretraining Enhanced by Glyph and Pinyin Information | Zijun Sun, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2106.16038.pdf)

| 模型        | 版本  | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                             | 应用领域 |
| ----------- | ----- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | -------------------------------------------------- | -------- |
| ChineseBERT | base  |            | [huggingface](https://huggingface.co/ShannonAI/ChineseBERT-base) | [ShannonAI](https://github.com/ShannonAI) | [github](https://github.com/ShannonAI/ChineseBert) | 通用     |
| ChineseBERT | large |            | [huggingface](https://huggingface.co/ShannonAI/ChineseBERT-large) | [ShannonAI](https://github.com/ShannonAI) | [github](https://github.com/ShannonAI/ChineseBert) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RoBERTa

+ 2019 | RoBERTa: A Robustly Optimized BERT Pretraining Approach | Yinhan Liu, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1907.11692.pdf)

| 模型                   | 版本     | TensorFlow                                                   | PyTorch                                                      | 作者                                        | 源地址                                                       | 应用领域 |
| ---------------------- | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------------------------ | -------- |
| RoBERTa-tiny-clue      | tiny     | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny-clue.zip) | [百度网盘-8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [github](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |
| RoBERTa-tiny-pair      | tiny     | [google drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny-pair.zip) | [百度网盘-8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [github](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |
| RoBERTa-tiny3L768-clue | tiny     | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny3L768-clue.zip) |                                                              | [CLUE](https://github.com/CLUEbenchmark)    | [github](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |
| RoBERTa-tiny3L312-clue | tiny     | [google drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny3L312-clue.zip) | [百度网盘-8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [github](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |
| RoBERTa-large-pair     | large    | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-large-pair.zip) | [百度网盘-8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [github](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |
| RoBERTa-large-clue     | large    | [google drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-large-clue.zip) | [百度网盘-8qvb](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | [CLUE](https://github.com/CLUEbenchmark)    | [github](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用     |
| RBT3                   | 3层base  | <p>[Google Drive](https://drive.google.com/file/d/1-rvV0nBDvRCASbRz8M9Decc3_8Aw-2yi/view?usp=drive_open)<br>[讯飞云-b9nx](https://pan.iflytek.com/link/275E5B46185C982D4AF5AC295E1651B6)</p> | [Google Drive](https://drive.google.com/file/d/1_LqmIxm8Nz1Abvlqb8QFZaxYo-TInOed/view) | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用     |
| RBTL3                  | 3层large | <p>[Google Drive](https://drive.google.com/open?id=1Jzn1hYwmv0kXkfTeIvNT61Rn1IbRc-o8)<br>[讯飞云-vySW](https://pan.iflytek.com/link/0DD18FAC080BAF75DBA28FB5C0047760)</p> | [Google Drive](https://drive.google.com/open?id=1eHM3l4fMo6DsQYGmey7UZGiTmQquHw25) | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用     |
| RBTL4                  | 4层large | [讯飞云-e8dN](http://pan.iflytek.com/link/7B04C5BF09812DB241BBA973D649824C) |                                                              | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用     |
| RBTL6                  | 6层large | [讯飞云-XNMA](http://pan.iflytek.com/link/B935B1F701A8FD352CAA74614126C4A2) |                                                              | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用     |
| RoBERTa-wwm-ext        | base     | <p>[Google Drive](https://drive.google.com/open?id=1jMAKIJmPn7kADgD3yQZhpsqM-IRM1qZt)<br>[讯飞云-Xe1p](http://pan.iflytek.com/#/link/98D11FAAF0F0DBCB094EE19CCDBC98BF)</p> | [Google Drive](https://drive.google.com/open?id=1eHM3l4fMo6DsQYGmey7UZGiTmQquHw25) | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用     |
| RoBERTa-wwm-ext-large  | large    | <p>[Google Drive](https://drive.google.com/open?id=1dtad0FFzG11CBsawu8hvwwzU2R0FDI94)<br>[讯飞云-u6gC](http://pan.iflytek.com/#/link/AC056611607108F33A744A0F56D0F6BE)</p> | [Google Drive](https://drive.google.com/open?id=1-2vEZfIFCdM1-vJ3GD6DlSyKT4eVXMKq) | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-BERT-wwm)          | 通用     |
| RoBERTa-base           | base     | <p>[Google Drive](https://drive.google.com/open?id=1ykENKV7dIFAqRRQbZIh0mSb7Vjc2MeFA)<br>[百度网盘](https://pan.baidu.com/s/1hAs7-VSn5HZWxBHQMHKkrg)</p> | <p>[Google Drive](https://drive.google.com/open?id=1H6f4tYlGXgug1DdhYzQVBuwIGAkAflwB)<br>[百度网盘](https://pan.baidu.com/s/1AGC76N7pZOzWuo8ua1AZfw)</p> | [brightmart](https://github.com/brightmart) | [github](https://github.com/brightmart/roberta_zh)           | 通用     |
| RoBERTa-Large          | large    | <p>[Google Drive](https://drive.google.com/open?id=1W3WgPJWGVKlU9wpUYsdZuurAIFKvrl_Y)<br>[百度网盘](https://pan.baidu.com/s/1Rk_QWqd7-wBTwycr91bmug)</p> | [Google Drive](https://drive.google.com/open?id=1yK_P8VhWZtdgzaG0gJ3zUGOKWODitKXZ) | [brightmart](https://github.com/brightmart) | [github](https://github.com/brightmart/roberta_zh)           | 通用     |
| RoBERTa-tiny           | tiny     | [huggingface](https://huggingface.co/uer)                    | [huggingface](https://huggingface.co/uer)                    | [DBIIR @ RUC](https://github.com/dbiir)     | [UER](https://github.com/dbiir/UER-py)                       | 通用     |
| RoBERTa-mini           | mini     | [huggingface](https://huggingface.co/uer)                    | [huggingface](https://huggingface.co/uer)                    | [DBIIR @ RUC](https://github.com/dbiir)     | [UER](https://github.com/dbiir/UER-py)                       | 通用     |
| RoBERTa-small          | small    | [huggingface](https://huggingface.co/uer)                    | [huggingface](https://huggingface.co/uer)                    | [DBIIR @ RUC](https://github.com/dbiir)     | [UER](https://github.com/dbiir/UER-py)                       | 通用     |
| RoBERTa-medium         | medium   | [huggingface](https://huggingface.co/uer)                    | [huggingface](https://huggingface.co/uer)                    | [DBIIR @ RUC](https://github.com/dbiir)     | [UER](https://github.com/dbiir/UER-py)                       | 通用     |
| RoBERTa-base           | base     | [huggingface](https://huggingface.co/uer)                    | [huggingface](https://huggingface.co/uer)                    | [DBIIR @ RUC](https://github.com/dbiir)     | [UER](https://github.com/dbiir/UER-py)                       | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ALBERT

+ 2019 | ALBERT: A Lite BERT For Self-Supervised Learning Of Language Representations | Zhenzhong Lan, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1909.11942.pdf)

| 模型             | 版本    | TensorFlow                                                   | PyTorch                                                      | 作者                                                  | 源地址                                              | 应用领域 |
| ---------------- | ------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------- | --------------------------------------------------- | -------- |
| Albert_tiny      | tiny    | [Google Drive](https://storage.googleapis.com/albert_zh/albert_tiny_489k.zip) | [Google Drive](https://drive.google.com/open?id=1VBsUJ7R5eWF1VcUBQY6BEn1a9miEvlBr) | [brightmart](https://github.com/brightmart)           | [github](https://github.com/brightmart/albert_zh)   | 通用     |
| Albert_base_zh   | base    | [Google Drive](https://storage.googleapis.com/albert_zh/albert_base_zh_additional_36k_steps.zip) | [Google Drive](https://drive.google.com/open?id=1HeijHGubWR-ElFnfxUf8IrRx7Ghm1S_Q) | [brightmart](https://github.com/brightmart)           | [github](https://github.com/brightmart/albert_zh)   | 通用     |
| Albert_large_zh  | large   | [Google Drive](https://storage.googleapis.com/albert_zh/albert_large_zh.zip) | [Google Drive](https://drive.google.com/open?id=1TAuv7OiFN8qbkT6S_VbfVbhkhg2GUF3q) | [brightmart](https://github.com/brightmart)           | [github](https://github.com/brightmart/albert_zh)   | 通用     |
| Albert_xlarge_zh | xlarge  | [Google Drive](https://storage.googleapis.com/albert_zh/albert_xlarge_zh_183k.zip) | [Google Drive](https://drive.google.com/open?id=1kMhogQRX0uGWIGdNhm7-3hsmHlrzY_gp) | [brightmart](https://github.com/brightmart)           | [github](https://github.com/brightmart/albert_zh)   | 通用     |
| Albert_base      | base    | [Google Drive](https://storage.googleapis.com/albert_models/albert_base_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [github](https://github.com/google-research/ALBERT) | 通用     |
| Albert_large     | large   | [Google Drive](https://storage.googleapis.com/albert_models/albert_large_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [github](https://github.com/google-research/ALBERT) | 通用     |
| Albert_xlarge    | xlarge  | [Google Drive](https://storage.googleapis.com/albert_models/albert_xlarge_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [github](https://github.com/google-research/ALBERT) | 通用     |
| Albert_xxlarge   | xxlarge | [Google Drive](https://storage.googleapis.com/albert_models/albert_xxlarge_zh.tar.gz) |                                                              | [Google Research](https://github.com/google-research) | [github](https://github.com/google-research/ALBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### NEZHA

+ 2019 | NEZHA: Neural Contextualized Representation for Chinese Language Understanding | Junqiu Wei, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1909.00204)

| 模型                           | 版本  | TensorFlow                                                   | PyTorch                                                      | 作者                                                    | 源地址                                                       | 应用领域 |
| ------------------------------ | ----- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------------ | -------- |
| NEZHA-base                     | base  | <p>[Google Drive](https://drive.google.com/drive/folders/1tFs-wMoXIY8zganI2hQgDBoDPqA8pSmh?usp=sharing)<br>[百度网盘-ntn3](https://pan.baidu.com/s/1UVQjy9v_Sv4cQd1ELdjqww)</p> | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI](https://github.com/huawei-noah)                | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |
| NEZHA-base-wwm                 | base  | <p>[Google Drive](https://drive.google.com/drive/folders/1bK6WbqAG-B6BX2d9RPprnh2MPK6zL0t_?usp=sharing)<br>[百度网盘-f68o](https://pan.baidu.com/s/1-YG8e5V2zKCnR3azsGZT1w)</p> | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI](https://github.com/huawei-noah)                | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |
| NEZHA-large                    | large | <p>[Google Drive](https://drive.google.com/drive/folders/1ZPPM5XtTTOrS_CDRak1t2nCBU-LFZ_zs?usp=sharing)<br>[百度网盘-7thu](https://pan.baidu.com/s/1R1Ew-Lu8oIP6QhWO6nqp5Q)</p> | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI](https://github.com/huawei-noah)                | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |
| NEZHA-large-wwm                | large | <p>[Google Drive](https://drive.google.com/drive/folders/1LOAUc9LXyogC2gmP_q1ojqj41Ez01aga?usp=sharing)<br>[百度网盘-ni4o](https://pan.baidu.com/s/1JK1RLIJd2wpuypku3stt8w)</p> | [lonePatient](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | [HUAWEI](https://github.com/huawei-noah)                | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用     |
| <p>WoNEZHA</br>(word-base)</p> | base  | [百度网盘-qgkq](https://pan.baidu.com/s/1ABKwUuIiMEEsRXxxlbyKmw) |                                                              | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/WoBERT)         | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### MacBERT

+ 2020 | Revisiting Pre-Trained Models for Chinese Natural Language Processing | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2004.13922.pdf)

| 模型          | 版本  | TensorFlow                                                   | PyTorch | 作者                                   | 源地址                                     | 应用领域 |
| ------------- | ----- | ------------------------------------------------------------ | ------- | -------------------------------------- | ------------------------------------------ | -------- |
| MacBERT-base  | base  | <p>[Google Drive](https://drive.google.com/file/d/1aV69OhYzIwj_hn-kO1RiBa-m8QAusQ5b/view?usp=sharing)<br>[讯飞云-E2cP](http://pan.iflytek.com/#/link/CF2A1F9AEBF859650E8956854A994C1B)</p> |         | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/MacBERT) | 通用     |
| MacBERT-large | large | <p>[Google Drive](https://drive.google.com/file/d/1lWYxnk1EqTA2Q20_IShxBrCPc5VSDCkT/view?usp=sharing)<br>[讯飞云-3Yg3](http://pan.iflytek.com/#/link/805D743F3826EC4F4EB5C774D34432AE)</p> |         | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/MacBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### WoBERT

+ 2020 | 提速不掉点：基于词颗粒度的中文WoBERT | 苏剑林. | spaces | [`Blog post`](https://kexue.fm/archives/7758)

| 模型        | 版本 | TensorFlow                                                   | PyTorch | 作者                                                    | 源地址                                               | 应用领域 |
| ----------- | ---- | ------------------------------------------------------------ | ------- | ------------------------------------------------------- | ---------------------------------------------------- | -------- |
| WoBERT      | base | [百度网盘-kim2](https://pan.baidu.com/s/1BrdFSx9_n1q2uWBiQrpalw) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/WoBERT) | 通用     |
| WoBERT-plus | base | [百度网盘-aedw](https://pan.baidu.com/s/1Ltq3ltQsyBCj56zoOOvI9A) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/WoBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### XLNET

+ 2019 | XLNet: Generalized Autoregressive Pretraining for Language Understanding | Zhilin Yang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1906.08237)

| 模型           | 版本   | TensorFlow                                                   | PyTorch                                                      | 作者                                        | 源地址                                           | 应用领域 |
| -------------- | ------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------------ | -------- |
| XLNet-base     | base   | <p>[Google Drive](https://drive.google.com/open?id=1m9t-a4gKimbkP5rqGXXsEAEPhJSZ8tvx)<br>[讯飞云-uCpe](http://pan.iflytek.com/#/link/32619C31BDEFAF2D82CB8C7F66F01D5C)</p> | [Google Drive](https://drive.google.com/open?id=1mPDgcMfpqAf2wk9Nl8OaMj654pYrWXaR) | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-XLNet) | 通用     |
| XLNet-mid      | middle | <p>[Google Drive](https://drive.google.com/open?id=1342uBc7ZmQwV6Hm6eUIN_OnBSz1LcvfA)<br>[讯飞云-68En](http://pan.iflytek.com/#/link/ED7DF7ED04B871AFE8E4D97704B9134D)</p> | [Google Drive](https://drive.google.com/open?id=1u-UmsJGy5wkXgbNK4w9uRnC0RxHLXhxy) | [Yiming Cui](https://github.com/ymcui)      | [github](https://github.com/ymcui/Chinese-XLNet) | 通用     |
| XLNet_zh_Large | large  | [百度网盘](https://pan.baidu.com/s/1dy0Z27DoZdMpSmoz1Q4G5A)  |                                                              | [brightmart](https://github.com/brightmart) | [github](https://github.com/brightmart/xlnet_zh) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ELECTRA

+ 2020 | ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators | Kevin Clark, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2003.10555)

| 模型                  | 版本  | TensorFlow                                                   | PyTorch | 作者                                     | 源地址                                             | 应用领域 |
| --------------------- | ----- | ------------------------------------------------------------ | ------- | ---------------------------------------- | -------------------------------------------------- | -------- |
| ELECTRA-180g-large    | large | <p>[Google Drive](https://drive.google.com/file/d/1P9yAuW0-HR7WvZ2r2weTnx3slo6f5u9q/view?usp=sharing)<br>[讯飞云-Yfcy](http://pan.iflytek.com/#/link/7605874F5A11CD693C60EAB79005CCF3)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |
| ELECTRA-180g-small-ex | small | <p>[Google Drive](https://drive.google.com/file/d/1NYJTKH1dWzrIBi86VSUK-Ml9Dsso_kuf/view?usp=sharing)<br>[讯飞云-GUdp](http://pan.iflytek.com/#/link/3EFCF909FC5CFEA6F0EA7AA774C64CF0)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |
| ELECTRA-180g-base     | base  | <p>[Google Drive](https://drive.google.com/file/d/1RlmfBgyEwKVBFagafYvJgyCGuj7cTHfh/view?usp=sharing)<br>[讯飞云-Xcvm](http://pan.iflytek.com/#/link/38E14C9BDBE8E93F09DFE2198E308489)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |
| ELECTRA-180g-small    | small | <p>[Google Drive](https://drive.google.com/file/d/177EVNTQpH2BRW-35-0LNLjV86MuDnEmu/view?usp=sharing)<br>[讯飞云-qsHj](http://pan.iflytek.com/#/link/D1B8FE678FA5BC31AA43BD99AD09913E)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 通用     |
| legal-ELECTRA-large   | large | <p>[Google Drive](https://drive.google.com/file/d/1jPyVi_t4QmTkFy7PD-m-hG-lQ8cIETzD/view?usp=sharing)<br>[讯飞云-7f7b](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |
| legal-ELECTRA-base    | base  | <p>[Google Drive](https://drive.google.com/file/d/12ZLaoFgpqGJxSi_9KiQV-jdVN4XRGMiD/view?usp=sharing)<br>[讯飞云-7f7b](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |
| legal-ELECTRA-small   | small | <p>[Google Drive](https://drive.google.com/file/d/1arQ5qNTNoc1OyMH8wBUKdTMy2QponIFY/view?usp=sharing)<br>[讯飞云-7f7b](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759)</p> |         | [Yiming Cui](https://github.com/ymcui)   | [github](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |
| ELECTRA-tiny          | tiny  | <p>[Google Drive](https://drive.google.com/file/d/1UP4byt4-kgenwST0KvyMYNbln6FfaSLp/view?usp=sharing)<br>[百度网盘-rs99](https://pan.baidu.com/share/init?surl=4b-IiCkjRg-6XIYPXnezZA)</p> |         | [CLUE](https://github.com/CLUEbenchmark) | [github](https://github.com/CLUEbenchmark/ELECTRA) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ZEN

+ 2019 | ZEN: Pre-training Chinese Text Encoder Enhanced by N-gram Representations | Shizhe Diao, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1911.00720.pdf)

| 模型            | 版本  | TensorFlow | PyTorch                                                      | 作者                                                         | 源地址                                                 | 应用领域 |
| --------------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------ | -------- |
| ZEN-Base        | base  |            | <p>[Google Drive](https://drive.google.com/open?id=1oxNdYMQOpFe3QlttH98bAqg_FQiiVeMr)<br>[百度网盘](https://pan.baidu.com/s/1E2ylFnzGSkwBc8tY_OqZYg)</p> | [Sinovation Ventures AI Institute](https://github.com/sinovation) | [github](https://github.com/sinovation/ZEN)            | 通用     |
| Erlangshen-ZEN2 | large |            | [huggingface](https://huggingface.co/IDEA-CCNL/Erlangshen-ZEN2-668M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL)                    | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ERNIE

+ 2019 | ERNIE: Enhanced Representation through Knowledge Integration | Yu Sun, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1904.09223)

+ 2020 | SKEP: Sentiment Knowledge Enhanced Pre-training for Sentiment Analysis | Hao Tian, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2005.05635)

+ 2020 | ERNIE-Gram: Pre-Training with Explicitly N-Gram Masked Language Modeling for Natural Language Understanding | Dongling Xiao, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2010.12148)

| 模型                 | 版本  | PaddlePaddle                                                 | PyTorch | 作者                                            | 源地址                                                       | 应用领域 |
| -------------------- | ----- | ------------------------------------------------------------ | ------- | ----------------------------------------------- | ------------------------------------------------------------ | -------- |
| ernie-1.0-base       | base  | [link](https://ernie-github.cdn.bcebos.com/model-ernie1.0.1.tar.gz) |         | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/ERNIE)              | 通用     |
| ernie_1.0_skep_large | large | [link](https://senta.bj.bcebos.com/skep/ernie_1.0_skep_large_ch.tar.gz) |         | [Baidu](https://github.com/baidu)               | [github](https://github.com/baidu/Senta)                     | 情感分析 |
| ernie-gram           | base  | [link](https://ernie-github.cdn.bcebos.com/model-ernie-gram-zh.1.tar.gz) |         | [Baidu](https://github.com/baidu)               | [github](https://github.com/PaddlePaddle/ERNIE/tree/develop/ernie-gram) | 通用     |

备注: 

> PaddlePaddle转TensorFlow可参考: [tensorflow_ernie](https://github.com/ArthurRizar/tensorflow_ernie)

> PaddlePaddle转PyTorch可参考: [ERNIE-Pytorch](https://github.com/nghuyong/ERNIE-Pytorch)

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ERNIE3

+ 2021 | ERNIE 3.0: Large-scale Knowledge Enhanced Pre-training for Language Understanding and Generation | Yu Sun, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2107.02137)

+ 2021 | ERNIE 3.0 Titan: Exploring Larger-scale Knowledge Enhanced Pre-training for Language Understanding and Generation | Shuohuan Wang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2106.02241)

| 模型             | 版本                           | PaddlePaddle                                                 | PyTorch                                                      | 作者                                            | 源地址                                                       | 应用领域 |
| ---------------- | ------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------- | ------------------------------------------------------------ | -------- |
| ernie-3.0-base   | 12-layer, 768-hidden, 12-heads | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_base_zh.pdparams) | [huggingface](https://huggingface.co/nghuyong/ernie-3.0-base-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-medium | 6-layer, 768-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_medium_zh.pdparams) | [huggingface](https://huggingface.co/nghuyong/ernie-3.0-medium-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-mini   | 6-layer, 384-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_mini_zh.pdparams) | [huggingface](https://huggingface.co/nghuyong/ernie-3.0-mini-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-micro  | 4-layer, 384-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_micro_zh.pdparams) | [huggingface](https://huggingface.co/nghuyong/ernie-3.0-micro-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-nano   | 4-layer, 312-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_nano_zh.pdparams) | [huggingface](https://huggingface.co/nghuyong/ernie-3.0-nano-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |

> PaddlePaddle转PyTorch可参考: [ERNIE-Pytorch](https://github.com/nghuyong/ERNIE-Pytorch)

<p align="right">[<a href="#top">Back to Top</a>]</p>


### RoFormer

+ 2021 | RoFormer: Enhanced Transformer with Rotary Position Embedding | Jianlin Su, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2104.09864)

+ 2021 | Transformer升级之路：2、博采众长的旋转式位置编码 | 苏剑林. | spaces | [`Blog post`](https://kexue.fm/archives/8265)

| 模型          | 版本       | TensorFlow                                                   | PyTorch | 作者                                                    | 源地址                                                    | 应用领域 |
| ------------- | ---------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------- | --------------------------------------------------------- | -------- |
| roformer      | base(L12)  | [百度网盘-xy9x](https://pan.baidu.com/s/1fiss862YsGCwf2HvU_Jm-g) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer)    | 通用     |
| roformer      | small(L6)  | [百度网盘-gy97](https://pan.baidu.com/s/1iIXgZHHCgrYGXVRRSSCVPg) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer)    | 通用     |
| roformer-char | base(L12)  | [百度网盘-bt94](https://pan.baidu.com/s/1Q1pq8F4Fsl6bTipUAkqeDQ) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer)    | 通用     |
| roformerV2    | small(L6)  | [百度网盘-ttn4](https://pan.baidu.com/s/1huUrC9P60Afggo8AfiUcmA)[追一](https://open.zhuiyi.ai/releases/nlp/models/zhuiyi/chinese_roformer-v2-char_L-6_H-384_A-6.zip) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer-v2) | 通用     |
| roformerV2    | base(L12)  | [百度网盘-pfoh](https://pan.baidu.com/s/1qcnN4LVKVe0-mnHlkN3-6Q)[追一](https://open.zhuiyi.ai/releases/nlp/models/zhuiyi/chinese_roformer-v2-char_L-12_H-768_A-12.zip) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer-v2) | 通用     |
| roformerV2    | large(L24) | [百度网盘-npfv](https://pan.baidu.com/s/1QiJWSZrGxn8vek-8myvL6w)[追一](https://open.zhuiyi.ai/releases/nlp/models/zhuiyi/chinese_roformer-v2-char_L-24_H-1024_A-16.zip) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer-v2) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### StructBERT

+ 2019 | StructBERT: Incorporating Language Structures into Pre-training for Deep Language Understanding | Wei Wang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1908.04577)

| 模型       | 版本       | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                                       | 应用领域 |
| ---------- | ---------- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ------------------------------------------------------------ | -------- |
| StructBERT | large(L24) |            | [阿里云](https://alice-open.oss-cn-zhangjiakou.aliyuncs.com/StructBERT/ch_model) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/StructBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Lattice-BERT

+ 2021 | Lattice-BERT: Leveraging Multi-Granularity Representations in Chinese Pre-trained Language Models | Yuxuan Lai, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2104.07204.pdf)

| 模型        | 版本      | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                                       | 应用领域 |
| ----------- | --------- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ------------------------------------------------------------ | -------- |
| LatticeBERT | tiny(L4)  |            | [阿里云](https://alice-open.oss-cn-zhangjiakou.aliyuncs.com/LatticeBERT/chinese_labert-tiny-std-512.tar.gz) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/LatticeBERT) | 通用     |
| LatticeBERT | small(L6) |            | [阿里云](https://alice-open.oss-cn-zhangjiakou.aliyuncs.com/LatticeBERT/chinese_labert-lite-std-512.tar.gz) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/LatticeBERT) | 通用     |
| LatticeBERT | base(L12) |            | [阿里云](https://alice-open.oss-cn-zhangjiakou.aliyuncs.com/LatticeBERT/chinese_labert-base-std-512.tar.gz) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/LatticeBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Mengzi-BERT

+ 2021 | Mengzi: Towards Lightweight yet Ingenious Pre-trained Models for Chinese | Zhuosheng Zhang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2110.06696)

| 模型            | 版本      | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                       | 应用领域 |
| --------------- | --------- | ---------- | ------------------------------------------------------------ | --------------------------------------- | -------------------------------------------- | -------- |
| Mengzi-BERT     | base(L12) |            | [huggingface](https://huggingface.co/Langboat/mengzi-bert-base) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 通用     |
| Mengzi-BERT-fin | base(L12) |            | [huggingface](https://huggingface.co/Langboat/mengzi-bert-base-fin) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 金融财经 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Bloom

+ 2022 | Bloom: BigScience Large Open-science Open-access Multilingual Language Model | huggingface bigscience | - | [`BLOG`](https://bigscience.huggingface.co/blog/bloom)

| 模型         | 版本    | TensorFlow | PyTorch                                                     | 作者                                        | 源地址                                                | 应用领域 |
| ------------ | ------- | ---------- | ----------------------------------------------------------- | ------------------------------------------- | ----------------------------------------------------- | -------- |
| bloom-6b4-zh | 6B(L30) |            | [huggingface](https://huggingface.co/Langboat/bloom-6b4-zh) | [Langboat](https://huggingface.co/Langboat) | [github](https://github.com/huggingface/transformers) | 通用     |

> 注：作者另有bloom-389m-zh到bloom-2b5-zh等多个中文模型

<p align="right">[<a href="#top">Back to Top</a>]</p>

### TaCL

+ 2021 | TaCL: Improving BERT Pre-training with Token-aware Contrastive Learning | Yixuan Su, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2111.04198.pdf)

| 模型 | 版本      | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                    | 应用领域 |
| ---- | --------- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ----------------------------------------- | -------- |
| TaCL | base(L12) |            | [huggingface](https://huggingface.co/cambridgeltl/tacl-bert-base-chinese) | [yxuansu](https://github.com/yxuansu) | [github](https://github.com/yxuansu/TaCL) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### MC-BERT

+ 2021 | MC-BERT: Conceptualized Representation Learning for Chinese Biomedical Text Mining | alibaba-research | arXiv | [`PDF`](https://arxiv.org/pdf/2008.10813.pdf)

| 模型    | 版本      | TensorFlow | PyTorch                                                      | 作者                                                    | 源地址                                                    | 应用领域 |
| ------- | --------- | ---------- | ------------------------------------------------------------ | ------------------------------------------------------- | --------------------------------------------------------- | -------- |
| MC-BERT | base(L12) |            | [link](https://drive.google.com/open?id=1ccXRvaeox5XCNP_aSk_ttLBY695Erlok) | [alibaba-research](https://github.com/alibaba-research) | [github](https://github.com/alibaba-research/ChineseBLUE) | 生物医疗 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 二郎神

| 模型       | 版本       | 类型 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域 |
| ---------- | ---------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | -------- |
| Erlangshen | large(L24) | bert |            | [huggingface](https://huggingface.co/IDEA-CCNL/Erlangshen-1.3B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### PERT

+ 2022 | PERT: Pre-Training BERT with Permuted Language Model | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2203.06906)

| 模型       | 版本       | TensorFlow                                                   | PyTorch                                                      | 作者                                   | 源地址                                  | 应用领域 |
| ---------- | ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | --------------------------------------- | -------- |
| PERT-base  | base(12L)  | [百度网盘-rcsw](https://pan.baidu.com/s/1yDHkYKmdaJkliTGHWQtdFA?pwd=rcsw) | [huggingface](https://huggingface.co/hfl/chinese-pert-base)  | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/PERT) | 通用     |
| PERT-large | large(24L) | [百度网盘-e9hs](https://pan.baidu.com/s/1MG44TRIgqV6m_StfB_yBqQ?pwd=e9hs) | [huggingface](https://huggingface.co/hfl/chinese-pert-large) | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/PERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### MobileBERT

+ 2020 | MobileBERT: a Compact Task-Agnostic BERT for Resource-Limited Devices | Zhiqing Sun, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2004.02984.pdf)

| 模型                        | 版本  | TensorFlow                                                   | PyTorch | 作者                                   | 源地址                                                | 应用领域 |
| --------------------------- | ----- | ------------------------------------------------------------ | ------- | -------------------------------------- | ----------------------------------------------------- | -------- |
| Chinese-MobileBERT-base-f2  | base  | [百度网盘-56bj](https://pan.baidu.com/s/16g1LgXXAV01I-cFgPdeOow?pwd=56bj) |         | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/Chinese-MobileBERT) | 通用     |
| Chinese-MobileBERT-base-f4  | base  | [百度网盘-v2v7](https://pan.baidu.com/s/16SGBJhWFYru47EEyTZJljA?pwd=v2v7) |         | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/Chinese-MobileBERT) | 通用     |
| Chinese-MobileBERT-large-f2 | large | [百度网盘-6m5a](https://pan.baidu.com/s/1Kp7n8lQJOtevzMovKSa3kw?pwd=6m5a) |         | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/Chinese-MobileBERT) | 通用     |
| Chinese-MobileBERT-large-f4 | large | [百度网盘-3h9b](https://pan.baidu.com/s/19xz9kH1HmM2Og0Aqn7l6vA?pwd=3h9b) |         | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/Chinese-MobileBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GAU-α

+ 2022 | GAU-α: (FLASH) Transformer Quality in Linear Time | Weizhe Hua, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2202.10447.pdf) | [`blog`](https://spaces.ac.cn/archives/9052)

| 模型                              | 版本 | TensorFlow                                                   | PyTorch | 作者                                                    | 源地址                                                  | 应用领域 |
| --------------------------------- | ---- | ------------------------------------------------------------ | ------- | ------------------------------------------------------- | ------------------------------------------------------- | -------- |
| chinese_GAU-alpha-char_L-24_H-768 | base | [下载](https://open.zhuiyi.ai/releases/nlp/models/zhuiyi/chinese_GAU-alpha-char_L-24_H-768.zip) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/GAU-alpha) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### DeBERTa

+ 2020 | DeBERTa: Decoding-enhanced BERT with Disentangled Attention | Pengcheng He, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2006.03654) |

| 模型              | 版本   | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域 |
| ----------------- | ------ | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | -------- |
| DeBERTa-v2-Large  | large  |            | [huggingface](https://huggingface.co/IDEA-CCNL/Erlangshen-DeBERTa-v2-320M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |
| DeBERTa-v2-xLarge | xlarge |            | [huggingface](https://huggingface.co/IDEA-CCNL/Erlangshen-DeBERTa-v2-710M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |
| DeBERTa-v2        | base   |            | [huggingface](https://huggingface.co/IDEA-CCNL/Erlangshen-DeBERTa-v2-186M-Chinese-SentencePiece) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GlyphBERT

+ 2021 | GlyphCRM: Bidirectional Encoder Representation for Chinese Character with its Glyph | Yuxin li, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2107.00395.pdf) |

| 模型          | 版本 | TensorFlow | PyTorch                                                 | 作者                                      | 源地址                                           | 应用领域 |
| ------------- | ---- | ---------- | ------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------ | -------- |
| GlyphCRM-base | base |            | [huggingface](https://huggingface.co/HIT-TMG/GlyphBERT) | [HITsz-TMG](https://github.com/HITsz-TMG) | [github](https://github.com/HITsz-TMG/GlyphBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CKBERT

+ 2022 | Revisiting and Advancing Chinese Natural Language Understanding with Accelerated Heterogeneous Knowledge Pre-training | Zhang, Taolin, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2210.05287)

| 模型                | 版本  | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                       | 应用领域 |
| ------------------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------- | -------------------------------------------- | -------- |
| pai-ckbert-base-zh  | base  |            | [huggingface](https://huggingface.co/alibaba-pai/pai-ckbert-base-zh) | [Alibaba](https://github.com/alibaba) | [github](https://huggingface.co/alibaba-pai) | 通用     |
| pai-ckbert-large-zh | large |            | [huggingface](https://huggingface.co/alibaba-pai/pai-ckbert-large-zh) | [Alibaba](https://github.com/alibaba) | [github](https://huggingface.co/alibaba-pai) | 通用     |
| pai-ckbert-huge-zh  | huge  |            | [huggingface](https://huggingface.co/alibaba-pai/pai-ckbert-huge-zh) | [Alibaba](https://github.com/alibaba) | [github](https://huggingface.co/alibaba-pai) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### LERT

+ 2022 | LERT: A Linguistically-motivated Pre-trained Language Model | Yiming Cui et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.05344)

| 模型               | 版本 | TensorFlow                                                   | PyTorch                                                      | 作者                                   | 源地址                                  | 应用领域 |
| ------------------ | ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | --------------------------------------- | -------- |
| Chinese-LERT-small | 15m  | [百度网盘-4vuy](https://pan.baidu.com/s/1fBk3em8a5iCMwPLJEBq2pQ?pwd=4vuy) | [huggingface](https://huggingface.co/hfl/chinese-lert-small) | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/LERT) | 通用     |
| Chinese-LERT-base  | 400m | [百度网盘-9jgi](https://pan.baidu.com/s/1_yb1jCDJ4s2P8OrF_5E_Tg?pwd=9jgi) | [huggingface](https://huggingface.co/hfl/chinese-lert-base)  | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/LERT) | 通用     |
| Chinese-LERT-large | 1.2G | [百度网盘-s82t](https://pan.baidu.com/s/1pxsS3almc90DPvMXH6BMYQ?pwd=s82t) | [huggingface](https://huggingface.co/hfl/chinese-lert-large) | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/LERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RoCBert

+ 2022 | RoCBert: Robust Chinese Bert with Multimodal Contrastive Pretraining | Hui Su et al. | ACL | [`PDF`](https://aclanthology.org/2022.acl-long.65.pdf)

| 模型    | 版本 | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                       | 应用领域 |
| ------- | ---- | ---------- | ------------------------------------------------------------ | --------------------------------------- | -------------------------------------------- | -------- |
| rocbert | base |            | [huggingface](https://huggingface.co/weiweishi/roc-bert-base-zh) | [Weiwe Shi](https://github.com/sww9370) | [github](https://github.com/sww9370/RoCBert) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### M3E

| 模型      | 版本  | PyTorch                                               | 作者                                      | 源地址                                                       | 备注         |
| --------- | ----- | ----------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------ | ------------ |
| m3e-base  | base  | [m3e-base](https://huggingface.co/moka-ai/m3e-base)   | [Moka-AI](https://huggingface.co/moka-ai) | [uniem](https://github.com/wangyuxinwhy/uniem)![Star](https://img.shields.io/github/stars/wangyuxinwhy/uniem.svg?style=social&label=Star) | 文本嵌入模型 |
| M3e-small | Small | [m3e-small](https://huggingface.co/moka-ai/m3e-small) | [Moka-AI](https://huggingface.co/moka-ai) | [uniem](https://github.com/wangyuxinwhy/uniem)![Star](https://img.shields.io/github/stars/wangyuxinwhy/uniem.svg?style=social&label=Star) | 文本嵌入模型 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### LEALLA

+ 2023 | LEALLA: Learning Lightweight Language-agnostic Sentence Embeddings with Knowledge Distillation | Zhuoyuan Mao et al. | EACL | [`PDF`](https://arxiv.org/abs/2302.08387)

| 模型         | 版本  | PyTorch                                                      | 作者            | 源地址 | 备注         |
| ------------ | ----- | ------------------------------------------------------------ | --------------- | ------ | ------------ |
| LEALLA-base  | base  | [LEALLA-base](https://huggingface.co/setu4993/LEALLA-base)   | Google Research | /      | 文本嵌入模型 |
| LEALLA-large | large | [LEALLA-large](https://huggingface.co/setu4993/LEALLA-large) | Google Research | /      | 文本嵌入模型 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## NLG系列

### GPT

+ 2019 | Improving Language Understandingby Generative Pre-Training | Alec Radford, et al. | arXiv | [`PDF`](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)

+ 2019 | Language Models are Unsupervised Multitask Learners | Alec Radford, et al. | arXiv | [`PDF`](https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf)

| 模型                | 版本      | TensorFlow                                                   | PyTorch                                                      | 作者                                                    | 源地址                                                       | 应用领域 |
| ------------------- | --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------- | ------------------------------------------------------------ | -------- |
| GPT2                | 30亿语料  |                                                              | <p>[Google Drive](https://drive.google.com/file/d/1mT_qCQg4AWnAXTwKfsyyRWCRpgPrBJS3)<br>[百度网盘-ffz6](https://pan.baidu.com/s/1yiuTHXUr2DpyBqmFYLJH6A)</p> | [Caspar ZHANG](https://github.com/imcaspar)             | [gpt2-ml](https://github.com/imcaspar/gpt2-ml)               | 通用     |
| GPT2                | 15亿语料  |                                                              | <p>[Google Drive](https://drive.google.com/file/d/1IzWpQ6I2IgfV7CldZvFJnZ9byNDZdO4n)<br>[百度网盘-q9vr](https://pan.baidu.com/s/1TA_3e-u2bXg_hcx_NwVbGw)</p> | [Caspar ZHANG](https://github.com/imcaspar)             | [gpt2-ml](https://github.com/imcaspar/gpt2-ml)               | 通用     |
| CDial-GPTLCCC-base  | base      |                                                              | [huggingface](https://huggingface.co/thu-coai/CDial-GPT_LCCC-base) | [thu-coai](https://github.com/thu-coai)                 | [CDial-GPT](https://github.com/thu-coai/CDial-GPT)           | 中文对话 |
| CDial-GPT2LCCC-base | base      |                                                              | [huggingface](https://huggingface.co/thu-coai/CDial-GPT2_LCCC-base) | [thu-coai](https://github.com/thu-coai)                 | [CDial-GPT](https://github.com/thu-coai/CDial-GPT)           | 中文对话 |
| CDial-GPTLCCC-large | large     |                                                              | [huggingface](https://huggingface.co/thu-coai/CDial-GPT_LCCC-large) | [thu-coai](https://github.com/thu-coai)                 | [CDial-GPT](https://github.com/thu-coai/CDial-GPT)           | 中文对话 |
| GPT2-dialogue       | base      |                                                              | <p>[Google Drive](https://drive.google.com/drive/folders/1Ogz3eapvtvdY4VUcY9AEwMbNRivLKhri?usp=sharing)</br>[百度网盘-osi6](https://pan.baidu.com/s/1qDZ24VKLBU9GKARX9Ev65g)</p> | [yangjianxin1](https://github.com/yangjianxin1)         | [GPT2-chitchat](https://github.com/yangjianxin1/GPT2-chitchat) | 闲聊对话 |
| GPT2-mmi            | base      |                                                              | <p>[Google Drive](https://drive.google.com/drive/folders/1oWgKXP6VG_sT_2VMrm0xL4uOqfYwzgUP?usp=sharing)</br>[百度网盘-1j88](https://pan.baidu.com/s/1ubXGuEvY8KmwEjIVTJVLww)</p> | [yangjianxin1](https://github.com/yangjianxin1)         | [GPT2-chitchat](https://github.com/yangjianxin1/GPT2-chitchat) | 闲聊对话 |
| GPT2-散文模型       | base      |                                                              | <p>[Google Drive](https://drive.google.com/drive/folders/1rJC4niJKMVwixUQkuL9k5teLRnEYTmUf?usp=sharing)</br>[百度网盘-fpyu](https://pan.baidu.com/s/1nbrW5iw34GRhoTin8uU2tQ)</p> | [Zeyao Du](https://github.com/Morizeyao)                | [GPT2-Chinese](https://github.com/Morizeyao/GPT2-Chinese)    | 散文     |
| GPT2-诗词模型       | base      |                                                              | <p>[Google Drive](https://drive.google.com/drive/folders/1Z6nF1nrgTkrZcRLHedQHXb4_M9I7yQPN?usp=sharing)</br>[百度网盘-7fev](https://pan.baidu.com/s/1Hy0OQ5xZcTLer9MQZW8o3g)</p> | [Zeyao Du](https://github.com/Morizeyao)                | [GPT2-Chinese](https://github.com/Morizeyao/GPT2-Chinese)    | 诗词     |
| GPT2-对联模型       | base      |                                                              | <p>[Google Drive](https://drive.google.com/drive/folders/1ZnsvS7oHRVueNKj_SeEhiQt86aze3ojj?usp=sharing)</br>[百度网盘-i5n0](https://pan.baidu.com/s/1j9yVQwjlXZq58wOyXK4lcg)</p> | [Zeyao Du](https://github.com/Morizeyao)                | [GPT2-Chinese](https://github.com/Morizeyao/GPT2-Chinese)    | 对联     |
| roformer-gpt        | base(L12) | [百度网盘-2nnn](https://pan.baidu.com/s/11YTnWLX0ThQr2P2yW0P7GA) |                                                              | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer)       | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GPT-3

+ 2019 | Transformer-XL: Attentive Language Models Beyond a Fixed-Length Context | Zihang Dai, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1901.02860)

+ 2020 | Language Models are Few-Shot Learners | Tom B. Brown, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2005.14165)

| 模型                   | 版本            | 介绍                                 | PyTorch                                                      | 作者                              | 源地址                                                    | 应用领域 |
| ---------------------- | --------------- | ------------------------------------ | ------------------------------------------------------------ | --------------------------------- | --------------------------------------------------------- | -------- |
| Chinese-Transformer-XL | 29亿参数(GPT-3) | [项目首页](https://gpt-3.aminer.cn/) | [模型下载](http://dorc-model-team.ks3-cn-beijing.ksyun.com/ren-zhi/my-model/mp_rank_00_model_states.pt) | [THUDM](https://github.com/THUDM) | [github](https://github.com/THUDM/Chinese-Transformer-XL) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### NEZHA-Gen

+ 2019 | NEZHA: Neural Contextualized Representation for Chinese Language Understanding | Junqiu Wei, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1909.00204)

+ 2019 | Improving Language Understandingby Generative Pre-Training | Alec Radford, et al. | arXiv | [`PDF`](https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf)

| 模型      | 版本 | TensorFlow                                                   | PyTorch | 作者                                     | 源地址                                                       | 应用领域 |
| --------- | ---- | ------------------------------------------------------------ | ------- | ---------------------------------------- | ------------------------------------------------------------ | -------- |
| NEZHA-Gen | base | <p>[Google Drive](https://drive.google.com/drive/folders/1i4f_8LhaVDNjnGlLXNJ0rNgBP0E4L6V0?usp=sharing)<br>[百度网盘-rb5m](https://pan.baidu.com/s/1Bgle8TpcxHyuUz_jAXOBWw)</p> |         | [HUAWEI](https://github.com/huawei-noah) | [github](https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/NEZHA-Gen-TensorFlow) | 通用     |
| NEZHA-Gen | base | <p>[Google Drive](https://drive.google.com/drive/folders/1B5-jxUlzhoKwFVMQ-nkqqbmJQgr1lRAp?usp=sharing)<br>[百度网盘-ytim](https://pan.baidu.com/s/1me6_BGYHbWFdTi80vRQ2Lg)</p> |         | [HUAWEI](https://github.com/huawei-noah) | [github](https://github.com/huawei-noah/Pretrained-Language-Model/tree/master/NEZHA-Gen-TensorFlow) | 诗歌     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CPM-Generate

+ 2020 | CPM: A Large-scale Generative Chinese Pre-trained Language Model | Zhengyan Zhang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2012.00413)

| 模型 | 版本     | 资源                                | PyTorch                                          | 作者                                         | 源地址                                               | 应用领域 |
| ---- | -------- | ----------------------------------- | ------------------------------------------------ | -------------------------------------------- | ---------------------------------------------------- | -------- |
| CPM  | 26亿参数 | [项目首页](https://cpm.baai.ac.cn/) | [模型下载](https://cpm.baai.ac.cn/download.html) | [Tsinghua AI](https://github.com/TsinghuaAI) | [github](https://github.com/TsinghuaAI/CPM-Generate) | 通用     |

备注: 

> PyTorch转TensorFlow可参考: [CPM-LM-TF2](https://github.com/qhduan/CPM-LM-TF2)

> PyTorch转PaddlePaddle可参考: [CPM-Generate-Paddle](https://github.com/jm12138/CPM-Generate-Paddle)

<p align="right">[<a href="#top">Back to Top</a>]</p>

### T5

+ 2019 | Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer | Colin Raffel, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1910.10683)

| 模型 | 版本  | TensorFlow                                                   | PyTorch                                                      | 作者                                    | 源地址                                 | 应用领域 |
| ---- | ----- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------------------------------------- | -------------------------------------- | -------- |
| T5   | small | [huggingface](https://huggingface.co/uer/t5-small-chinese-cluecorpussmall) | [huggingface](https://huggingface.co/uer/t5-small-chinese-cluecorpussmall) | [DBIIR @ RUC](https://github.com/dbiir) | [UER](https://github.com/dbiir/UER-py) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### T5-PEGASUS

+ 2019 | Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer | Colin Raffel, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1910.10683)

+ 2019 | PEGASUS: Pre-training with Extracted Gap-sentences for Abstractive Summarization | Jingqing Zhang, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1912.08777.pdf)

+ 2021 | T5 PEGASUS：开源一个中文生成式预训练模型 | 苏剑林. | spaces | [`Blog post`](https://spaces.ac.cn/archives/8209)

| 模型       | 版本  | Keras                                                        | PyTorch | 作者                                                    | 源地址                                                   | 应用领域 |
| ---------- | ----- | ------------------------------------------------------------ | ------- | ------------------------------------------------------- | -------------------------------------------------------- | -------- |
| T5 PEGASUS | base  | [百度网盘-3sfn](https://pan.baidu.com/s/1lQ9Dt9wZDO3IgiCL9tP-Ug) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/t5-pegasus) | 通用     |
| T5 PEGASUS | small | [百度网盘-qguk](https://pan.baidu.com/s/1bXRVWnDyAck9VfSO9_1oJQ) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/t5-pegasus) | 通用     |

>  Keras转PyTorch可参考: [t5-pegasus-pytorch](https://github.com/renmada/t5-pegasus-pytorch)

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Mengzi-T5

+ 2021 | Mengzi: Towards Lightweight yet Ingenious Pre-trained Models for Chinese | Zhuosheng Zhang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2110.06696)

| 模型      | 版本      | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                       | 应用领域 |
| --------- | --------- | ---------- | ------------------------------------------------------------ | --------------------------------------- | -------------------------------------------- | -------- |
| Mengzi-T5 | base(L12) |            | [huggingface](https://huggingface.co/Langboat/mengzi-t5-base) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### PanGu-Alpha

+ 2021 | PanGu-α: Large-scale Autoregressive Pretrained Chinese Language Models with Auto-parallel Computation | Wei Zeng, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2104.12369)

| 模型                   | 版本 | 资源                                                         | 下载地址                                                     | 作者                                                         | 源地址                                                       | 应用领域 |
| ---------------------- | ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | -------- |
| 盘古α-2.6B             | 2.6G | [项目首页](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha/src/branch/master) | [模型下载](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha/src/branch/master) | [PCL-Platform.Intelligence](https://git.openi.org.cn/PCL-Platform.Intelligence) | [github](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha) | 通用     |
| 盘古α-13B              | 12G  | [项目首页](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha/src/branch/master) | [模型下载](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha/src/branch/master) | [PCL-Platform.Intelligence](https://git.openi.org.cn/PCL-Platform.Intelligence) | [github](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha) | 通用     |
| 盘古α-2.6B pytorch版本 | 2.6G | [项目首页](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha-GPU/src/branch/master/panguAlpha_pytorch) | [模型下载](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha-GPU/src/branch/master/panguAlpha_pytorch#user-content-%E6%A8%A1%E5%9E%8B%E6%96%87%E4%BB%B6%E4%B8%8B%E8%BD%BD) | [PCL-Platform.Intelligence](https://git.openi.org.cn/PCL-Platform.Intelligence) | [github](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha-GPU) | 通用     |
| 盘古α-13B pytorch版本  | 12G  | [项目首页](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha-GPU/src/branch/master/panguAlpha_pytorch) | [模型下载](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha-GPU/src/branch/master/panguAlpha_pytorch#user-content-%E6%A8%A1%E5%9E%8B%E6%96%87%E4%BB%B6%E4%B8%8B%E8%BD%BD) | [PCL-Platform.Intelligence](https://git.openi.org.cn/PCL-Platform.Intelligence) | [github](https://git.openi.org.cn/PCL-Platform.Intelligence/PanGu-Alpha-GPU) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### EVA

+ 2021 | EVA: An Open-Domain Chinese Dialogue System with Large-Scale Generative Pre-Training | Hao Zhou, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2108.01547)

| 模型          | 版本     | 介绍                                            | 模型下载                                                     | 作者                                    | 源地址                                    | 应用领域       | 备注             |
| ------------- | -------- | ----------------------------------------------- | ------------------------------------------------------------ | --------------------------------------- | ----------------------------------------- | -------------- | ---------------- |
| EVA           | 28亿参数 | [项目首页](https://wudaoai.cn/model/detail/EVA) | [模型下载](https://wudaoai.cn/model/download?resourceId=1428554651225075712&filename=eva-ckpt.tar.gz) | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 | 需要登陆才能下载 |
| EVA2.0-xLarge | xlarge   | [项目首页](https://wudaoai.cn/model/detail/EVA) | [huggingface](https://huggingface.co/thu-coai/EVA2.0-xlarge) | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 |                  |
| EVA2.0-large  | large    | [项目首页](https://wudaoai.cn/model/detail/EVA) | [huggingface](https://huggingface.co/thu-coai/EVA2.0-large)  | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 |                  |
| EVA2.0-base   | base     | [项目首页](https://wudaoai.cn/model/detail/EVA) | [huggingface](https://huggingface.co/thu-coai/EVA2.0-base)   | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 |                  |

<p align="right">[<a href="#top">Back to Top</a>]</p>-

### BART

+ 2019 | BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension | Mike Lewis, et al. | arxiv | [`PDF`](https://arxiv.org/abs/1910.13461)

| 模型       | 版本  | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                   | 应用领域 |
| ---------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ---------------------------------------- | -------- |
| BART-base  | base  |            | [huggingface](https://huggingface.co/fnlp/bart-base-chinese) | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 中文通用 |
| BART-large | large |            | [huggingface](https://huggingface.co/fnlp/bart-large-chinese) | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 闻仲

| 模型     | 版本       | 类型 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域 |
| -------- | ---------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | -------- |
| Wenzhong | large(L24) | GPT2 |            | [huggingface](https://huggingface.co/IDEA-CCNL/Wenzhong-3.5B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 余元

| 模型   | 版本       | 类型 | TensorFlow | PyTorch                                                     | 作者                                      | 源地址                                                 | 应用领域 |
| ------ | ---------- | ---- | ---------- | ----------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------ | -------- |
| Yuyuan | large(L24) | GPT2 |            | [huggingface](https://huggingface.co/IDEA-CCNL/Yuyuan-3.5B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 医学领域 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RWKV

+ 2021 | An Attention Free Transformer | Shuangfei Zhai, et al. | arxiv | [`PDF`](https://arxiv.org/abs/2105.14103)
+ 2022 | The RWKV Language Model . | [github](https://github.com/BlinkDL/RWKV-LM)

| 模型 | 版本      | 类型 | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                         | 应用领域 |
| ---- | --------- | ---- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ---------------------------------------------- | -------- |
| RWKV | base(L12) |      |            | [github](https://github.com/BlinkDL/AI-Writer/releases)      | [PENG Bo](https://github.com/BlinkDL) | [github](https://github.com/BlinkDL/AI-Writer) | 小说     |
| RWKV | 7B        |      |            | [huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-7b) | [PENG Bo](https://github.com/BlinkDL) | [github](https://github.com/BlinkDL/ChatRWKV)  | 小说     |
| RWKV | 14B       |      |            | [huggingface](https://huggingface.co/BlinkDL/rwkv-4-pile-7b/tree/main) | [PENG Bo](https://github.com/BlinkDL) | [github](https://github.com/BlinkDL/ChatRWKV)  | 小说     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### PromptCLUE

| 模型             | 版本      | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                          | 应用领域 |
| ---------------- | --------- | ---------- | ------------------------------------------------------------ | --------------------------------------- | ----------------------------------------------- | -------- |
| PromptCLUE       | base(L12) |            | [huggingface](https://huggingface.co/ClueAI/PromptCLUE-base) | [ClueAI](https://huggingface.co/ClueAI) | [github](https://github.com/clue-ai/PromptCLUE) | 通用     |
| PromptCLUE-v1-5  | base(L12) |            | [huggingface](https://huggingface.co/ClueAI/PromptCLUE-base-v1-5) | [ClueAI](https://huggingface.co/ClueAI) | [github](https://github.com/clue-ai/PromptCLUE) | 通用     |
| PromptCLUE-large | large     |            | [API在线调用](https://www.clueai.cn/)                        | [ClueAI](https://huggingface.co/ClueAI) | [github](https://github.com/clue-ai/PromptCLUE) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ChatYuan

| 模型              | 版本  | 类型 | TensorFlow | PyTorch                                                      | 作者                                 | 源地址                                        | 应用领域   |
| ----------------- | ----- | ---- | ---------- | ------------------------------------------------------------ | ------------------------------------ | --------------------------------------------- | ---------- |
| ChatYuan          | large | T5   |            | [huggingface](https://huggingface.co/ClueAI/ChatYuan-large-v1) | [ClueAI](https://github.com/clue-ai) | [github](https://github.com/clue-ai/ChatYuan) | 功能型对话 |
| ChatYuan-large-v2 | large | T5   |            | [huggingface](https://huggingface.co/ClueAI/ChatYuan-large-v2) | [ClueAI](https://github.com/clue-ai) | [github](https://github.com/clue-ai/ChatYuan) | 功能型对话 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### SkyText

| 模型    | 版本  | 类型 | TensorFlow | PyTorch                                               | 作者                                          | 源地址                                                   | 应用领域 |
| ------- | ----- | ---- | ---------- | ----------------------------------------------------- | --------------------------------------------- | -------------------------------------------------------- | -------- |
| SkyText | large | GPT3 |            | [huggingface](https://huggingface.co/SkyWork/SkyText) | [SkyWorkAIGC](https://github.com/SkyWorkAIGC) | [github](https://github.com/SkyWorkAIGC/SkyText-CN-GPT3) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ProphetNet

+ 2020 | Prophetnet: Predicting future n-gram for sequence-to-sequence pre-training | Qi, Weizhen, et al. | arxiv | [`PDF`](https://arxiv.org/pdf/2001.04063.pdf)
+ 2021 | ProphetNet-X: Large-Scale Pre-training Models for English, Chinese, Multi-lingual, Dialog, and Code Generation | Qi, Weizhen, et al. | arxiv | [`PDF`](https://arxiv.org/abs/2104.08006)

| 模型                 | 版本 | 类型 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                       | 应用领域 |
| -------------------- | ---- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ | -------- |
| ProphetNet-Zh        |      |      |            | [link](https://msraprophetnet.blob.core.windows.net/prophetnet/release_checkpoints/prophetnet_zh.pt) | [microsoft](https://github.com/microsoft) | [github](https://github.com/microsoft/ProphetNet/tree/master/ProphetNet) | 通用     |
| ProphetNet-Dialog-Zh |      |      |            | [link](https://msraprophetnet.blob.core.windows.net/prophetnet/release_checkpoints/prophetnet_dialog_zh.pt) | [microsoft](https://github.com/microsoft) | [github](https://github.com/microsoft/ProphetNet/tree/master/ProphetNet) | 对话     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## NLU-NLG系列

### UniLM

+ 2019 | Unified Language Model Pre-training for Natural Language Understanding and Generation | Li Dong, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1905.03197)

| 模型  | 版本 | TensorFlow                                                   | PyTorch                                                      | 作者                                                    | 源地址                                              | 应用领域 |
| ----- | ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------- | --------------------------------------------------- | -------- |
| Unilm | base | [百度网盘-tblr](https://pan.baidu.com/s/1HgxIkBl5Yfwrzs1K1B6NFA) | [百度网盘-etwf](https://pan.baidu.com/s/1DHJGOFJ5cce5N5g4aBDiMQ) | [YunwenTechnology](https://github.com/YunwenTechnology) | [github](https://github.com/YunwenTechnology/Unilm) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Simbert 

+ 2020 | 鱼与熊掌兼得：融合检索和生成的SimBERT模型 | 苏剑林. | spaces | [`Blog post`](https://kexue.fm/archives/7427)

| 模型          | 版本  | TensorFlow                                                   | PyTorch | 作者                                                    | 源地址                                                       | 应用领域 |
| ------------- | ----- | ------------------------------------------------------------ | ------- | ------------------------------------------------------- | ------------------------------------------------------------ | -------- |
| SimBERT Tiny  | tiny  | [百度网盘-1tp7](https://pan.baidu.com/s/1z_agqTuBTuyHANwrS-gPcg) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/pretrained-models) | 通用     |
| SimBERT Small | small | [百度网盘-nu67](https://pan.baidu.com/s/1kq_EQDI0gpiZBLFd_AxwrA) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/pretrained-models) | 通用     |
| SimBERT Base  | base  | [百度网盘-6xhq](https://pan.baidu.com/s/1uGfQmX1Kxcv_cXTVsvxTsQ) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/pretrained-models) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RoFormer-sim

+ 2021 | SimBERTv2来了！融合检索和生成的RoFormer-Sim模型 | 苏剑林. | spaces | [`Blog post`](https://kexue.fm/archives/8454)

| 模型            | 版本      | TensorFlow                                                   | PyTorch | 作者                                                    | 源地址                                                     | 应用领域 |
| --------------- | --------- | ------------------------------------------------------------ | ------- | ------------------------------------------------------- | ---------------------------------------------------------- | -------- |
| roformer-sim    | base(L12) | [百度网盘-2cgz](https://pan.baidu.com/s/1f1FB288nv1a6jYjsNCordg) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer-sim) | 通用     |
| roformer-sim    | small(L6) | [百度网盘-h68q](https://pan.baidu.com/s/1r0eJ7shGwQ0RzV9BTFFW4g) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer-sim) | 通用     |
| roformer-sim-v2 | base(L12) | [百度网盘-w15n](https://pan.baidu.com/s/1Igh3tSvSu_ahDZmGaOlVoA) |         | [ZhuiyiTechnology](https://github.com/ZhuiyiTechnology) | [github](https://github.com/ZhuiyiTechnology/roformer-sim) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 周文王

| 模型        | 版本       | 类型     | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域 |
| ----------- | ---------- | -------- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | -------- |
| Zhouwenwang | base(L12)  | roformer |            | [huggingface](https://huggingface.co/IDEA-CCNL/Zhouwenwang-110M) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |
| Zhouwenwang | large(L24) | roformer |            | [huggingface](https://huggingface.co/IDEA-CCNL/Zhouwenwang-1.3B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CPM-2

+ 2021 | CPM-2: Large-scale Cost-effective Pre-trained Language Models | Zhengyan Zhang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2106.10715)

| 模型  | 版本       | 介绍                                | 模型下载                                                     | 作者                                        | 源地址                                        | 应用领域 | 备注             |
| ----- | ---------- | ----------------------------------- | ------------------------------------------------------------ | ------------------------------------------- | --------------------------------------------- | -------- | ---------------- |
| CPM-2 | 110亿参数  | [项目首页](https://wudaoai.cn/home) | [模型下载](https://resource.wudaoai.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [BAAI-WuDao](https://github.com/BAAI-WuDao) | [github](https://github.com/BAAI-WuDao/Model) | 通用     | 需要申请才能下载 |
| CPM-2 | 100亿参数  | [项目首页](https://wudaoai.cn/home) | [模型下载](https://resource.wudaoai.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [BAAI-WuDao](https://github.com/BAAI-WuDao) | [github](https://github.com/BAAI-WuDao/Model) | 中英     | 需要申请才能下载 |
| CPM-2 | 1980亿参数 | [项目首页](https://wudaoai.cn/home) | [模型下载](https://resource.wudaoai.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [BAAI-WuDao](https://github.com/BAAI-WuDao) | [github](https://github.com/BAAI-WuDao/Model) | 中英     | 需要申请才能下载 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CPT

+ 2021 | CPT: A Pre-Trained Unbalanced Transformer for Both Chinese Language Understanding and Generation | Yunfan Shao, et al. | arxiv | [`PDF`](https://arxiv.org/pdf/2109.05729.pdf)

| 模型      | 版本       | TensorFlow | PyTorch                                              | 作者                                  | 源地址                                   | 应用领域 |
| --------- | ---------- | ---------- | ---------------------------------------------------- | ------------------------------------- | ---------------------------------------- | -------- |
| CPT-base  | base(L12)  |            | [huggingface](https://huggingface.co/fnlp/cpt-base)  | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 通用     |
| CPT-large | large(L24) |            | [huggingface](https://huggingface.co/fnlp/cpt-large) | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GLM

+ 2022 | GLM: General Language Model Pretraining with Autoregressive Blank Infilling | Zhengxiao Du, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2103.10360)
+ 2022 | GLM-130B: An Open Bilingual Pre-trained Model | Aohan Zeng, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2210.02414)

| 模型     | 版本    | TensorFlow | PyTorch                                                      | 作者                                        | 源地址                                      | 应用领域 |
| -------- | ------- | ---------- | ------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------- | -------- |
| GLM      | large   |            | [Huggingface](https://huggingface.co/BAAI/glm-large-chinese) | [THUDM](https://github.com/THUDM)           | [github](https://github.com/THUDM/glm)      | 通用     |
| GLM      | xxlarge |            | [Huggingface](https://huggingface.co/BAAI/glm-10b-chinese)   | [THUDM](https://github.com/THUDM)           | [github](https://github.com/THUDM/glm)      | 通用     |
| GLM-130B | 130B    |            | [申请地址1](https://models.aminer.cn/glm/zh-CN/download/GLM-130B)[申请地址2](https://docs.google.com/forms/d/e/1FAIpQLSehr5Dh_i3TwACmFFi8QEgIVNYGmSPwV0GueIcsUev0NEfUug/viewform) | [THUDM](https://models.aminer.cn/glm-130b/) | [github](https://github.com/THUDM/GLM-130B) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### PLUG

+ 2019 | StructBERT: Incorporating Language Structures into Pre-training for Deep Language Understanding | Wei Wang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1908.04577)
+ 2020 | PALM: Pre-training an Autoencoding&Autoregressive Language Model for Context-conditioned Generation | Bin Bi, et al. | ACL| [`PDF`](https://aclanthology.org/2020.emnlp-main.700/)

| 模型 | 版本 | 模型下载                                                  | 作者                                  | 源地址                                                       | 应用领域 |
| ---- | ---- | --------------------------------------------------------- | ------------------------------------- | ------------------------------------------------------------ | -------- |
| PLUG | 27B  | [AliceMind-需要申请](https://www.alice-mind.com/portal#/) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/StructBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### OPD

+ 2022 | 待定 | , et al. | arXiv | [`PDF`]()

| 模型 | 版本 | 介绍                                                   | 模型下载                                               | 作者                                    | 源地址                                    | 应用领域       | 备注             |
| ---- | ---- | ------------------------------------------------------ | ------------------------------------------------------ | --------------------------------------- | ----------------------------------------- | -------------- | ---------------- |
| OPD  | 6.3B | [项目首页](http://coai.cs.tsinghua.edu.cn/static/opd/) | [模型下载](http://coai.cs.tsinghua.edu.cn/static/opd/) | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/OPD) | 中文开放域对话 | 需要申请才能下载 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## Multi-Modal

### WenLan

+ 2021 | WenLan: Bridging Vision and Language by Large-Scale Multi-Modal Pre-Training | Yuqi Huo, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2103.06561)

| 模型          | 版本     | 介绍                                              | 模型下载                                                     | 作者                                        | 源地址                                         | 应用领域     | 备注             |
| ------------- | -------- | ------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------- | ---------------------------------------------- | ------------ | ---------------- |
| BriVL(WenLan) | 10亿参数 | [项目首页](https://wudaoai.cn/model/detail/BriVL) | [模型下载](https://wudaoai.cn/model/download?resourceId=1425655534320660480&filename=BriVL-1.0-1B-zh.tar) | [BAAI-WuDao](https://github.com/BAAI-WuDao) | [github](https://github.com/BAAI-WuDao/BriVlL) | 中文通用图文 | 需要登陆才能下载 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CogView

+ 2021 | CogView: Mastering Text-to-Image Generation via Transformers | Ming Ding, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2105.13290.pdf)

| 模型    | 版本     | 介绍                                                | 模型下载                                            | 作者                               | 源地址                                     | 应用领域           | 备注             |
| ------- | -------- | --------------------------------------------------- | --------------------------------------------------- | ---------------------------------- | ------------------------------------------ | ------------------ | ---------------- |
| CogView | 40亿参数 | [项目首页](https://wudaoai.cn/model/detail/CogView) | [模型下载](https://wudaoai.cn/model/detail/CogView) | [THUDM ](https://github.com/THUDM) | [github](https://github.com/THUDM/CogView) | 中文多模态生成模型 | 需要登陆才能下载 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 紫东太初


| 模型                        | 版本     | 介绍                                                         | 模型下载                                                     | 作者                                             | 源地址                                                      | 应用领域          | 备注                                             |
| --------------------------- | -------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------ | ----------------------------------------------------------- | ----------------- | ------------------------------------------------ |
| 紫东太初- light_vision_text |          | [项目首页](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/light_vision_text) | [模型下载](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/light_vision_text) | [中科院自动化所](https://gitee.com/zidongtaichu) | [github](https://gitee.com/zidongtaichu/multi-modal-models) | 中文图像-文本领域 | 紫东太初多模态大模型中的图像-文本预训练模型      |
| 紫东太初-text[GPT]          | 32亿参数 | [项目首页](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/text) | [百度网盘-nos5](https://pan.baidu.com/s/1Wsu5OVlQBNai24NhNiaqRw) | [中科院自动化所](https://gitee.com/zidongtaichu) | [github](https://gitee.com/zidongtaichu/multi-modal-models) | 中文通用          | 紫东太初多模态大模型中的文本预训练模型           |
| 紫东太初-vision             |          | [项目首页](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/vision) | [模型下载](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/vision) | [中科院自动化所](https://gitee.com/zidongtaichu) | [github](https://gitee.com/zidongtaichu/multi-modal-models) | 视觉领域          | 紫东太初多模态大模型中的视觉预训练模型           |
| 紫东太初-speech             |          | [项目首页](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/speech) | [模型下载](https://gitee.com/zidongtaichu/multi-modal-models/tree/master/speech) | [中科院自动化所](https://gitee.com/zidongtaichu) | [github](https://gitee.com/zidongtaichu/multi-modal-models) | 语音领域          | 紫东太初多模态大模型中的语音检测与识别多任务模型 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Mengzi-oscar

+ 2021 | Mengzi: Towards Lightweight yet Ingenious Pre-trained Models for Chinese | Zhuosheng Zhang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2110.06696)

| 模型         | 版本      | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                       | 应用领域        |
| ------------ | --------- | ---------- | ------------------------------------------------------------ | --------------------------------------- | -------------------------------------------- | --------------- |
| Mengzi-oscar | base(L12) |            | [huggingface](https://huggingface.co/Langboat/mengzi-oscar-base) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### R2D2

+ 2022 | Zero and R2D2: A Large-scale Chinese Cross-modal Benchmark and A Vision-Language Framework | Chunyu Xie, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2205.03860)

| 模型      | 版本  | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                    | 首页                         | 应用领域        |
| --------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ----------------------------------------- | ---------------------------- | --------------- |
| R2D2ViT-L | large |            | [Google](https://drive.google.com/file/d/18Fd3vGvj0Dz8rPlxROxugjZaF8Z4jf7g/view) | [yuxie11](https://github.com/yuxie11) | [github](https://github.com/yuxie11/R2D2) | [zero](https://zero.so.com/) | 中文多模态-图文 |
| PRD2ViT-L | large |            | [Google](https://drive.google.com/file/d/15zDdam7_-YT0suA3Wc226vvxcyBxWZ_O/view?usp=sharing) | [yuxie11](https://github.com/yuxie11) | [github](https://github.com/yuxie11/R2D2) | [zero](https://zero.so.com/) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Chinese-CLIP

+ 2021 | Learning Transferable Visual Models From Natural Language Supervision | Alec Radford, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2103.00020)
+ 2022 | Chinese CLIP: Contrastive Vision-Language Pretraining in Chinese | An Yang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.01335)

| 模型                             | 版本 | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                            | 应用领域        |
| -------------------------------- | ---- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ------------------------------------------------- | --------------- |
| CN-CLIP<sub>RN50</sub>           | 77M  |            | [aliyuncs](https://clip-cn-beijing.oss-cn-beijing.aliyuncs.com/checkpoints/clip_cn_rn50.pt) | [OFA-Sys](https://github.com/OFA-Sys) | [github](https://github.com/OFA-Sys/Chinese-CLIP) | 中文多模态-图文 |
| CN-CLIP<sub>ViT-B/16</sub>       | 188M |            | [aliyuncs](https://clip-cn-beijing.oss-cn-beijing.aliyuncs.com/checkpoints/clip_cn_vit-b-16.pt) | [OFA-Sys](https://github.com/OFA-Sys) | [github](https://github.com/OFA-Sys/Chinese-CLIP) | 中文多模态-图文 |
| CN-CLIP<sub>ViT-L/14</sub>       | 406M |            | [aliyuncs](https://clip-cn-beijing.oss-cn-beijing.aliyuncs.com/checkpoints/clip_cn_vit-l-14.pt) | [OFA-Sys](https://github.com/OFA-Sys) | [github](https://github.com/OFA-Sys/Chinese-CLIP) | 中文多模态-图文 |
| CN-CLIP<sub>ViT-L/14@336px</sub> | 407M |            | [aliyuncs](https://clip-cn-beijing.oss-cn-beijing.aliyuncs.com/checkpoints/clip_cn_vit-l-14-336.pt) | [OFA-Sys](https://github.com/OFA-Sys) | [github](https://github.com/OFA-Sys/Chinese-CLIP) | 中文多模态-图文 |
| CN-CLIP<sub>ViT-H/14</sub>       | 958M |            | [aliyuncs](https://clip-cn-beijing.oss-cn-beijing.aliyuncs.com/checkpoints/clip_cn_vit-h-14.pt) | [OFA-Sys](https://github.com/OFA-Sys) | [github](https://github.com/OFA-Sys/Chinese-CLIP) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### TaiYi-CLIP

+ 2021 | Learning Transferable Visual Models From Natural Language Supervision | Alec Radford, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2103.00020)
+ 2022 | Fengshenbang 1.0: Being the Foundation of Chinese Cognitive Intelligence | Junjie Wang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2209.02970)

| 模型                                  | 版本 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域        |
| ------------------------------------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | --------------- |
| Taiyi-CLIP-Roberta-large-326M-Chinese | base |            | [huggingface](https://huggingface.co/IDEA-CCNL/Taiyi-CLIP-Roberta-large-326M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### AltCLIP

+ 2022 | AltCLIP: Altering the Language Encoder in CLIP for Extended Language Capabilities | Chen, Zhongzhi, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.06679)

| 模型    | 版本  | TensorFlow | PyTorch                                            | 作者                                     | 源地址                                                       | 应用领域        |
| ------- | ----- | ---------- | -------------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| AltCLIP | 3.22G |            | [huggingface](https://huggingface.co/BAAI/AltCLIP) | [FlagAI](https://github.com/FlagAI-Open) | [github](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/AltCLIP) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### AltDiffusion

+ 2022 | AltCLIP: Altering the Language Encoder in CLIP for Extended Language Capabilities | Chen, Zhongzhi, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.06679)
+ 2022 | High-Resolution Image Synthesis With Latent Diffusion Models | Rombach, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2112.10752)

| 模型         | 版本 | TensorFlow | PyTorch                                                 | 作者                                     | 源地址                                                       | 应用领域        |
| ------------ | ---- | ---------- | ------------------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| AltDiffusion | 8.0G |            | [huggingface](https://huggingface.co/BAAI/AltDiffusion) | [FlagAI](https://github.com/FlagAI-Open) | [github](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/AltDiffusion) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Taiyi-Stable-Diffusion

+ 2022 | Fengshenbang 1.0: Being the Foundation of Chinese Cognitive Intelligence | Junjie Wang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2209.02970)
+ 2022 | High-Resolution Image Synthesis With Latent Diffusion Models | Rombach, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2112.10752)

| 模型                   | 版本 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域        |
| ---------------------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | --------------- |
| Taiyi-Stable-Diffusion | 1B   |            | [huggingface](https://huggingface.co/IDEA-CCNL/Taiyi-Stable-Diffusion-1B-Chinese-v0.1) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### wukong

+ 2022 | Wukong: A 100 Million Large-scale Chinese Cross-modal Pre-training Benchmark | Jiaxi Gu, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2202.06767)

| 模型   | 版本 | TensorFlow | PyTorch                                                      | 作者                                     | 源地址                                                       | 应用领域        |
| ------ | ---- | ---------- | ------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| CLIP   |      |            | [url](https://wukong-dataset.github.io/wukong-dataset/benchmark.html) | [HUAWEI](https://github.com/huawei-noah) | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 中文多模态-图文 |
| FILIP  |      |            | [url](https://wukong-dataset.github.io/wukong-dataset/benchmark.html) | [HUAWEI](https://github.com/huawei-noah) | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 中文多模态-图文 |
| wukong |      |            | [url](https://wukong-dataset.github.io/wukong-dataset/benchmark.html) | [HUAWEI](https://github.com/huawei-noah) | [github](https://github.com/huawei-noah/Pretrained-Language-Model) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### OFA

+ 2022 | OFA: Unifying Architectures, Tasks, and Modalities Through a Simple Sequence-to-Sequence Learning Framework | Peng Wang, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2202.03052.pdf)

| 模型        | 版本 | TensorFlow | PyTorch                                                      | 作者                                            | 源地址                                                | 应用领域        |
| ----------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------------- | ----------------------------------------------------- | --------------- |
| OFA         |      |            | [link](https://github.com/OFA-Sys/OFA/blob/main/checkpoints_cn.md) | [OFA-Sys](https://github.com/OFA-Sys)           | [github](https://github.com/OFA-Sys/OFA)              | 中文多模态-图文 |
| OFA-Chinese |      |            | [Huggingface](https://huggingface.co/YeungNLP/ofa-cn-base-muge-v2) | [Yang JianXin](https://github.com/yangjianxin1) | [github](https://github.com/yangjianxin1/OFA-Chinese) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### QA-CLIP

| 模型            | 版本 | 视觉架构 | PyTorch                                                      | 作者                                     | 源地址                                                       | 应用领域        |
| --------------- | ---- | -------- | ------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| QA-CLIPRN50     | 77M  | ResNet50 | [ckpt](https://huggingface.co/TencentARC/QA-CLIP/resolve/main/QA-CLIP-RN50.pt) | [腾讯](https://github.com/TencentARC-QQ) | [QA-CLIP](https://github.com/TencentARC-QQ/QA-CLIP)![Star](https://img.shields.io/github/stars/TencentARC-QQ/QA-CLIP.svg?style=social&label=Star) | 中文多模态-图文 |
| QA-CLIPViT-B/16 | 188M | ViT-B/16 | [ckpt](https://huggingface.co/TencentARC/QA-CLIP/resolve/main/QA-CLIP-base.pt) | [腾讯](https://github.com/TencentARC-QQ) | [QA-CLIP](https://github.com/TencentARC-QQ/QA-CLIP)![Star](https://img.shields.io/github/stars/TencentARC-QQ/QA-CLIP.svg?style=social&label=Star) | 中文多模态-图文 |
| QA-CLIPViT-L/14 | 406M | ViT-L/14 | [ckpt](https://huggingface.co/TencentARC/QA-CLIP/resolve/main/QA-CLIP-large.pt) | [腾讯](https://github.com/TencentARC-QQ) | [QA-CLIP](https://github.com/TencentARC-QQ/QA-CLIP)![Star](https://img.shields.io/github/stars/TencentARC-QQ/QA-CLIP.svg?style=social&label=Star) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## Table

### SDCUP

+ 2021 | Improving Text-to-SQL with Schema Dependency Learning | Binyuan Hui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2103.04399)

| 模型  | 版本  | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                                       | 应用领域 |
| ----- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ------------------------------------------------------------ | -------- |
| sdcup | base  |            | [阿里云](http://alice-open.oss-cn-zhangjiakou.aliyuncs.com/SDCUP/sdcup_base_model.bin-50000) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/SDCUP) | 中文表格 |
| sdcup | large |            | [阿里云](http://alice-open.oss-cn-zhangjiakou.aliyuncs.com/SDCUP/sdcup_large_model.bin-60000) | [Alibaba](https://github.com/alibaba) | [github](https://github.com/alibaba/AliceMind/tree/main/SDCUP) | 中文表格 |

<p align="right">[<a href="#top">Back to Top</a>]</p>


## 更新

* 2023.06.26  增加[CoLLaMA](#ChatLLM),CoLLaMA是基于代码的多语言大模型。
* 2023.06.25 增加[ChatGLM2-6B](#ChatLLM),ChatGLM2-6B 是开源中英双语对话模型 ChatGLM-6B 的第二代版本。
* 2023.06.24 增加[TechGPT](#ChatLLM),TechGPT是“东北大学知识图谱研究组”发布的垂直领域大语言模型。
* 2023.06.20 增加[Yayi、BayLing](#ChatLLM),百聆（BayLing）是一个强化了语言对齐的指令跟随大规模语言模型;Yayi大模型 在百万级人工构造的高质量领域数据上进行指令微调得到，训练数据覆盖媒体宣传、舆情分析、公共安全、金融风控、城市治理等五大领域。
* 2023.06.19 增加[panda](#ChatLLM),Panda是海外中文开源大语言模型。
* 2023.06.18 增加[ZhiXi](#ChatLLM),ZhiXi基于Llama的针对知识抽取的大模型。
* 2023.06.15 增加[Baichuan-7B](#LLM),baichuan-7B是由百川智能开发的一个开源可商用的大规模预训练语言模型。
* 2023.06.14 增加[Chinese-Falcon](#LLM),Chinese-Falcon 模型在 Falcon 基础上扩充中文词表，在中英文数据上增量预训练。 模型以 Apache License 2.0 协议开源，支持商业用途。。
* 2023.06.13 增加[OpenLLaMA-Chinese](#ChatLLM),OpenLLaMA-Chinese是免费的中文大型语言模型，基于OpenLLaMA，可用于非商业和商业目的。
* 2023.06.09 增加[QA-CLIP](#QA-CLIP),[M3E](#M3E),[Aquila](#LLM),QA-CLIP是中文CLIP模型,M3E是文本嵌入模型,Aquila是语言大模型。
* 2023.06.08 增加[YuLan](#ChatLLM),YuLan是由中国人名大学开源的双语言任务大模型,开源13B和65B大小。
* 2023.06.08 增加[Chinese-Alpaca-33B](#ChatLLM),[Chinese-LLaMA-33B](#LLM)，中文LLaMA/Alpaca-33B。
* 2023.06.07 增加[Tigerbot](#ChatLLM),TigerBot是一款国产自研的多语言任务大模型,开源7B和180B大小。
* 2023.06.06 增加[Video-LLaMA](#MultiModal-ChatLLM),[BiLLa](#ChatLLM),Video-LLaMA是一个用于视频理解的指令调整的视觉语言模型，BiLLa是开源的推理能力增强的中英双语LLaMA模型。
* 2023.05.26 增加[XuanYuan](#ChatLLM),[XrayGLM](#MultiModal-ChatLLM),XuanYuan是国内首个开源的千亿级中文对话大模型,XrayGLM是中文医学领域多模态大语言模型。
* 2023.05.21 增加[ziya,BLOOMChat](#ChatLLM),Ziya-LLaMA-13B-v1拥有130亿参数，从LLaMA-13B开始重新构建中文词表，进行千亿token量级的已知的最大规模继续预训练，使模型具备原生中文能力.
* 2023.05.18 增加[VisualGLM-6B](#MultiModal-ChatLLM),VisualGLM-6B 是一个开源的，支持图像、中文和英文的多模态对话语言模型。
* 2023.05.16 增加[BiLLa](#ChatLLM),开源中英文双语大模型。
* 2023.05.12 增加[Bactrian-X](#ChatLLM),开源多语言大模型。
* 2023.05.08 增加[OpenBuddy](#ChatLLM),一款强大的开源多语言聊天机器人模型。
* 2023.04.26 更新[LLaMA-zh、YuYan](#LLM),增加LLama-zh、Yuyan、扁鹊等LLM和chatLLm模型
* 2023.04.25 增加[BBT](#LLM)，基于Transformer和Decoder-Only的架构开发了BigBang Transformer「乾元」大规模预训练语言模型。
* 2023.04.21 增加[MOSS](#ChatLLM),更新复旦大学开源的MOSS模型以及对应的数据集。
* 2023.04.20 增加[Phoenix](#ChatLLM),基于BLOOMZ-mt模型微调得到的大语言模型。
* 2023.04.19 增加[ChatPLUG](#ChatLLM)，该模型基于PLUG，使用亿级互联网社交数据、百科数据预训练和百万级高质量对话数据进行instruction微调得到。
* 2023.04.18 增加[COIG](#中文指令数据集)数据集，用不同方法构建中文指令数据集的项目，收集了大约20万个中文指令样本。
* 2023.04.13 更新[ChatLLM](#ChatLLM)，增加HuaTuo,Med_ChatGLM两个医学模型。
* 2023.04.09 更新[中文指令数据集](#中文指令数据集)[ChatLLM](#ChatLLM)，增加个性角色对话数据集、chinese-alpaca-13b模型。
* 2023.04.03 更新[中文指令数据集](#中文指令数据集)[ChatLLM](#ChatLLM)，增加BELLE-13b模型，math-0.25，multiturn-0.8数据集。
* 2023.04.02 更新[ChatLLM](#ChatLLM)列表，增加由香港科技大学开源的7B/13B/33B/65B中文大型语言模型
* 2023.03.30 增加Chinese-Vicuna模型，Traditional-Chinese-alpaca数据集
* 2023.03.29 增加[OFA](#OFA),中文多模态统一预训练模型,OFA是阿里巴巴发布的多模态统一预训练模型.
* 2023.03.29 更新[中文指令数据集](#中文指令数据集)，增加InstructionWild数据集。
* 2023.03.23 增加[中文指令数据集](#中文指令数据集)，并初始化三个已公开数据集。
* 2023.03.20 增加[BELLE](#ChatLLM),开源中文对话大模型-70亿参数,基于Stanford Alpaca，对中文做了优化，模型调优仅使用由ChatGPT生产的数据.
* 2023.03.14 增加[ChatLLM](#ChatLLM)列表，主要收集具备问答跟对话等功能的大型语言模型,并增加ChatGLM模型。
* 2023.03.11 增加[ProphetNet](#ProphetNet),提出了一种新的自监督学习目标——同时预测多个未来字符，在序列到序列的多个自然语言生成任务都取得了优异性能。
* 2023.03.10 增加[RoCBert](#RoCBert),利用对抗学习生成更多噪声数据，用来进行中文BERT模型的训练，得到鲁棒性更强的中文BERT模型。
* 2023.03.03 更新[LLM](#LLM),新增多语言模型`Flan-ul2`和`Flan-t5-xxl`
* 2023.02.21 增加[LLM](#LLM),大规模语言模型列表，只罗列出参数量大于10B以上模型，其余量级模型，可参考对应的项目地址。
* 2023.01.14 增加[SkyText](#SkyText),SkyText是由奇点智源发布的中文GPT3预训练大模型，可以进行聊天、问答、中英互译等不同的任务.
* 2023.01.14 增加[ChatYuan](#ChatYuan),ChatYuan模型可以用于问答、结合上下文做对话、做各种生成任务，包括创意性写作，也能回答一些像法律、新冠等领域问题。
* 2022.12.10 增加[PromptCLUE](#PromptCLUE),全中文任务零样本学习模型,基于1000亿token中文语料上预训练，并且在数百种任务上进行Prompt任务式训练。
* 2022.12.01 增加[wukong](#wukong),基于一个名为「悟空」的大型中文跨模态数据集，其中包含来自网络的 1 亿个图文对，预训练的多模态模型。
* 2022.11.30 增加[AltDiffusion](#AltDiffusion)，使用 AltCLIP 作为text encoder，基于 Stable Diffusion 训练了中英双语Diffusion模型(AltDiffusion)
* 2022.11.30 增加[AltCLIP](#AltCLIP),一个简单高效的方法去训练更加优秀的双语CLIP模型,名为AltCLIP。AltCLIP基于 OpenAI CLIP 训练。
* 2022.11.30 增加[Taiyi-Stable-Diffusion](#Taiyi-Stable-Diffusion),首个开源的中英双语Stable Diffusion模型，基于0.2亿筛选过的中文图文对训练。
* 2022.11.9 增加[OPD](#OPD),OPD是一个中文开放域对话预训练模型，拥有63亿参数，在70GB高质量对话数据上进行训练而成.`大规模` & `高性能`
* 2022.11.8 更新[Chinese-CLIP](#Chinese-CLIP),Chinese-CLIP是中文多模态图文表征模型，更新后Chinese-CLIP扩充到5个模型规模，同时增加了技术报告论文以及检索demo，同时在达摩院ModelScope平台同步集成。
* 2022.10.31 增加[LERT](#LERT),为了验证通过显式注入语言学知识预训练模型能否获得进一步性能提升，HFL提出了一种**语言学信息增强的预训练模型LERT**，融合了多种语言学知识。大量实验结果表明，在同等训练数据规模下，LERT能够带来显著性能提升。
* 2022.10.14 增加[CKBERT](#CKBERT)，中文知识库增强BERT预训练语言模型。
* 2022.10.01 增加[GlyphBERT](#GlyphBERT), GlyphBERT是一个包含了汉字字形特征中文预训练模型。它通过将输入的字符渲染成图像并设计成多通道位置特征图的形式，并设计了一个两层 残差卷积神经网络模块来提取字符的图像特征进行训练。
* 2022.09.30 增加[DeBERTa](#DeBERTa)，一个中文版的DeBERTa-v2，我们用悟道语料库(180G版本)进行预训练，在预训练阶段中使用了封神框架。
* 2022.09.30 增加[TaiYi-CLIP](#TaiYi-CLIP),首个开源的中文CLIP模型，1.23亿图文对上进行预训练的文本端RoBERTa-large。
* 2022.09.27 增加[PLUG](#PLUG),PLUG集语言理解与生成能力于一身，支持文本生成、问答、语义理解等多类下游任务，PLUG开源将助力开发者在语言理解和语言生成上做出更多延拓。
* 2022.09.11 增加[bloom-6b4](#Bloom),多语言预训练bloom系列生成模型7b1参数(https://huggingface.co/bigscience/bloom-7b1 )的中文vocab提取，bloom系列另有最大176B模型(https://huggingface.co/bigscience/bloom).
* 2022.09.11 增加[GLM-130B](#GLM),提出了开源的双语预训练生成模型 GLM(General Language Model)。
* 2022.09.11 增加[PanGu-α: Large-scale Autoregressive Pretrained Chinese Language Models with Auto-parallel Computation](#PanGu-Alpha) 2.6B和13B 生成模型pytorch版
* 2022.06.29 增加[ERNIE 3.0](#ERNIE3),大规模知识增强预训练语言理解和生成.
* 2022.06.22 增加[Zero and R2D2: A Large-scale Chinese Cross-modal Benchmark and A Vision-Language Framework](#R2D2)，基于大规模中文跨模态基准数据集Zero，训练视觉语言预训练框架 R2D2，用于大规模跨模态学习。
* 2022.06.15 增加[GLM: General Language Model Pretraining with Autoregressive Blank Infilling](#GLM),提出了一种新的通用语言模型 GLM(General Language Model)。 使用自回归填空目标进行预训练，可以针对各种自然语言理解和生成任务进行微调。
* 2022.05.16 增加[GAU-α](#GAU-α),主要提出了一个融合了Attention层和FFN层的新设计GAU（Gated Attention Unit，门控注意力单元），它是新模型更快、更省、更好的关键，此外它使得整个模型只有一种层，也显得更为优雅。
* 2022.03.27 增加[RoFormer-V2](#RoFormer),RoFormer升级版，主要通过结构的简化来提升速度，并通过无监督预训练和有监督预训练的结合来提升效果，从而达到了速度与效果的“双赢”。
* 2022.03.02 增加[MobileBERT](#MobileBERT),MobileBERT是BERT-large模型更“苗条”的版本，使用了瓶颈结构（bottleneck）并且对自注意力和前馈神经网络之间的平衡做了细致的设计。
* 2022.02.24 增加[PERT: Pre-Training BERT with Permuted Language Model](#PERT),一种基于乱序语言模型的预训练模型（PERT），在不引入掩码标记[MASK]的情况下自监督地学习文本语义信息。
* 2021.12.06 增加[SDCUP: Improving Text-to-SQL with Schema Dependency Learning](#SDCUP),达摩院深度语言模型体系 AliceMind 发布中文社区首个表格预训练模型 SDCUP。
* 2021.11.27 增加[RWKV](#RWKV)中文预训练生成模型,类似 GPT-2,模型参考地址：[RWKV-LM](https://github.com/BlinkDL/RWKV-LM)
* 2021.11.27 增加IDEA研究院开源的封神榜系列语言模型，包含[二郎神](#二郎神)、[周文王](#周文王)、[闻仲](#闻仲)、[余元](#余元)。
* 2021.11.25 增加[MC-BERT: Conceptualized Representation Learning for Chinese Biomedical Text Mining](#MC-BERT), 生物医学领域的中文预训练模型.
* 2021.11.24 增加[TaCL: Improving BERT Pre-training with Token-aware Contrastive Learning](#TaCL), Token-aware对比学习预训练模型.
* 2021.10.18 增加[Mengzi: Towards Lightweight yet Ingenious Pre-trained Models for Chinese](#Mengzi-BERT),基于语言学信息融入和训练加速等方法研发了 Mengzi 系列模型.
* 2021.10.14 增加[中文版BART](#BART),训练比较可靠的中文版BART，为中文生成类任务如摘要等提供Baseline.
* 2021.10.14 增加[CPT: A Pre-Trained Unbalanced Transformer for Both Chinese Language Understanding and Generation](#CPT),CPT：兼顾理解和生成的中文预训练模型.
* 2021.10.13 增加[紫东太初多模态大模型](#紫东太初): 全球首个多模态图文音预训练模型,实现了视觉-文本-语音三模态统一表示，构建了三模态预训练大模型。
* 2021.09.19 增加[CogView: Mastering Text-to-Image Generation via Transformers](#CogView),世界最大的中文多模态生成模型,模型支持文生成图为基础的多领域下游任务.
* 2021.09.10 增加[WenLan: Bridging Vision and Language by Large-Scale Multi-Modal Pre-Training](#WenLan)，首个中文通用图文多模态大规模预训练模型。
* 2021.09.10 增加[EVA: An Open-Domain Chinese Dialogue System with Large-Scale Generative Pre-Training](#EVA)，一个开放领域的中文对话预训练模型。
* 2021.08.19 增加[Chinese-Transformer-XL](#GPT-3)：基于中文预训练语料WuDaoCorpus（290G）训练的GPT-3模型。
* 2021.08.16 增加[CPM-2: Large-scale Cost-effective Pre-trained Language Models](#CPM-2)
* 2021.08.16 增加[Lattice-BERT: Leveraging Multi-Granularity Representations in Chinese Pre-trained Language Models](#Lattice-BERT)
* 2021.07.19 增加[roformer-sim-v2](#RoFormer-sim)：利用标注数据增强版本
* 2021.07.15 增加[BERT-CCPoem](#BERT)：古典诗歌语料训练的BERT
* 2021.07.06 增加[ChineseBERT：Chinese Pretraining Enhanced by Glyph and Pinyin Information](#BERT)
* 2021.06.22 增加[StructBERT: Incorporating Language Structures into Pre-training for Deep Language Understanding](#StructBERT)
* 2021.06.14 增加[RoFormer：Enhanced Transformer with Rotary Position Embedding](#RoFormer)
* 2021.05.25 增加[ERNIE-Gram: Pre-Training with Explicitly N-Gram Masked Language Modeling for Natural Language Understanding ]((#ERNIE))
* 2021.04.28 增加[PanGu-α: Large-scale Autoregressive Pretrained Chinese Language Models with Auto-parallel Computation ](#PanGu-Alpha)
* 2021.03.16 增加[T5-PEGASUS: 开源一个中文生成式预训练模型](#T5-PEGASUS)
* 2021.03.09 增加UER系列模型
* 2021.03.04 增加[WoBERT: 基于词颗粒度的中文](#WoBERT)
* 2020.11.11 初始化BERT系列模型[BERT](#BERT)

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 贡献者

<a href="https://github.com/eryajf/learn-github/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=lonePatient/awesome-pretrained-chinese-nlp-models" />
</a>

### Misc
#### &#8627; Stargazers
[![Stargazers repo roster for ](https://reporoster.com/stars/lonePatient/awesome-pretrained-chinese-nlp-models)](https://github.com/lonePatient/awesome-pretrained-chinese-nlp-models/stargazers)

#### &#8627; Forkers
[![Forkers repo roster for](https://reporoster.com/forks/lonePatient/awesome-pretrained-chinese-nlp-models)](https://github.com/lonePatient/awesome-pretrained-chinese-nlp-models/network/members)

#### &#8627; Star History

<div align="center">

[![Star History Chart](https://api.star-history.com/svg?repos=lonePatient/awesome-pretrained-chinese-nlp-models&type=Date)](https://star-history.com/#lonePatient/awesome-pretrained-chinese-nlp-models&Date)

</div>

![Visitor Count](https://profile-counter.glitch.me/lonepatient/count.svg)
