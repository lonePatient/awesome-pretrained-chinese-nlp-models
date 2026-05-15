# Awesome Pretrained Chinese NLP Models[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

![](/resources/LLMS.png)

<div align="center"> 
    <a href="https://arxiv.org/pdf/2303.18223.pdf">论文: A Survey of Large Language Models</a>
</div>

在自然语言处理领域中，预训练语言模型（Pretrained Language Models）已成为非常重要的基础技术，本仓库主要收集目前网上公开的一些高质量中文预训练模型、中文多模态模型、中文大语言模型等内容(感谢分享资源的大佬)，并将持续更新......

> 国内下载HuggingFace仓库模型推荐使用HuggingFace镜像地址: <https://hf-mirror.com/>

## 📑 目录导航

***

## 📚 模型分类索引

### 🤖 大模型系列

| 分类       | 说明             | 链接                        |
| :------- | :------------- | :------------------------ |
| 通用基础大模型  | 参数 >7B 的基础语言模型 | [查看](#Base-LLM)           |
| 垂直基础大模型  | 金融、医疗、法律等垂直领域  | [查看](#Domain-Base-LLM)    |
| 通用对话大模型  | 对话式通用语言模型      | [查看](#chatllm)            |
| 垂直对话大模型  | 垂直领域对话模型       | [查看](#domain-chatllm)     |
| 多模态对话大模型 | 图文等多模态模型       | [查看](#multimodal-chatllm) |
| 推理类大模型   | 数学、逻辑推理模型      | [查看](#reasoningllm)       |

### 🔧 预训练模型系列

| 系列            | 代表模型                                                | 链接                        |
| :------------ | :-------------------------------------------------- | :------------------------ |
| **NLU系列**     | BERT · RoBERTa · ALBERT · ERNIE · MacBERT · ELECTRA | [查看全部 29 个](docs/nlu-models.md)       |
| **NLG系列**     | GPT · GPT-3 · T5 · BART · CPM · RWKV                | [查看全部 18 个](docs/nlg-models.md)       |
| **NLU-NLG系列** | UniLM · GLM · CPT · SimBERT                         | [查看全部 9 个](docs/nlu-nlg-models.md)    |
| **多模态系列**     | WenLan · CogView · Chinese-CLIP · OFA               | [查看全部 13 个](docs/multimodal-models.md) |

### 📦 资源与工具

[📊 大模型评估基准](#大模型评估基准) · [🧪 在线体验](#在线体验大模型) · [📦 开源模型库平台](#开源模型库平台) · [📚 开源数据集库](#开源数据集库) · [📝 中文指令数据集](docs/chinese-instruct-datasets.md) · [🎯 Embedding](#Embedding) · [🔗 Other-Awesome](docs/other-awesome.md)

***

**📌 备注说明**

> **ND:** Non-Causal Decoder (非因果解码器) | **CD:** Causal Decoder (因果解码器) | **ED:** Encoder-Decoder (编码器-解码器)

***
## Base-LLM

> 大规模基础模型：表格中只罗列出参数量`大于7B`以上模型。

| 模型                    | 大小                        | 时间      | 语言 | 架构  | 下载                                                                                                                          | 项目                                                                                     | 机构                                                | 备注                                                                                                               |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| XVERSE-MoE            | 255B / A36B               | 2024-09 | 中英 | MoE | [🤗HF](https://huggingface.co/xverse/XVERSE-MoE-A36B)                                                                       | [GitHub](https://github.com/xverse-ai/XVERSE-MoE-A36B)                                 | xverse-ai                                         | -                                                                                                                |
| Qwen-2.5              | 0.5\~72B (7档)             | 2024-09 | 中英 | CD  | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-66e81a666513e518adb90d9e)                                             | [GitHub](https://github.com/QwenLM/Qwen2.5)                                            | QwenLM                                            | [Blog](https://qwenlm.github.io/blog/qwen2.5/)                                                                   |
| Tele-FLM              | 52B / 102B / 1TB          | 2024-07 | 多语 | CD  | [🤗HF](https://huggingface.co/CofeAI)                                                                                       | -                                                                                      | CofeAI                                            | [Paper](https://arxiv.org/pdf/2404.16645)                                                                        |
| meta-llama-3.1        | 8B / 70B / 405B           | 2024-07 | 多语 | CD  | [🤗HF](https://huggingface.co/meta-llama)                                                                                   | [GitHub](https://github.com/meta-llama/llama3)                                         | meta-llama                                        | -                                                                                                                |
| internlm2.5-Base      | 7B                        | 2024-07 | 中英 | CD  | [🤗HF](https://huggingface.co/internlm)                                                                                     | [GitHub](https://github.com/InternLM/InternLM)                                         | InternLM                                          | [Technical Report](https://arxiv.org/abs/2403.17297)                                                             |
| MAP-NEO-Base          | 2B / 7B                   | 2024-06 | 中英 | CD  | [🤗HF](https://huggingface.co/collections/m-a-p/neo-models-66395a5c9662bb58d5d70f04)                                        | [GitHub](https://github.com/multimodal-art-projection/MAP-NEO)                         | multimodal-art-projection                         | [Paper](https://arxiv.org/abs/2405.19327)                                                                        |
| Nemotron-4-Base       | 340B                      | 2024-06 | 多语 | CD  | [🤗HF](https://huggingface.co/nvidia)                                                                                       | -                                                                                      | NVIDIA                                            | [Technical Report](https://research.nvidia.com/publication/2024-06_nemotron-4-340b)                              |
| Index-Base            | 1.9B                      | 2024-06 | 中英 | CD  | [🤗HF](https://huggingface.co/IndexTeam/Index-1.9B-Chat)                                                                    | [GitHub](https://github.com/bilibili/Index-1.9B)                                       | bilibili                                          | [Report](https://github.com/bilibili/Index-1.9B/blob/main/Index-1.9B%20%E6%8A%80%E6%9C%AF%E6%8A%A5%E5%91%8A.pdf) |
| Qwen2-Base            | 0.5B / 2B / 5B / 7B / 72B | 2024-06 | 多语 | CD  | [🤗HF](https://huggingface.co/Qwen)                                                                                         | [GitHub](https://github.com/QwenLM/Qwen2)                                              | QwenLM                                            | [Blog](https://qwenlm.github.io/)                                                                                |
| GLM-4-Base            | 9B                        | 2024-06 | 多语 | -   | [🤗HF](https://huggingface.co/THUDM)                                                                                        | [GitHub](https://github.com/THUDM/GLM-4)                                               | THUDM                                             | -                                                                                                                |
| Yi-1.5-Base           | 6B / 9B / 34B             | 2024-05 | 中英 | CD  | [🤗HF](https://huggingface.co/01-ai)                                                                                        | [GitHub](https://github.com/01-ai/Yi-1.5)                                              | 01-ai                                             | [Paper](https://arxiv.org/abs/2403.04652)                                                                        |
| DeepSeek-V2-Base      | A21B / 236B               | 2024-05 | 中英 | MoE | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V2)                                                                      | [GitHub](https://github.com/deepseek-ai/DeepSeek-V2)                                   | deepseek-ai                                       | [Paper](https://github.com/deepseek-ai/DeepSeek-V2/blob/main/deepseek-v2-tech-report.pdf)                        |
| Llama-3-Base          | 8B / 70B                  | 2024-04 | 多语 | CD  | [🤗HF](https://hf-mirror.com/meta-llama)                                                                                    | [GitHub](https://github.com/meta-llama/llama3)                                         | Meta Llama                                        | -                                                                                                                |
| Zhinao-Base           | 7B                        | 2024-04 | 中英 | CD  | [🤗HF](https://huggingface.co/qihoo360) · [ModelScope](https://www.modelscope.cn/models/qihoo360/360Zhinao-7B-Base/summary) | -                                                                                      | 奇虎科技                                              | -                                                                                                                |
| XVERSE-MoE            | A4.2B / 25.8B             | 2024-04 | 中英 | MoE | [🤗HF](https://huggingface.co/xverse)                                                                                       | [GitHub](https://github.com/xverse-ai/XVERSE-MoE-A4.2B)                                | xverse-ai                                         | -                                                                                                                |
| SoftTiger-Base        | 13B / 70B                 | 2024-04 | 中英 | CD  | [🤗HF](https://huggingface.co/TigerResearch)                                                                                | [GitHub](https://github.com/TigerResearch/TigerBot)                                    | TigerResearch                                     | -                                                                                                                |
| HammerLLM             | 1.4B                      | 2024-04 | 中英 | -   | [🤗HF](https://huggingface.co/DataHammer)                                                                                   | [GitHub](https://github.com/Academic-Hammer/HammerLLM)                                 | DataHammer                                        | -                                                                                                                |
| Mengzi3-Base          | 13B                       | 2024-04 | 中英 | CD  | [🤗HF](https://huggingface.co/Langboat)                                                                                     | [GitHub](https://github.com/Langboat/Mengzi3)                                          | Langboat                                          | -                                                                                                                |
| Breeze-Base           | 7B                        | 2024-02 | 中英 | -   | [🤗HF](https://huggingface.co/MediaTek-Research)                                                                            | -                                                                                      | MediaTek Research                                 | -                                                                                                                |
| TowerBase             | 7B / 13B                  | 2024-02 | 多语 | CD  | [🤗HF](https://hf-mirror.com/Unbabel)                                                                                       | -                                                                                      | Unbabel                                           | -                                                                                                                |
| Qwen1.5-Base          | 0.5\~110B (7档)            | 2024-02 | 中英 | -   | [🤗HF](https://huggingface.co/Qwen)                                                                                         | [GitHub](https://github.com/QwenLM/Qwen1.5)                                            | Qwen                                              | [Blog](https://qwenlm.github.io/zh/blog/qwen1.5/)                                                                |
| LongAlign-Base        | 6B / 7B / 13B             | 2024-02 | 中英 | -   | [🤗HF](https://hf-mirror.com/THUDM)                                                                                         | [GitHub](https://github.com/THUDM/LongAlign)                                           | THUDM                                             | [Paper](https://arxiv.org/abs/2401.18058)                                                                        |
| Chinese-Mixtral-Base  | 8x7B                      | 2024-02 | 中英 | MoE | [Baidu](https://pan.baidu.com/s/1nwJ8JkMTUrCkDEccg7C9Pw?pwd=33kb) · [🤗HF](https://huggingface.co/hfl/chinese-mixtral)      | [GitHub](https://github.com/ymcui/Chinese-Mixtral)                                     | Yiming Cui                                        | -                                                                                                                |
| iFlytekSpark-Base     | 13B                       | 2024-01 | 中英 | CD  | [MindSpore](https://xihe.mindspore.cn/modelzoo/iflytek/introduce)                                                           | -                                                                                      | 科大讯飞                                              | -                                                                                                                |
| Orion-Base            | 14B                       | 2024-01 | 多语 | CD  | [🤗HF](https://huggingface.co/OrionStarAI)                                                                                  | [GitHub](https://github.com/OrionStarAI/Orion)                                         | OrionStarAI                                       | [Paper](https://github.com/OrionStarAI/Orion/blob/master/doc/Orion14B_v3.pdf)                                    |
| YaYi2-Base            | 30B                       | 2023-12 | 多语 | CD  | [🤗HF](https://huggingface.co/wenge-research)                                                                               | [GitHub](https://github.com/wenge-research/YAYI2)                                      | wenge-research                                    | [Paper](https://arxiv.org/abs/2312.14862)                                                                        |
| Aquila2-Base          | 7B / 34B / 70B            | 2023-12 | 中英 | CD  | [🤗HF](https://huggingface.co/BAAI)                                                                                         | [GitHub](https://github.com/FlagAI-Open/Aquila2)                                       | FlagAI                                            | -                                                                                                                |
| Alaya-Base            | 7B                        | 2023-12 | 中英 | CD  | [🤗HF](https://huggingface.co/DataCanvas)                                                                                   | [GitHub](https://github.com/DataCanvasIO/Alaya)                                        | DataCanvas                                        | -                                                                                                                |
| Qwen-Base             | 1.8B / 7B / 14B / 72B     | 2023-12 | 中英 | CD  | [🤗HF](https://huggingface.co/Qwen)                                                                                         | [GitHub](https://github.com/QwenLM/Qwen)                                               | 阿里云                                               | [Paper](https://arxiv.org/abs/2309.16609)                                                                        |
| DeepSeek-Base         | 7B / 67B                  | 2023-11 | 中英 | CD  | [🤗HF](https://huggingface.co/deepseek-ai)                                                                                  | [GitHub](https://github.com/deepseek-ai/DeepSeek-LLM)                                  | deepseek-ai                                       | -                                                                                                                |
| Yuan-2.0              | 2B / 51B / 102B           | 2023-11 | 中英 | CD  | [GitHub](https://github.com/IEIT-Yuan/Yuan-2.0) · [🤗HF](https://hf-mirror.com/IEITYuan)                                    | [GitHub](https://github.com/IEIT-Yuan/Yuan-2.0)                                        | IEIT-Yuan                                         | -                                                                                                                |
| Yi-Base               | 6B / 9B / 34B             | 2023-11 | 中英 | CD  | [🤗HF](https://huggingface.co/01-ai)                                                                                        | [GitHub](https://github.com/01-ai/Yi)                                                  | 01.AI                                             | -                                                                                                                |
| XVERSE-Base           | 7B / 13B / 65B            | 2023-11 | 多语 | CD  | [🤗HF](https://huggingface.co/xverse)                                                                                       | [GitHub](https://github.com/xverse-ai/XVERSE-13B)                                      | 元象科技                                              | -                                                                                                                |
| Nanbeige-Base         | 16B                       | 2023-11 | 中英 | CD  | [🤗HF](https://huggingface.co/Nanbeige)                                                                                     | [GitHub](https://github.com/Nanbeige/Nanbeige)                                         | Nanbeige LLM Lab                                  | -                                                                                                                |
| LingoWhale            | 8B                        | 2023-11 | 中英 | CD  | [🤗HF](https://huggingface.co/deeplang-ai/LingoWhale-8B)                                                                    | [GitHub](https://github.com/DeepLangAI/LingoWhale-8B/)                                 | DeepLang AI                                       | -                                                                                                                |
| Skywork-Base          | 13B                       | 2023-10 | 中文 | CD  | [🤗HF](https://huggingface.co/Skywork)                                                                                      | [GitHub](https://github.com/SkyworkAI/Skywork)                                         | SkyworkAI                                         | [Paper](https://arxiv.org/abs/2310.16713)                                                                        |
| BlueLM-Base           | 7B                        | 2023-11 | 中英 | CD  | [🤗HF](https://huggingface.co/vivo-ai)                                                                                      | [GitHub](https://github.com/vivo-ai-lab/BlueLM)                                        | vivo AI Lab                                       | -                                                                                                                |
| ChatGLM3-Base         | 6B                        | 2023-10 | 中英 | ND  | [🤗HF](https://huggingface.co/THUDM)                                                                                        | [GitHub](https://github.com/THUDM/ChatGLM3)                                            | THUDM                                             | -                                                                                                                |
| Ziya2-Base            | 13B                       | 2023-10 | 中英 | CD  | [🤗HF](https://modelscope.cn/models/Fengshenbang/Ziya2-13B-Base/summary)                                                    | [GitHub](https://github.com/IDEA-CCNL/Fengshenbang-LM)                                 | IDEA研究院                                           | -                                                                                                                |
| OpenBA-LM             | 15B                       | 2023-09 | 中英 | ED  | [🤗HF](https://huggingface.co/OpenBA/OpenBA-LM)                                                                             | [GitHub](https://github.com/OpenNLG/OpenBA)                                            | OpenNLG Group                                     | [Paper](https://arxiv.org/abs/2309.10706)                                                                        |
| TigerBot-Base-70B     | 80B                       | 2023-09 | 多语 | CD  | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-70b-base)                                                              | [GitHub](https://github.com/TigerResearch/TigerBot)                                    | 虎博科技                                              | [Paper](https://github.com/TigerResearch/TigerBot/wiki/TigerBot%E2%80%9070B%E5%8F%91%E5%B8%83%EF%BC%81)          |
| FLM                   | 101B                      | 2023-09 | 中英 | CD  | [🤗HF](https://huggingface.co/CofeAI/FLM-101B)                                                                              | -                                                                                      | CofeAI                                            | -                                                                                                                |
| Falcon                | 7B / 40B / 180B           | 2023-09 | 多语 | CD  | [🤗HF](https://huggingface.co/tiiuae/)                                                                                      | -                                                                                      | Technology Innovation Institute                   | -                                                                                                                |
| Baichuan2             | 7B / 13B                  | 2023-09 | 中文 | CD  | [🤗HF](https://huggingface.co/baichuan-inc)                                                                                 | [GitHub](https://github.com/baichuan-inc/Baichuan2)                                    | 百川智能                                              | -                                                                                                                |
| Chinese-LLaMA-2-16K   | 7B / 13B                  | 2023-08 | 中英 | CD  | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-2-7b-16k)                                                            | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2)                              | Yiming Cui                                        | -                                                                                                                |
| YuLan-LLaMA-2         | 13B                       | 2023-08 | 中英 | CD  | [🤗HF](https://huggingface.co/yulan-team/YuLan-LLaMA-2-13b)                                                                 | [GitHub](https://github.com/RUC-GSAI/YuLan-Chat)                                       | 中国人民大学                                            | -                                                                                                                |
| Aquila-Base-33B       | 33B                       | 2023-08 | 中英 | CD  | TODO                                                                                                                        | [GitHub](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)            | FlagAI                                            | -                                                                                                                |
| TigerBot-Base-13B     | 13B                       | 2023-08 | 多语 | CD  | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-13b-base)                                                              | [GitHub](https://github.com/TigerResearch/TigerBot)                                    | 虎博科技                                              | -                                                                                                                |
| Linly-Chinese-LLaMA-2 | 7B / 13B                  | 2023-07 | 中英 | CD  | [🤗HF](https://huggingface.co/Linly-AI/Chinese-LLaMA-2-7B-hf)                                                               | [GitHub](https://github.com/CVI-SZU/Linly)                                             | 深圳大学计算机视觉研究所                                      | -                                                                                                                |
| Chinese-LLaMA-2       | 7B                        | 2023-07 | 中英 | CD  | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-2-7b)                                                                | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2)                              | Yiming Cui                                        | -                                                                                                                |
| Jiang-Base            | 13B                       | 2023-07 | 中文 | CD  | [🤗HF](https://huggingface.co/kdf/jiang-base)                                                                               | -                                                                                      | 知未智能                                              | -                                                                                                                |
| BlueWhaleX            | 7B / 13B                  | 2023-07 | 中文 | CD  | [🤗HF](https://huggingface.co/BlueWhaleX/bwx-7B-hf)                                                                         | -                                                                                      | 蓝鲸国数                                              | -                                                                                                                |
| Llama-2               | 7B / 13B / 70B            | 2023-07 | 多语 | CD  | [🤗HF](https://huggingface.co/llamaste/Llama-2-7b)                                                                          | [GitHub](https://github.com/facebookresearch/llama)                                    | Meta                                              | [Paper](https://scontent-hkg4-1.xx.fbcdn.net/v/t39.2365-6/10000000_663429262362723_1696968207443577320_n.pdf)    |
| PolyLM                | 13B                       | 2023-07 | 多语 | CD  | [🤗HF](https://huggingface.co/DAMO-NLP-MT/polylm-13b)                                                                       | [ModelScope](https://modelscope.cn/models/damo/nlp_polylm_13b_text_generation/summary) | 达摩院                                               | [Paper](https://arxiv.org/pdf/2307.06018.pdf)                                                                    |
| Baichuan-13B          | 13B                       | 2023-07 | 中文 | 通用  | \[[🤗HF\]](https://huggingface.co/baichuan-inc/Baichuan-13B-Base)                                                           | [Baichuan-13B](https://github.com/baichuan-inc/Baichuan-13B)                           | [百川智能](https://github.com/baichuan-inc)           | CD                                                                                                               |
| TigerBot              | 7B                        | 2023-07 | 多语 | CD  | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-7b-base-v2)                                                            | [GitHub](https://github.com/TigerResearch/TigerBot)                                    | 虎博科技                                              | -                                                                                                                |
| InternLM-Base         | 7B / 20B                  | 2023-07 | 中文 | CD  | [🤗HF](https://huggingface.co/internlm/internlm-7b)                                                                         | [GitHub](https://github.com/InternLM/InternLM)                                         | 上海人工智能实验室                                         | [Report](https://github.com/InternLM/InternLM-techreport/tree/main)                                              |
| MPT                   | 7B / 30B                  | 2023-06 | 多语 | CD  | [🤗HF](https://huggingface.co/mosaicml/mpt-7b)                                                                              | [GitHub](https://github.com/mosaicml/llm-foundry)                                      | MosaicML                                          | -                                                                                                                |
| Baichuan              | 7B                        | 2023-06 | 中英 | 通用  | \[[🤗HF\]](https://huggingface.co/baichuan-inc/baichuan-7B)                                                                 | [baichuan-7B](https://github.com/baichuan-inc/baichuan-7B)                             | [百川智能](https://github.com/baichuan-inc)           | CD                                                                                                               |
| Chinese-Falcon        | 7B                        | 2023-06 | 中英 | CD  | [🤗HF](https://huggingface.co/Linly-AI/Chinese-Falcon-7B)                                                                   | [GitHub](https://github.com/CVI-SZU/Linly)                                             | 深圳大学计算机视觉研究所                                      | [Blog](https://zhuanlan.zhihu.com/p/636994073)                                                                   |
| AtomGPT               | 13B                       | 2023-06 | 中英 | CD  | [🤗HF](https://huggingface.co/AtomEchoAI/AtomGPT-index)                                                                     | -                                                                                      | 原子回声                                              | -                                                                                                                |
| Aquila                | 7B                        | 2023-06 | 中英 | 通用  | \[[🤗HF\]](https://model.baai.ac.cn/model-detail/100098)                                                                    | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)            | [FlagAI](https://github.com/FlagAI-Open)          | CD                                                                                                               |
| Chinese-LLaMA         | 33B                       | 2023-06 | 中英 | CD  | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-lora-33b)                                                            | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca)                                | Yiming Cui                                        | -                                                                                                                |
| TigerBot              | 7B                        | 2023-06 | 多语 | CD  | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-7b-base)                                                               | [GitHub](https://github.com/TigerResearch/TigerBot)                                    | 虎博科技                                              | -                                                                                                                |
| Panda-OpenLLaMA       | 7B                        | 2023-05 | 中英 | CD  | [🤗HF](https://huggingface.co/chitanda/panda-7b-open-llama-preview-300pt)                                                   | [GitHub](https://github.com/dandelionsllm/pandallm)                                    | dandelionsllm                                     | -                                                                                                                |
| Panda                 | 7/13B                     | 2023-05 | 中英 | 通用  | \[[🤗HF\]](https://huggingface.co/chitanda/llama-panda-zh-13b-delta)                                                        | [pandallm](https://github.com/dandelionsllm/pandallm)                                  | [dandelionsllm](https://github.com/dandelionsllm) | CD                                                                                                               |
| OpenLLaMA             | 13B                       | 2023-05 | 中英 | CD  | [🤗HF](https://huggingface.co/Linly-AI/OpenLLaMA-13B)                                                                       | [GitHub](https://github.com/CVI-SZU/Linly)                                             | 深圳大学计算机视觉研究所                                      | -                                                                                                                |
| BiLLa-LLM             | 7B                        | 2023-05 | 中英 | CD  | [🤗HF](https://huggingface.co/Neutralzz/BiLLa-7B-LLM)                                                                       | [GitHub](https://github.com/Neutralzz/BiLLa)                                           | Zhongli Li                                        | -                                                                                                                |
| Ziya-LLaMA-Reward     | 7B                        | 2023-05 | 中英 | CD  | [🤗HF](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-7B-Reward)                                                               | [GitHub](https://github.com/IDEA-CCNL/Fengshenbang-LM)                                 | IDEA研究院                                           | -                                                                                                                |
| YuYan                 | 11B                       | 2023-04 | 中文 | 通用  | \[[🤗HF\]](https://huggingface.co/FUXI/yuyan-11b)                                                                           | /                                                                                      | [网易伏羲](https://huggingface.co/FUXI)               | CD                                                                                                               | [Paper](https://aclanthology.org/2022.naacl-industry.8/) |
| Chinese-LLaMA         | 7B / 13B / 33B            | 2023-04 | 中文 | CD  | [🤗HF](https://huggingface.co/P01son/Linly-Chinese-LLaMA-33b-hf)                                                            | [GitHub](https://github.com/CVI-SZU/Linly)                                             | 深圳大学计算机视觉研究所                                      | [Blog](https://zhuanlan.zhihu.com/p/616748134)                                                                   |
| OpenChineseLLaMA      | 7B                        | 2023-04 | 中英 | CD  | [🤗HF](https://huggingface.co/openlmlab/open-chinese-llama-7b-patch)                                                        | [GitHub](https://github.com/OpenLMLab/OpenChineseLLaMA)                                | OpenLMLab                                         | -                                                                                                                |
| MOSS-003              | 16B                       | 2023-04 | 中英 | CD  | [🤗HF](https://huggingface.co/fnlp/moss-moon-003-base)                                                                      | [GitHub](https://github.com/OpenLMLab/MOSS)                                            | 复旦大学                                              | -                                                                                                                |
| BBT-2-Text            | 13B / 12B                 | 2023-04 | 中文 | CD  | [申请](https://bbt.ssymmetry.com/model.html)                                                                                  | [GitHub](https://github.com/ssymmetry/BBT-FinCUGE-Applications)                        | 超对称                                               | [Paper](https://bbt.ssymmetry.com/thesis.html)                                                                   |
| Chinese-LLaMA         | 13B                       | 2023-04 | 中英 | CD  | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-lora-13b)                                                            | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca)                                | Yiming Cui                                        | -                                                                                                                |
| Flan-UL2              | 20B                       | 2023-03 | 多语 | ED  | [🤗HF](https://huggingface.co/google/flan-ul2/tree/main)                                                                    | [GitHub](https://github.com/google-research/google-research/tree/master/ul2)           | Google                                            | [Paper](https://arxiv.org/pdf/2205.05131v3.pdf)                                                                  |
| CPM-Bee               | 10B                       | 2023-01 | 中英 | CD  | [🤗HF](https://huggingface.co/openbmb/cpm-bee-10b)                                                                          | [GitHub](https://github.com/OpenBMB/CPM-Bee)                                           | OpenBMB                                           | -                                                                                                                |
| BLOOM                 | 176B                      | 2022-11 | 多语 | CD  | [🤗HF](https://huggingface.co/bigscience/bloom)                                                                             | [GitHub](https://github.com/bigscience-workshop/Megatron-DeepSpeed)                    | BigScience                                        | [Paper](https://arxiv.org/pdf/2211.05100.pdf)                                                                    |
| BLOOMZ                | 176B                      | 2022-11 | 多语 | CD  | [🤗HF](https://huggingface.co/bigscience/bloomz)                                                                            | [GitHub](https://github.com/bigscience-workshop/Megatron-DeepSpeed)                    | BigScience                                        | [Paper](https://arxiv.org/abs/2211.01)                                                                           |
| Flan-T5-XXL           | 11B                       | 2022-11 | 多语 | ED  | [🤗HF](https://huggingface.co/google/flan-t5-xxl)                                                                           | [GitHub](https://github.com/google-research/t5x)                                       | Google                                            | [Paper](https://arxiv.org/pdf/2210.11416.pdf)                                                                    |
| CPM-Ant+              | 10B                       | 2022-10 | 中英 | CD  | [BMB](http://openbmb.oss-cn-hongkong.aliyuncs.com/model_center/cpm-ant-plus-10b/cpm-ant-plus-10b.zip)                       | [GitHub](https://github.com/OpenBMB/CPM-Live)                                          | OpenBMB                                           | [Blog](https://www.openbmb.org/community/blogs/blogpage?id=98afef2ce45f4fe9a4bc15a66d7ccb92)                     |
| GLM-130B              | 130B                      | 2022-10 | 中英 | ND  | [申请](https://docs.google.com/forms/d/e/1FAIpQLSehr5Dh_i3TwACmFFi8QEgIVNYGmSPwV0GueIcsUev0NEfUug/viewform)                   | [GitHub](https://github.com/THUDM/GLM-130B)                                            | 清华大学                                              | [Paper](http://arxiv.org/abs/2210.02414)                                                                         |
| CPM-Ant               | 10B                       | 2022-09 | 中文 | CD  | [🤗HF](https://openbmb.oss-cn-hongkong.aliyuncs.com/model_center/cpmlive-10b/cpm_live_10B.zip)                              | [GitHub](https://github.com/OpenBMB/CPM-Live)                                          | OpenBMB                                           | [Blog](https://www.openbmb.org/community/blogs/blogpage?id=98afef2ce45f4fe9a4bc15a66d7ccb92)                     |
| GLM                   | 10B                       | 2022-09 | 中文 | ND  | [🤗HF](https://lfs.aminer.cn/misc/cogview/glm-10b-chinese.zip)                                                              | [GitHub](https://github.com/THUDM/GLM)                                                 | 清华大学                                              | [Paper](https://arxiv.org/abs/2103.10360)                                                                        |
| Yuan-1.0              | 245B                      | 2021-09 | 中文 | CD  | [API](https://air.inspur.com/home)                                                                                          | [GitHub](https://github.com/Shawn-Inspur/Yuan-1.0)                                     | 浪潮                                                | [Paper](https://arxiv.org/abs/2110.04725)                                                                        |
| CPM-2                 | 10B / 11B / 200B          | 2021-06 | 中文 | ED  | [申请](https://resource.wudao.baai.ac.cn/home?ind=2\&name=WuDao%20WenYuan\&id=1394901846484627456)                            | [GitHub](https://github.com/TsinghuaAI/CPM)                                            | 智源研究院                                             | [Paper](https://arxiv.org/abs/2106.10715)                                                                        |
| PanGu-Alpha           | 13B / 200B                | 2021-05 | 中文 | CD  | [🤗HF](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha)                                                       | [OpenI](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha)                 | 鹏城实验室                                             | [Paper](https://arxiv.org/pdf/2104.12369.pdf)                                                                    |
| PLUG                  | 27B                       | 2021-04 | 中文 | ED  | [申请](https://www.alice-mind.com/portal#/)                                                                                   | [GitHub](https://github.com/alibaba/AliceMind)                                         | 阿里巴巴                                              | -                                                                                                                |
| GPT-3                 | 13B / 30B                 | 2021-04 | 中文 | CD  | TODO                                                                                                                        | [ModelScope](https://modelscope.cn/models/damo/nlp_gpt3_text-generation_13B/summary)   | 达摩院                                               | -                                                                                                                |

<p align="right">[<a href="#top">Back to Top</a>]</p>


## Domain-Base-LLM

> 各个垂直领域开源基础模型

|          模型         |     大小    | 时间      |  语言 | 领域 |                                           下载                                          |                                        项目地址                                       |                              机构/个人                             |  架构 |                                          文献                                         | 备注     |
| :-----------------: | :-------: | ------- | :-: | -- | :-----------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------: | :------------------------------------------------------------: | :-: | :---------------------------------------------------------------------------------: | ------ |
|       Qwen-2.5      |   1.5/7B  | 2024-09 |  中英 | 代码 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-coder-66eaa22e6f99801bf65b0c2f) |                    [Qwen2.5](https://github.com/QwenLM/Qwen2.5)                   |               [QwenLM](https://github.com/QwenLM)              |  CD |                    [Blog](https://qwenlm.github.io/blog/qwen2.5/)                   |
|       Qwen-2.5      | 1.5/7/72B | 2024-09 |  中英 | 数学 |  [🤗HF](https://huggingface.co/collections/Qwen/qwen25-math-66eaa240a1b7d5ee65f1da3e) |                    [Qwen2.5](https://github.com/QwenLM/Qwen2.5)                   |               [QwenLM](https://github.com/QwenLM)              |  CD |                    [Blog](https://qwenlm.github.io/blog/qwen2.5/)                   |
| Tongyi-Finance-Base |    14B    | 2023-11 |  中文 | 金融 |  [ModelScope](https://modelscope.cn/models/TongyiFinance/Tongyi-Finance-14B/summary)  | [通义金融-14B](https://modelscope.cn/models/TongyiFinance/Tongyi-Finance-14B/summary) |   [通义金融大模型](https://modelscope.cn/organization/TongyiFinance)  |  CD |
|      ChiMed-GPT     |    13B    | 2023-10 |  中文 | 医疗 |                \[[🤗HF\]](https://huggingface.co/SYNLP/ChiMed-GPT-1.0)                |                 [ChiMed-GPT](https://github.com/synlp/ChiMed-GPT)                 |              [中国科学技术大学](https://github.com/synlp)              |  CD |                      [Paper](https://arxiv.org/abs/2311.06025)                      |
|    CodeShell-base   |     7B    | 2023-10 |  中英 | 代码 |                \[[🤗HF\]](https://huggingface.co/WisdomShell/CodeShell)               |               [codeshell](https://github.com/WisdomShell/codeshell)               |          [WisdomShell](https://github.com/WisdomShell)         |  CD |
|     WiNGPT-base     |     7B    | 2023-09 |  中文 | 医学 |            \[[🤗HF\]](https://huggingface.co/winninghealth/WiNGPT2-7B-Base)           |                [WiNGPT2](https://github.com/winninghealth/WiNGPT2)                | [Winning Health AI Research](https://github.com/winninghealth) |  CD |
|       XuanYuan      |    70B    | 2023-09 |  中文 | 金融 |              \[[🤗HF\]](https://huggingface.co/Duxiaoman-DI/XuanYuan-70B)             |                [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan)               |             [度小满](https://github.com/Duxiaoman-DI)             |  CD | [Report](https://github.com/Duxiaoman-DI/XuanYuan/blob/main/xuanyuan_70b_report.md) |
|      CodeLLAma      |  7/13/34B | 2023-08 |  多语 | 代码 |                      \[[🤗HF\]](https://huggingface.co/codellama)                     |             [codellama](https://github.com/facebookresearch/codellama)            |      [Meta Research](https://github.com/facebookresearch)      |  CD |                      [Paper](https://arxiv.org/abs/2308.12950)                      |
|   educhat-base-002  |   7/13B   | 2023-06 |  中英 | 教育 |            \[[🤗HF\]](https://huggingface.co/butyuhao/educhat-base-002-13b)           |                  [EduChat](https://github.com/icalk-nlp/EduChat)                  |             [华东师范大学](https://github.com/icalk-nlp)             |  CD |
|    AquilaCode-NV    |     7B    | 2023-06 |  中英 | 代码 |                \[[🤗HF\]](https://model.baai.ac.cn/model-detail/100099)               |    [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)    |            [FlagAI](https://github.com/FlagAI-Open)            |  CD |
|    AquilaCode-TS    |     7B    | 2023-06 |  中英 | 代码 |                \[[🤗HF\]](https://model.baai.ac.cn/model-detail/100099)               |    [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila)    |            [FlagAI](https://github.com/FlagAI-Open)            |  CD |
|        LaWGPT       |     7B    | 2023-05 |  中英 | 法律 |               \[[🤗HF\]](https://huggingface.co/entity303/legal-lora-7b)              |                 [LawGPT](https://github.com/pengxiao-song/LaWGPT)                 |        [Pengxiao Song](https://github.com/pengxiao-song)       |  CD |
|       CodeGeeX      |    13B    | 2022-06 |  多语 | 代码 |                [申请](https://models.aminer.cn/codegeex/download/request)               |                   [CodeGeeX](https://github.com/THUDM/CodeGeeX)                   |                [清华大学](https://github.com/THUDM)                |  CD |                   [blog](https://models.aminer.cn/codegeex/blog/)                   |

<p align="right">[<a href="#top">Back to Top</a>]</p>


## ChatLLM

> 具备问答和对话等功能的大型语言模型。[查看完整列表 →](docs/chat-llm.md)

| 模型 | 大小 | 时间 | 架构 | 下载 | 项目 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| GLM-4.6 | A32/355B | 2025-10 | MoE | [🤗HF](https://huggingface.co/zai-org/GLM-4.5-Base) | [GLM-4.5](https://github.com/zai-org/GLM-4.5) |
| Ling-1T | 1T | 2025-10 | CD | [🤗HF](https://huggingface.co/inclusionAI/Ling-1T) | / |
| Qwen3-Next | A3/80B | 2025-09 | MoE | [🤗HF](https://huggingface.co/Qwen/Qwen3-Next-80B-A3B-Instruct) | [Qwen3](https://github.com/QwenLM/Qwen3) |
| Kimi-k2 | A32B/1T | 2025-08 | MoE | [HF](https://huggingface.co/moonshotai/Kimi-K2-Instruct) | [Kimi-K2](https://github.com/MoonshotAI/Kimi-K2) |
| ERNIE-4.5 | A47/300B A3/21B | 2025-07 | MoE | [🤗HF](https://huggingface.co/baidu) | / |
| Qwen-3 | 4/14/30/235B | 2025-05 | CD/MoE | [🤗HF](https://huggingface.co/collections/Qwen/qwen3-67dd247413f0e2e4f653967f) | [Qwen3](https://github.com/QwenLM/Qwen3) |
| MiMo | 7B | 2025-05 | CD | [🤗HF](https://huggingface.co/XiaomiMiMo) | [MiMo](https://github.com/XiaomiMiMo/MiMo) |
| deepseek-v3 | 671B | 2024-12 | MoE | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V3) | [DeepSeek-V3](https://github.com/deepseek-ai/DeepSeek-V3) |
| Hunyuan-Large | A52/389B | 2024-11 | MoE | [🤗HF](https://huggingface.co/tencent/Tencent-Hunyuan-Large) | [Tencent-Hunyuan-Large](https://github.com/Tencent/Tencent-Hunyuan-Large) |
| Qwen-2.5 | 0.5/1.5/3/7/14/32/72B | 2024-09 | CD | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-66e81a666513e518adb90d9e) | [Qwen2.5](https://github.com/QwenLM/Qwen2.5) |
| MiniCPM3 | 4B | 2024-09 | CD | [🤗HF](https://huggingface.co/openbmb/MiniCPM3-4B) | [MiniCPM](https://github.com/OpenBMB/MiniCPM) |

> 📋 查看全部 180+ 个模型请访问 [ChatLLM 完整列表 →](docs/chat-llm.md)

## Domain-ChatLLM

> 各个垂直领域开源对话模型。[查看完整列表 →](docs/domain-chat-llm.md)

| 模型 | 大小 | 时间 | 领域 | 下载 | 项目 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Qwen3-Coder-Next | / | 2026-02 | 代码 | [🤗HF](https://huggingface.co/Qwen) | [Qwen3](https://github.com/QwenLM/Qwen3) |
| Skywork-SWE | 32B | 2025-06 | 软件工程 | [🤗HF](https://huggingface.co/Skywork/Skywork-SWE-32B) | / |
| Kimi-Dev | / | 2025-06 | 代码 | [🤗HF](https://huggingface.co/moonshotai) | / |
| Qwen3-Coder | / | 2025-08 | 代码 | [🤗HF](https://huggingface.co/Qwen) | [Qwen3](https://github.com/QwenLM/Qwen3) |
| DeepSeek-Coder-V2 | A21/236B | 2024-06 | 代码 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-Coder-V2-Instruct) | [DeepSeek-Coder-V2](https://github.com/deepseek-ai/DeepSeek-Coder-V2) |
| CodeGeeX4 | 9B | 2024-07 | 代码 | [🤗HF](https://huggingface.co/THUDM/codegeex4-all-9b) | [CodeGeeX4](https://github.com/THUDM/CodeGeeX) |
| Yi-Coder | 1.5/9B | 2024-09 | 代码 | [🤗HF](https://huggingface.co/01-ai) | [Yi-Coder](https://github.com/01-ai/Yi-Coder) |
| OpenCoder | 1.5/8B | 2024-11 | 代码 | [🤗HF](https://huggingface.co/infly/OpenCoder) | [OpenCoder](https://github.com/OpenCoder-4/OpenCoder) |

> 📋 查看全部 60+ 个模型请访问 [Domain-ChatLLM 完整列表 →](docs/domain-chat-llm.md)

## MultiModal-ChatLLM

> 收集包含中文的多模态大模型，具备对话等功能。[查看完整列表 →](docs/multimodal-chat-llm.md)

| 模型 | 大小 | 时间 | 领域 | 下载 | 项目 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| HY-World-2.0 | 1.2B | 2026-04 | 3D世界 | [🤗HF](https://huggingface.co/tencent/HY-World-2.0) | [HY-World-2.0](https://github.com/Tencent/HY-World-2.0) |
| Gemma-4-IT | E2B~31B | 2026-04 | 通用 | [🤗HF](https://huggingface.co/collections/google/gemma-4) | - |
| Qianfan-OCR | 4B | 2026-03 | 文档 | [🤗HF](https://huggingface.co/baidu/Qianfan-OCR) | [GitHub](https://github.com/baidubce/Qianfan-VL) |
| AutoGLM-Phone | 9B | 2025-12 | Agent | [🤗HF](https://huggingface.co/zai-org/AutoGLM-Phone-9B) | [Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM) |
| Dolphin-v2 | 3B | 2025-12 | 文图 | [🤗HF](https://huggingface.co/ByteDance/Dolphin-v2) | [Dolphin](https://github.com/bytedance/Dolphin) |
| DeepSeek-OCR | 3B | 2025-10 | 文图 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-OCR) | [DeepSeek-OCR](https://github.com/deepseek-ai/DeepSeek-OCR) |
| Qwen-Image | 20B | 2025-08 | 文图 | [🤗HF](https://huggingface.co/Qwen/Qwen-Image) | [Qwen-Image](https://github.com/QwenLM/Qwen-Image) |
| InternVL 2.5 | 2~78B | 2024-12 | 文图 | [🤗HF](https://huggingface.co/collections/OpenGVLab/internvl-25-673e1019b66e2218f68d7c1c) | [InternVL](https://github.com/OpenGVLab/InternVL) |
| Qwen2-VL | 2/7/72B | 2024-08 | 图文视 | [🤗HF](https://huggingface.co/Qwen/Qwen2-VL-7B-Instruct) | [Qwen2-VL](https://github.com/QwenLM/Qwen2-VL) |
| MiniCPM-V 2.6 | 8B | 2024-08 | 文图视 | [🤗HF](https://huggingface.co/openbmb/MiniCPM-V-2_6) | [MiniCPM-V](https://github.com/OpenBMB/MiniCPM-V) |

> 📋 查看全部 90+ 个模型请访问 [MultiModal-ChatLLM 完整列表 →](docs/multimodal-chat-llm.md)

## ReasoningLLM

> 收集推理能力比较突出的中文大模型。[查看完整列表 →](docs/reasoning-llm.md)

| 模型 | 大小 | 时间 | 架构 | 下载 | 项目 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| DeepSeek-V4-Pro | A49/1.6T | 2026-04 | MoE | [🤗HF](https://huggingface.co/collections/deepseek-ai/deepseek-v4) | [DeepSeek-V4](https://github.com/deepseek-ai/DeepSeek-V4) |
| MiMo-V2.5-Pro | A42/1.02T | 2026-04 | MoE | [🤗HF](https://huggingface.co/XiaomiMiMo/MiMo-V2.5-Pro) | [MiMo](https://github.com/XiaomiMiMo/MiMo) |
| Kimi-K2.6 | A32/1T | 2026-04 | MoE | [🤗HF](https://huggingface.co/moonshotai/Kimi-K2.6) | [Kimi-K2.6](https://github.com/MoonshotAI/Kimi-K2.6) |
| Qwen3.6 | A3/35B | 2026-04 | MoE | [🤗HF](https://huggingface.co/Qwen/Qwen3.6-35B-A3B) | [Qwen3.6](https://github.com/QwenLM/Qwen3.6) |
| DeepSeek-V3.2 | / | 2025-12 | MoE | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V3.2) | [DeepSeek-V3.2-Exp](https://github.com/deepseek-ai/DeepSeek-V3.2-Exp) |
| QwQ-32B | 32B | 2025-03 | CD | [🤗HF](https://huggingface.co/Qwen/QwQ-32B) | / |
| DeepSeek-R1 | A37/671B | 2025-01 | MoE | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-R1) | [DeepSeek-R1](https://github.com/deepseek-ai/DeepSeek-R1) |
| MiniMax-M1 | A46/456B | 2025-06 | MoE | [🤗HF](https://huggingface.co/MiniMaxAI) | [MiniMax-M1](https://github.com/MiniMax-AI/MiniMax-M1) |

> 📋 查看全部 50+ 个模型请访问 [ReasoningLLM 完整列表 →](docs/reasoning-llm.md)

### Embedding

> MTEB排行榜:  <https://huggingface.co/spaces/mteb/leaderboard> [镜像](https://hf-mirror.com/spaces/mteb/leaderboard)

|         模型         |     大小    | 时间      |  语言 |  领域 |                                   下载                                  |                             项目地址                             |                                 机构/个人                                |                           文                          |
| :----------------: | :-------: | ------- | :-: | :-: | :-------------------------------------------------------------------: | :----------------------------------------------------------: | :------------------------------------------------------------------: | :--------------------------------------------------: |
|   Qwen3-Embedding  |  0.6/4/8B | 2025-06 |  多语 |  通用 |      [\[🤗HF\]](https://huggingface.co/Qwen/Qwen3-Embedding-0.6B)     | [Qwen3-Embedding](https://github.com/QwenLM/Qwen3-Embedding) |                  [QwenLM](https://github.com/QwenLM)                 |       [Arxiv](https://arxiv.org/abs/2506.05176)      |
|   JinaColBERT V2   |   large   | 2024-08 |  多语 |  通用 |       \[[🤗HF\]](https://huggingface.co/jinaai/jina-colbert-v2)       |                               /                              |               [Jina AI](https://huggingface.co/jinaai)               |       [Paper](https://arxiv.org/abs/2408.16672)      |
| Conan-embedding-v1 |   large   | 2024-08 |  中文 |  通用 |    \[[🤗HF\]](https://huggingface.co/TencentBAC/Conan-embedding-v1)   |                               /                              |            [TencentABC](https://huggingface.co/TencentBAC)           |       [Paper](https://arxiv.org/abs/2408.15710)      |
|      xiaobu-v2     |   large   | 2024-07 |  中文 |  通用 |     \[[🤗HF\]](https://huggingface.co/lier007/xiaobu-embedding-v2)    |                               /                              |               [lier007](https://huggingface.co/lier007)              |
|    zpoint\_large   |   Large   | 2024-06 |  中文 |  通用 | \[[🤗HF\]](https://huggingface.co/iampanda/zpoint_large_embedding_zh) |                               /                              |              **[yang](https://huggingface.co/iampanda)**             |
|         BCE        |    279M   | 2024-01 |  多语 |  通用 | \[[🤗HF\]](https://huggingface.co/maidalun1020/bce-embedding-base_v1) | [BCEmbedding](https://github.com/netease-youdao/BCEmbedding) |          [netease-youdao](https://github.com/netease-youdao)         |
|       Cohere       |    Base   | 2023-09 |  多语 |  通用 |               \[[🤗HF\]](https://huggingface.co/Cohere)               |                               /                              |                [Cohere](https://huggingface.co/Cohere)               | [Blog](https://txt.cohere.com/introducing-embed-v3/) |
|        jina        |    Base   | 2023-10 |  中英 |  通用 |  \[[🤗HF\]](https://huggingface.co/jinaai/jina-embeddings-v2-base-zh) |                               /                              |               [Jina AI](https://huggingface.co/jinaai)               |
|        Dmeta       | **400MB** | 2024-02 |  中文 |  通用 |      \[[🤗HF\]](https://hf-mirror.com/DMetaSoul/Dmeta-embedding)      |                               /                              |             [DMetaSoul](https://hf-mirror.com/DMetaSoul)             |
|       bge-m3       | 2024-02 |  中文 |  通用 |                 \[[🤗HF\]](https://hf-mirror.com/BAAI)                |                               /                              |                  [BAAI](https://hf-mirror.com/BAAI)                  |     [Paper](https://arxiv.org/pdf/2402.03216.pdf)    |
|       tao-8k       | 2023-11 |  中文 |  通用 |                 \[[🤗HF\]](https://hf-mirror.com/amu)                 |                   [amu](https://hf-mirror.com/amu)                   |
|         bge        |   s/b/l   | 2023-10 |  中文 |  通用 |                 \[[🤗HF\]](https://hf-mirror.com/BAAI)                |                               /                              |                  [BAAI](https://hf-mirror.com/BAAI)                  |
|       gte-zh       |   s/b/l   | 2023-08 |  中文 |  通用 |      \[[🤗HF\]](https://hf-mirror.com/DMetaSoul/Dmeta-embedding)      |                               /                              |                             Alibaba DAMO                             |               [Paper](arXiv:2308.03281)              |
|         m3e        |   s/b/l   | 2023-06 |  中文 |  通用 |               \[[🤗HF\]](https://hf-mirror.com/moka-ai)               |                               /                              |               [Moka-AI](https://hf-mirror.com/moka-ai)               |
|        LaBSE       |  多语 |  通用 |     \[[🤗HF\]](https://hf-mirror.com/sentence-transformers/LaBSE)     |                               /                              | [Sentence Transformers](https://hf-mirror.com/sentence-transformers) |




## 大模型评估基准

### 1. C-Eval

C-Eval 是一个全面的中文基础模型评估套件。它包含了13948个多项选择题，涵盖了52个不同的学科和四个难度级别，查看[论文](https://arxiv.org/abs/2305.08322)了解更多细节。

\[[官方网站](https://cevalbenchmark.com/)]   \[[Github](https://github.com/SJTU-LIT/ceval)]  \[[论文](https://arxiv.org/abs/2305.08322)]

### 2. FlagEval

FlagEval是一个面向AI基础模型的评测工具包。我们的目标是探索和集合科学、公正、开放的基础模型评测基准、方法及工具，对多领域（如语言、语音、视觉及多模态）的基础模型进行多维度（如准确性、效率、鲁棒性等）的评测。我们希望通过对基础模型的评测，加深对基础模型的理解，促进相关的技术创新及产业应用。

\[[官方网站](https://cevalbenchmark.com/)]   \[[Github](https://github.com/FlagOpen/FlagEval)]

### 3. SuperCLUElyb

SuperCLUE琅琊榜，这是一个中文通用大模型对战评价基准，它以众包的方式提供匿名、随机的对战。在本文中，我们发布了初步的结果和基于Elo评级系统的排行榜，Elo评级是国际象棋和其他竞技游戏中广泛使用的评级系统。我们邀请整个社区加入这项工作，贡献新的模型，并通过提问和投票选出你最喜欢的答案来评估它们。

\[[官方网站](https://www.superclueai.com/)]   \[[Github](https://github.com/CLUEbenchmark/SuperCLUElyb)]

### 4. XiezhiBenchmark

该基准包括来自13个不同学科的516个学科的220,000个多项选择题，以及15,000个来自单一学科和多个学科的问题。我们对47个最新的大型语言模型在Xiezhi上进行了评估，结果表明在科学、工程、农学、医学和艺术等领域，大型语言模型的表现超过了人类的平均水平，但在经济学、法学、教育学、文学、历史和管理学等领域，人类的表现仍然远远超过了大型语言模型。

\[[官方网站]()]   \[[Github](https://github.com/mikegu721/xiezhibenchmark)] \[[论文](https://arxiv.org/abs/2306.05783)]

### 5. Open LLM Leaderboard

由HuggingFace组织的一个LLM评测榜单，目前已评估了较多主流的开源LLM模型，以英文为主。主要目标是跟踪、排名和评估最新的大语言模型和聊天机器人，让所有人方便的观察到开源社区的进展和评估这些模型。这个排行榜有一个关键优势，社区中的任何成员都可以提交模型，并在 Hugging Face 的 GPU 集群上自动评估。

\[[官方网站](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)]

### 6. 中文大模型安全评测平台

大模型安全测评依托于一套系统的安全评测框架，涵盖了仇恨言论、偏见歧视言论、犯罪违法、隐私、伦理道德等八大类别，包括细粒度划分的40余个二级安全类别。

\[[官方网站](http://coai.cs.tsinghua.edu.cn/leaderboard/)]   \[[Github](https://github.com/thu-coai/Safety-Prompts)] \[[论文](https://arxiv.org/abs/2304.10436)]

### 7. OpenCompass大语言模型评测

OpenCompass 是一款开源、高效、全面的评测大模型体系及开放平台。我们提供完整开源可复现的评测框架，支持大语言模型、多模态模型各类模型的一站式评测。利用分布式技术，即使面对千亿参数模型也能在数小时内完成评测。基于多个不同维度的高认可度数据集开放多样化的评测方式，包括零样本评测、小样本评测和思维链评测，全方位量化模型各个维度能力。

\[[官方网站](https://opencompass.org.cn/)]   \[[Github](https://github.com/open-compass/opencompass)]




## 在线体验大模型

> **注**：需要申请或者注册方可体验,更多见[Github](https://github.com/wgwang/LLMs-In-China)

### 1. ChatGPT--OpenAI

OpenAI所提出的GPT相关模型，也是目前最火的大语言模型，发布版本已经到了4.0.

\[[官方网站](https://chat.openai.com/chat)]

### 2. New bing--微软

NewBing是微软在2023年3月推出的一款全新的搜索引擎，它基于OpenAI的大型语言模型（LLM），并结合了ChatGPT和DALL·E的技术，为用户提供了一个AI驱动的网络助手。

\[[官方网站](https://www.bing.com/)]

### 3. 文心一言--百度

百度全新一代知识增强大语言模型，文心大模型家族的新成员，能够与人对话互动，回答问题，协助创作，高效便捷地帮助人们获取信息、知识和灵感。

\[[官方网站](https://yiyan.baidu.com/welcome)]

### 4. 通义大模型--阿里

阿里大模型统一品牌，覆盖语言、听觉、多模态等领域致力于实现接近人类智慧的通用智能，让AI从“单一感官”到“五官全开”

\[[官方网站](https://tongyi.aliyun.com/)]

### 5. 星火认知大模型--科大讯飞

科大讯飞推出的新一代认知智能大模型，拥有跨领域的知识和语言理解能力，能够基于自然对话方式理解与执行任务。从海量数据和大规模知识中持续进化，实现从提出、规划到解决问题的全流程闭环。

\[[官方网站](https://xinghuo.xfyun.cn/)]

### 6. Claude--Anthropic

Claude，是人工智能初创公司Anthropic 发布的一款类似ChatGPT的产品。

\[[官方网站](https://www.anthropic.com/product)]

### 7. ChatGLM--智谱AI

基于千亿基座模型 GLM-130B，注入代码预训练，通过有监督微调等技术实现人类意图对齐，具备问答、多轮对话、代码生成功能的中英双语大模型。

\[[官方网站](https://chatglm.cn/)]

### 8. 天工大模型--昆仑万维

天工作为一款大型语言模型，拥有强大的自然语言处理和智能交互能力，能够实现智能问答、聊天互动、文本生成等多种应用场景，并且具有丰富的知识储备，涵盖科学、技术、文化、艺术、历史等领域。

\[[官方网站](https://tiangong.kunlun.com/)]

### 9. 序列猴子大模型--出门问问

序列猴子大模型是一个具有长序列、多模态、单模型、大数据等特点的超大规模语言模型，基于其通用的表示能力与推理能力，能够进行多轮交互，打造更便捷流畅的用户体验，极大地提高了生产效率和数据处理能力，被广泛应用于问答系统、自然语言处理、机器翻译、文本摘要等领域。

\[[官方网站](https://openapi.mobvoi.com/largemodel-introduce)]

### 10. MOSS--复旦大学

MOSS是复旦大学自然语言处理实验室发布的国内第一个对话式大型语言模型

\[[官方网站](https://moss.fastnlp.top/)]

### 11. 360智脑大模--360

360智脑的生成与创作、多轮对话、代码能力、阅读理解、逻辑与推理、多模态等十大核心能力可覆盖大模型全部应用场景。

\[[官方网站](https://ai.360.cn/)]

### 12. 曹植GPT大语言模型--达观数据

达观数据积极探索大语言模型LLM的实践，研发国产版GPT“曹植”系统，作为垂直、专用、自主可控的国产版ChatGPT模型，不仅实现专业领域的AIGC智能化应用，且可内置在客户各类业务系统中提供专用服务

\[[官方网站](http://www.datagrand.com/products/aigc/)]

### 13. 日日新--商汤

商汤“日日新SenseNova”大模型体系，正式问世

不仅展示了大模型体系下的语言大模型，还展示了AI文生图创作、2D/3D数字人生成、大场景/小物体生成等一系列生成式AI模型及应用，还揭开了依托商汤AI大装置SenseCore实现“大模型+大算力”融合创新的研发体系。

\[[官方网站](https://techday.sensetime.com/list)]

### 14. 天燕大模型--APUS

天燕大模型是APUS公司自研的多模态大模型（LMM），具备对文本、图像、视频、音频的理解和生成能力（视频和音频的能力即将推出）。

\[[官方网站](https://www.apusai.com/#/)]

### 15. 元乘象--智子引擎

图文机器人

\[[官方网站](https://chatimg.aixiaoqingxu.com/)]

### 16. 西湖大模型--西湖心辰

\[[官方网站](https://xinchenai.com/)]

### 17. Dongni--深思考

AI多模态搜索引擎

\[[官方网站](https://www.dongni.ai/#/)]

### 18. 山海大模型--云知声

只需一次对话即可获取信息、知识和灵感，解决需求。是每个人身边的助理、朋友和专家。

\[[官方网站](https://shanhai.unisound.com/)]

### 19. MiniMax大模型--MiniMax

MiniMax 最新一代的中文大语言模型帮助人类高效写作、激发创意、获取知识、做出决策现已对企业开放API体验

\[[官方网站](https://api.minimax.chat/)]




## 开源模型库平台

1. 🤗[HuggingFace](https://huggingface.co/): The AI community building the future.

- 模型下载地址: <https://huggingface.co/models>

1. [ModelScope](https://modelscope.cn/home): ModelScope平台是以模型为中心的模型开源社区

- 模型下载地址:<https://modelscope.cn/models>

1. [flagopen](https://flagopen.baai.ac.cn/#/home): flagopen飞智大模型技术开源体系

- 模型下载地址: <https://model.baai.ac.cn/models>

1. [始智AI](https://wisemodel.cn/home): 中国AI开源创新社区

- 模型下载地址: <https://wisemodel.cn/models>




## 开源数据集库

1. huggfaceing数据集仓库: <https://huggingface.co/datasets>

- 包含了自然语言处理、计算机视觉、语音、多模态等数据集，内置100多个多语言公共数据集下载

1. ModelScope数据集仓库:<https://modelscope.cn/datasets>

- 提供了覆盖自然语言处理、计算机视觉、语音、多模态等数据集，更有阿里巴巴集团贡献的专业领域数据集，

1. flagopen数据集仓库: <https://data.baai.ac.cn/data>

- 内置公共数据集下载，可下200G大规模预训练语料[WuDaoCorpora](https://data.baai.ac.cn/details/WuDaoCorporaText)

1. cluebenchmarks数据集仓库：<https://www.cluebenchmarks.com/dataSet_search.html>

- 多个中英文NLP数据集，并可申请下载100GB的高质量中文预训练语料[CLUECorpus2020](https://github.com/CLUEbenchmark/CLUECorpus2020)

1. [MNBVC](https://github.com/esbatmop/MNBVC): Massive Never-ending BT Vast Chinese corpus

- 超大规模中文语料集

1. OpenDataLab数据集仓库: <https://opendatalab.com/>

- OpenDataLab 是有影响力的数据开源开放平台，公开数据集触手可及。

1. [OSCAR](https://oscar-project.org/): Open Super-large Crawled Aggregated coRpus, 多语言数据集

- 最新版本包含1.4T的中文语言数据集





## 🔧 预训练模型系列

> 中文预训练语言模型系列，涵盖 NLU、NLG、NLU-NLG 和多模态四大类。

| 系列 | 说明 | 代表模型 | 详情 |
| :--- | :--- | :--- | :--- |
| **NLU系列** | 自然语言理解 | BERT · RoBERTa · ALBERT · ERNIE · MacBERT · ELECTRA 等 29 个 | [查看完整列表 →](docs/nlu-models.md) |
| **NLG系列** | 自然语言生成 | GPT · GPT-3 · T5 · BART · CPM · RWKV 等 18 个 | [查看完整列表 →](docs/nlg-models.md) |
| **NLU-NLG系列** | 理解与生成 | UniLM · GLM · CPT · SimBERT 等 9 个 | [查看完整列表 →](docs/nlu-nlg-models.md) |
| **多模态系列** | 多模态预训练 | WenLan · CogView · Chinese-CLIP · OFA 等 13 个 | [查看完整列表 →](docs/multimodal-models.md) |

## Other-Awesome

> 其他优质 Awesome 资源列表。[查看完整列表 →](docs/other-awesome.md)

## 更新

- 2026.05.03 增加[Ring-2.6-1T](docs/reasoning-llm.md)、[Ling-2.6-1T](docs/reasoning-llm.md)、[Ling-2.6-flash](docs/reasoning-llm.md)，Ring-2.6-1T 是万亿参数旗舰推理模型，支持 Agent 执行、Reasoning Effort 机制和异步强化学习训练；Ling-2.6-1T 是万亿参数旗舰模型，采用 MLA+Linear Attention 混合架构，Fast Thinking 机制；Ling-2.6-flash 是 104B 总参数/7.4B 激活参数的推理效率优化模型，面向高频 Agent 场景
- 2026.04.24 增加[DeepSeek-V4-Pro, DeepSeek-V4-Flash](docs/reasoning-llm.md)、[MiMo-V2.5-Pro](docs/reasoning-llm.md)，DeepSeek-V4-Pro 总参数 1.6T/激活 49B，V4-Flash 总参数 284B/激活 13B，均支持 1M 超长上下文；MiMo-V2.5-Pro 是小米开源的 1.02T 总参数 MoE 推理模型，激活 42B 参数，支持 1M 上下文
- 2026.04.21 增加[Qwen3.6-35B-A3B](docs/reasoning-llm.md)、[Kimi-K2.6](docs/reasoning-llm.md)、[HY-World-2.0](docs/multimodal-chat-llm.md)
- 2026.04.12 增加[MiniMax-M2.7](docs/reasoning-llm.md)，MiniMax 开源的推理大模型，230B 总参数 MoE 架构，激活 10B 参数
- 2026.04.06 增加[Gemma-4](docs/multimodal-chat-llm.md)，Google DeepMind 开源的多模态大模型
- 2026.02.16 增加[Step-3.5-Flash, GLM-5, MiniMax-M2.5, Kimi-K2.5, Ring-2.5-1T](docs/reasoning-llm.md)、[GLM-OCR, Ace-Step1.5, HunyuanImage-3.0-Instruct](docs/multimodal-chat-llm.md)

> 📋 查看完整更新日志请访问 [更新日志 →](docs/changelog.md)


### Contributors

<a href="https://github.com/eryajf/learn-github/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=lonePatient/awesome-pretrained-chinese-nlp-models" />
</a>

### Misc

#### ↳ Stargazers

[![Stargazers repo roster for ](https://reporoster.com/stars/lonePatient/awesome-pretrained-chinese-nlp-models)](https://github.com/lonePatient/awesome-pretrained-chinese-nlp-models/stargazers)

#### ↳ Forkers

[![Forkers repo roster for](https://reporoster.com/forks/lonePatient/awesome-pretrained-chinese-nlp-models)](https://github.com/lonePatient/awesome-pretrained-chinese-nlp-models/network/members)

#### ↳ Star History

<div align="center">
[![Star History Chart](https://api.star-history.com/svg?repos=lonePatient/awesome-pretrained-chinese-nlp-models&type=Date)](https://star-history.com/#lonePatient/awesome-pretrained-chinese-nlp-models&Date)

</div>

![Visitor Count](https://profile-counter.glitch.me/lonepatient/count.svg)
