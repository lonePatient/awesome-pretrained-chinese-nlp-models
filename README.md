# Awesome Pretrained Chinese NLP Models[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

![](/resources/LLMS.png)
<div align="center"> 
    <a href="https://arxiv.org/pdf/2303.18223.pdf">论文: A Survey of Large Language Models</a>
</div>

在自然语言处理领域中，预训练语言模型（Pretrained Language Models）已成为非常重要的基础技术，本仓库主要收集目前网上公开的一些高质量中文预训练模型、中文多模态模型、中文大语言模型等内容(感谢分享资源的大佬)，并将持续更新......

> 国内下载HuggingFace仓库模型推荐使用HuggingFace镜像地址: https://hf-mirror.com/

# Expand Table of Contents

---

## 📚 模型分类索引

### 🤖 大模型系列

| 分类 | 说明 | 链接 |
|:-----|:-----|:-----|
| 通用基础大模型 | 参数 >7B 的基础语言模型 | [查看](#Base-LLM) |
| 垂直基础大模型 | 金融、医疗、法律等垂直领域 | [查看](#Domain-Base-LLM) |
| 通用对话大模型 | 对话式通用语言模型 | [查看](#ChatLLM) |
| 垂直对话大模型 | 垂直领域对话模型 | [查看](#Domain-ChatLLM) |
| 多模态对话大模型 | 图文等多模态模型 | [查看](#MultiModal-ChatLLM) |
| 推理类大模型 | 数学、逻辑推理模型 | [查看](#ReasoningLLM) |

### 🔧 预训练模型系列

| 系列 | 代表模型 | 链接 |
|:-----|:---------|:-----|
| **NLU系列** | BERT · RoBERTa · ALBERT · ERNIE · MacBERT · ELECTRA | [查看全部 29 个](#NLU系列) |
| **NLG系列** | GPT · GPT-3 · T5 · BART · CPM · RWKV | [查看全部 18 个](#NLG系列) |
| **NLU-NLG系列** | UniLM · GLM · CPT · SimBERT | [查看全部 9 个](#NLU-NLG系列) |
| **多模态系列** | WenLan · CogView · Chinese-CLIP · OFA | [查看全部 13 个](#Multi-Modal) |

### 📦 资源与工具

[📊 大模型评估基准](#大模型评估基准) · [🧪 在线体验](#在线体验大模型) · [📦 开源模型库平台](#开源模型库平台) · [📚 开源数据集库](#开源数据集库) · [📝 中文指令数据集](#中文指令数据集) · [🎯 Embedding](#Embedding) · [🔗 Other-Awesome](#other-awesome)

---

**📌 备注说明**

> **ND:** Non-Causal Decoder (非因果解码器) | **CD:** Causal Decoder (因果解码器) | **ED:** Encoder-Decoder (编码器-解码器)

---

## Base-LLM

> 大规模基础模型：表格中只罗列出参数量`大于7B`以上模型。

| 模型 | 大小 | 时间 | 语言 | 架构 | 下载 | 项目 | 机构 | 备注 |
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
| XVERSE-MoE | 255B / A36B | 2024-09 | 中英 | MoE | [🤗HF](https://huggingface.co/xverse/XVERSE-MoE-A36B) | [GitHub](https://github.com/xverse-ai/XVERSE-MoE-A36B) | xverse-ai | - |
| Qwen-2.5 | 0.5~72B (7档) | 2024-09 | 中英 | CD | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-66e81a666513e518adb90d9e) | [GitHub](https://github.com/QwenLM/Qwen2.5) | QwenLM | [Blog](https://qwenlm.github.io/blog/qwen2.5/) |
| Tele-FLM | 52B / 102B / 1TB | 2024-07 | 多语 | CD | [🤗HF](https://huggingface.co/CofeAI) | - | CofeAI | [Paper](https://arxiv.org/pdf/2404.16645) |
| meta-llama-3.1 | 8B / 70B / 405B | 2024-07 | 多语 | CD | [🤗HF](https://huggingface.co/meta-llama) | [GitHub](https://github.com/meta-llama/llama3) | meta-llama | - |
| internlm2.5-Base | 7B | 2024-07 | 中英 | CD | [🤗HF](https://huggingface.co/internlm) | [GitHub](https://github.com/InternLM/InternLM) | InternLM | [Technical Report](https://arxiv.org/abs/2403.17297) |
| MAP-NEO-Base | 2B / 7B | 2024-06 | 中英 | CD | [🤗HF](https://huggingface.co/collections/m-a-p/neo-models-66395a5c9662bb58d5d70f04) | [GitHub](https://github.com/multimodal-art-projection/MAP-NEO) | multimodal-art-projection | [Paper](https://arxiv.org/abs/2405.19327) |
| Nemotron-4-Base | 340B | 2024-06 | 多语 | CD | [🤗HF](https://huggingface.co/nvidia) | - | NVIDIA | [Technical Report](https://research.nvidia.com/publication/2024-06_nemotron-4-340b) |
| Index-Base | 1.9B | 2024-06 | 中英 | CD | [🤗HF](https://huggingface.co/IndexTeam/Index-1.9B-Chat) | [GitHub](https://github.com/bilibili/Index-1.9B) | bilibili | [Report](https://github.com/bilibili/Index-1.9B/blob/main/Index-1.9B%20%E6%8A%80%E6%9C%AF%E6%8A%A5%E5%91%8A.pdf) |
| Qwen2-Base | 0.5B / 2B / 5B / 7B / 72B | 2024-06 | 多语 | CD | [🤗HF](https://huggingface.co/Qwen) | [GitHub](https://github.com/QwenLM/Qwen2) | QwenLM | [Blog](https://qwenlm.github.io/) |
| GLM-4-Base | 9B | 2024-06 | 多语 | - | [🤗HF](https://huggingface.co/THUDM) | [GitHub](https://github.com/THUDM/GLM-4) | THUDM | - |
| Yi-1.5-Base | 6B / 9B / 34B | 2024-05 | 中英 | CD | [🤗HF](https://huggingface.co/01-ai) | [GitHub](https://github.com/01-ai/Yi-1.5) | 01-ai | [Paper](https://arxiv.org/abs/2403.04652) |
| DeepSeek-V2-Base | A21B / 236B | 2024-05 | 中英 | MoE | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V2) | [GitHub](https://github.com/deepseek-ai/DeepSeek-V2) | deepseek-ai | [Paper](https://github.com/deepseek-ai/DeepSeek-V2/blob/main/deepseek-v2-tech-report.pdf) |
| Llama-3-Base | 8B / 70B | 2024-04 | 多语 | CD | [🤗HF](https://hf-mirror.com/meta-llama) | [GitHub](https://github.com/meta-llama/llama3) | Meta Llama | - |
| Zhinao-Base | 7B | 2024-04 | 中英 | CD | [🤗HF](https://huggingface.co/qihoo360) · [ModelScope](https://www.modelscope.cn/models/qihoo360/360Zhinao-7B-Base/summary) | - | 奇虎科技 | - |
| XVERSE-MoE | A4.2B / 25.8B | 2024-04 | 中英 | MoE | [🤗HF](https://huggingface.co/xverse) | [GitHub](https://github.com/xverse-ai/XVERSE-MoE-A4.2B) | xverse-ai | - |
| SoftTiger-Base | 13B / 70B | 2024-04 | 中英 | CD | [🤗HF](https://huggingface.co/TigerResearch) | [GitHub](https://github.com/TigerResearch/TigerBot) | TigerResearch | - |
| HammerLLM | 1.4B | 2024-04 | 中英 | - | [🤗HF](https://huggingface.co/DataHammer) | [GitHub](https://github.com/Academic-Hammer/HammerLLM) | DataHammer | - |
| Mengzi3-Base | 13B | 2024-04 | 中英 | CD | [🤗HF](https://huggingface.co/Langboat) | [GitHub](https://github.com/Langboat/Mengzi3) | Langboat | - |
| Breeze-Base | 7B | 2024-02 | 中英 | - | [🤗HF](https://huggingface.co/MediaTek-Research) | - | MediaTek Research | - |
| TowerBase | 7B / 13B | 2024-02 | 多语 | CD | [🤗HF](https://hf-mirror.com/Unbabel) | - | Unbabel | - |
| Qwen1.5-Base | 0.5~110B (7档) | 2024-02 | 中英 | - | [🤗HF](https://huggingface.co/Qwen) | [GitHub](https://github.com/QwenLM/Qwen1.5) | Qwen | [Blog](https://qwenlm.github.io/zh/blog/qwen1.5/) |
| LongAlign-Base | 6B / 7B / 13B | 2024-02 | 中英 | - | [🤗HF](https://hf-mirror.com/THUDM) | [GitHub](https://github.com/THUDM/LongAlign) | THUDM | [Paper](https://arxiv.org/abs/2401.18058) |
| Chinese-Mixtral-Base | 8x7B | 2024-02 | 中英 | MoE | [Baidu](https://pan.baidu.com/s/1nwJ8JkMTUrCkDEccg7C9Pw?pwd=33kb) · [🤗HF](https://huggingface.co/hfl/chinese-mixtral) | [GitHub](https://github.com/ymcui/Chinese-Mixtral) | Yiming Cui | - |
| iFlytekSpark-Base | 13B | 2024-01 | 中英 | CD | [MindSpore](https://xihe.mindspore.cn/modelzoo/iflytek/introduce) | - | 科大讯飞 | - |
| Orion-Base | 14B | 2024-01 | 多语 | CD | [🤗HF](https://huggingface.co/OrionStarAI) | [GitHub](https://github.com/OrionStarAI/Orion) | OrionStarAI | [Paper](https://github.com/OrionStarAI/Orion/blob/master/doc/Orion14B_v3.pdf) |
| YaYi2-Base | 30B | 2023-12 | 多语 | CD | [🤗HF](https://huggingface.co/wenge-research) | [GitHub](https://github.com/wenge-research/YAYI2) | wenge-research | [Paper](https://arxiv.org/abs/2312.14862) |
| Aquila2-Base | 7B / 34B / 70B | 2023-12 | 中英 | CD | [🤗HF](https://huggingface.co/BAAI) | [GitHub](https://github.com/FlagAI-Open/Aquila2) | FlagAI | - |
| Alaya-Base | 7B | 2023-12 | 中英 | CD | [🤗HF](https://huggingface.co/DataCanvas) | [GitHub](https://github.com/DataCanvasIO/Alaya) | DataCanvas | - |
| Qwen-Base | 1.8B / 7B / 14B / 72B | 2023-12 | 中英 | CD | [🤗HF](https://huggingface.co/Qwen) | [GitHub](https://github.com/QwenLM/Qwen) | 阿里云 | [Paper](https://arxiv.org/abs/2309.16609) |
| DeepSeek-Base | 7B / 67B | 2023-11 | 中英 | CD | [🤗HF](https://huggingface.co/deepseek-ai) | [GitHub](https://github.com/deepseek-ai/DeepSeek-LLM) | deepseek-ai | - |
| Yuan-2.0 | 2B / 51B / 102B | 2023-11 | 中英 | CD | [GitHub](https://github.com/IEIT-Yuan/Yuan-2.0) · [🤗HF](https://hf-mirror.com/IEITYuan) | [GitHub](https://github.com/IEIT-Yuan/Yuan-2.0) | IEIT-Yuan | - |
| Yi-Base | 6B / 9B / 34B | 2023-11 | 中英 | CD | [🤗HF](https://huggingface.co/01-ai) | [GitHub](https://github.com/01-ai/Yi) | 01.AI | - |
| XVERSE-Base | 7B / 13B / 65B | 2023-11 | 多语 | CD | [🤗HF](https://huggingface.co/xverse) | [GitHub](https://github.com/xverse-ai/XVERSE-13B) | 元象科技 | - |
| Nanbeige-Base | 16B | 2023-11 | 中英 | CD | [🤗HF](https://huggingface.co/Nanbeige) | [GitHub](https://github.com/Nanbeige/Nanbeige) | Nanbeige LLM Lab | - |
| LingoWhale | 8B | 2023-11 | 中英 | CD | [🤗HF](https://huggingface.co/deeplang-ai/LingoWhale-8B) | [GitHub](https://github.com/DeepLangAI/LingoWhale-8B/) | DeepLang AI | - |
| Skywork-Base | 13B | 2023-10 | 中文 | CD | [🤗HF](https://huggingface.co/Skywork) | [GitHub](https://github.com/SkyworkAI/Skywork) | SkyworkAI | [Paper](https://arxiv.org/abs/2310.16713) |
| BlueLM-Base | 7B | 2023-11 | 中英 | CD | [🤗HF](https://huggingface.co/vivo-ai) | [GitHub](https://github.com/vivo-ai-lab/BlueLM) | vivo AI Lab | - |
| ChatGLM3-Base | 6B | 2023-10 | 中英 | ND | [🤗HF](https://huggingface.co/THUDM) | [GitHub](https://github.com/THUDM/ChatGLM3) | THUDM | - |
| Ziya2-Base | 13B | 2023-10 | 中英 | CD | [🤗HF](https://modelscope.cn/models/Fengshenbang/Ziya2-13B-Base/summary) | [GitHub](https://github.com/IDEA-CCNL/Fengshenbang-LM) | IDEA研究院 | - |
| OpenBA-LM | 15B | 2023-09 | 中英 | ED | [🤗HF](https://huggingface.co/OpenBA/OpenBA-LM) | [GitHub](https://github.com/OpenNLG/OpenBA) | OpenNLG Group | [Paper](https://arxiv.org/abs/2309.10706) |
| TigerBot-Base-70B | 80B | 2023-09 | 多语 | CD | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-70b-base) | [GitHub](https://github.com/TigerResearch/TigerBot) | 虎博科技 | [Paper](https://github.com/TigerResearch/TigerBot/wiki/TigerBot%E2%80%9070B%E5%8F%91%E5%B8%83%EF%BC%81) |
| FLM | 101B | 2023-09 | 中英 | CD | [🤗HF](https://huggingface.co/CofeAI/FLM-101B) | - | CofeAI | - |
| Falcon | 7B / 40B / 180B | 2023-09 | 多语 | CD | [🤗HF](https://huggingface.co/tiiuae/) | - | Technology Innovation Institute | - |
| Baichuan2 | 7B / 13B | 2023-09 | 中文 | CD | [🤗HF](https://huggingface.co/baichuan-inc) | [GitHub](https://github.com/baichuan-inc/Baichuan2) | 百川智能 | - |
| Chinese-LLaMA-2-16K | 7B / 13B | 2023-08 | 中英 | CD | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-2-7b-16k) | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2) | Yiming Cui | - |
| YuLan-LLaMA-2 | 13B | 2023-08 | 中英 | CD | [🤗HF](https://huggingface.co/yulan-team/YuLan-LLaMA-2-13b) | [GitHub](https://github.com/RUC-GSAI/YuLan-Chat) | 中国人民大学 | - |
| Aquila-Base-33B | 33B | 2023-08 | 中英 | CD | TODO | [GitHub](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila) | FlagAI | - |
| TigerBot-Base-13B | 13B | 2023-08 | 多语 | CD | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-13b-base) | [GitHub](https://github.com/TigerResearch/TigerBot) | 虎博科技 | - |
| Linly-Chinese-LLaMA-2 | 7B / 13B | 2023-07 | 中英 | CD | [🤗HF](https://huggingface.co/Linly-AI/Chinese-LLaMA-2-7B-hf) | [GitHub](https://github.com/CVI-SZU/Linly) | 深圳大学计算机视觉研究所 | - |
| Chinese-LLaMA-2 | 7B | 2023-07 | 中英 | CD | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-2-7b) | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2) | Yiming Cui | - |
| Jiang-Base | 13B | 2023-07 | 中文 | CD | [🤗HF](https://huggingface.co/kdf/jiang-base) | - | 知未智能 | - |
| BlueWhaleX | 7B / 13B | 2023-07 | 中文 | CD | [🤗HF](https://huggingface.co/BlueWhaleX/bwx-7B-hf) | - | 蓝鲸国数 | - |
| Llama-2 | 7B / 13B / 70B | 2023-07 | 多语 | CD | [🤗HF](https://huggingface.co/llamaste/Llama-2-7b) | [GitHub](https://github.com/facebookresearch/llama) | Meta | [Paper](https://scontent-hkg4-1.xx.fbcdn.net/v/t39.2365-6/10000000_663429262362723_1696968207443577320_n.pdf) |
| PolyLM | 13B | 2023-07 | 多语 | CD | [🤗HF](https://huggingface.co/DAMO-NLP-MT/polylm-13b) | [ModelScope](https://modelscope.cn/models/damo/nlp_polylm_13b_text_generation/summary) | 达摩院 | [Paper](https://arxiv.org/pdf/2307.06018.pdf) |
|     Baichuan-13B      |        13B        | 2023-07 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/baichuan-inc/Baichuan-13B-Base) | [Baichuan-13B](https://github.com/baichuan-inc/Baichuan-13B) |         [百川智能](https://github.com/baichuan-inc)          |  CD  |                                                              |            |
| TigerBot | 7B | 2023-07 | 多语 | CD | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-7b-base-v2) | [GitHub](https://github.com/TigerResearch/TigerBot) | 虎博科技 | - |
| InternLM-Base | 7B / 20B | 2023-07 | 中文 | CD | [🤗HF](https://huggingface.co/internlm/internlm-7b) | [GitHub](https://github.com/InternLM/InternLM) | 上海人工智能实验室 | [Report](https://github.com/InternLM/InternLM-techreport/tree/main) |
| MPT | 7B / 30B | 2023-06 | 多语 | CD | [🤗HF](https://huggingface.co/mosaicml/mpt-7b) | [GitHub](https://github.com/mosaicml/llm-foundry) | MosaicML | - |
|       Baichuan        |        7B         | 2023-06 | 中英 | 通用 |   [[🤗HF\]](https://huggingface.co/baichuan-inc/baichuan-7B) | [baichuan-7B](https://github.com/baichuan-inc/baichuan-7B) |         [百川智能](https://github.com/baichuan-inc)          |  CD  |                                                              |            |
| Chinese-Falcon | 7B | 2023-06 | 中英 | CD | [🤗HF](https://huggingface.co/Linly-AI/Chinese-Falcon-7B) | [GitHub](https://github.com/CVI-SZU/Linly) | 深圳大学计算机视觉研究所 | [Blog](https://zhuanlan.zhihu.com/p/636994073) |
| AtomGPT | 13B | 2023-06 | 中英 | CD | [🤗HF](https://huggingface.co/AtomEchoAI/AtomGPT-index) | - | 原子回声 | - |
|        Aquila         |        7B         | 2023-06 | 中英 | 通用 |     [[🤗HF\]](https://model.baai.ac.cn/model-detail/100098)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila) |           [FlagAI](https://github.com/FlagAI-Open)           |  CD  |                                                              |            |
| Chinese-LLaMA | 33B | 2023-06 | 中英 | CD | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-lora-33b) | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca) | Yiming Cui | - |
| TigerBot | 7B | 2023-06 | 多语 | CD | [🤗HF](https://huggingface.co/TigerResearch/tigerbot-7b-base) | [GitHub](https://github.com/TigerResearch/TigerBot) | 虎博科技 | - |
| Panda-OpenLLaMA | 7B | 2023-05 | 中英 | CD | [🤗HF](https://huggingface.co/chitanda/panda-7b-open-llama-preview-300pt) | [GitHub](https://github.com/dandelionsllm/pandallm) | dandelionsllm | - |
|         Panda         |       7/13B       | 2023-05 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/chitanda/llama-panda-zh-13b-delta) | [pandallm](https://github.com/dandelionsllm/pandallm) |      [dandelionsllm](https://github.com/dandelionsllm)       |  CD  |                                                              |            |
| OpenLLaMA | 13B | 2023-05 | 中英 | CD | [🤗HF](https://huggingface.co/Linly-AI/OpenLLaMA-13B) | [GitHub](https://github.com/CVI-SZU/Linly) | 深圳大学计算机视觉研究所 | - |
| BiLLa-LLM | 7B | 2023-05 | 中英 | CD | [🤗HF](https://huggingface.co/Neutralzz/BiLLa-7B-LLM) | [GitHub](https://github.com/Neutralzz/BiLLa) | Zhongli Li | - |
| Ziya-LLaMA-Reward | 7B | 2023-05 | 中英 | CD | [🤗HF](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-7B-Reward) | [GitHub](https://github.com/IDEA-CCNL/Fengshenbang-LM) | IDEA研究院 | - |
|         YuYan         |        11B        | 2023-04 | 中文 | 通用 |        [[🤗HF\]](https://huggingface.co/FUXI/yuyan-11b)      |                              /                               |           [网易伏羲](https://huggingface.co/FUXI)            |  CD  |   [Paper](https://aclanthology.org/2022.naacl-industry.8/)   |            |
| Chinese-LLaMA | 7B / 13B / 33B | 2023-04 | 中文 | CD | [🤗HF](https://huggingface.co/P01son/Linly-Chinese-LLaMA-33b-hf) | [GitHub](https://github.com/CVI-SZU/Linly) | 深圳大学计算机视觉研究所 | [Blog](https://zhuanlan.zhihu.com/p/616748134) |
| OpenChineseLLaMA | 7B | 2023-04 | 中英 | CD | [🤗HF](https://huggingface.co/openlmlab/open-chinese-llama-7b-patch) | [GitHub](https://github.com/OpenLMLab/OpenChineseLLaMA) | OpenLMLab | - |
| MOSS-003 | 16B | 2023-04 | 中英 | CD | [🤗HF](https://huggingface.co/fnlp/moss-moon-003-base) | [GitHub](https://github.com/OpenLMLab/MOSS) | 复旦大学 | - |
| BBT-2-Text | 13B / 12B | 2023-04 | 中文 | CD | [申请](https://bbt.ssymmetry.com/model.html) | [GitHub](https://github.com/ssymmetry/BBT-FinCUGE-Applications) | 超对称 | [Paper](https://bbt.ssymmetry.com/thesis.html) |
| Chinese-LLaMA | 13B | 2023-04 | 中英 | CD | [🤗HF](https://huggingface.co/ziqingyang/chinese-llama-lora-13b) | [GitHub](https://github.com/ymcui/Chinese-LLaMA-Alpaca) | Yiming Cui | - |
| Flan-UL2 | 20B | 2023-03 | 多语 | ED | [🤗HF](https://huggingface.co/google/flan-ul2/tree/main) | [GitHub](https://github.com/google-research/google-research/tree/master/ul2) | Google | [Paper](https://arxiv.org/pdf/2205.05131v3.pdf) |
| CPM-Bee | 10B | 2023-01 | 中英 | CD | [🤗HF](https://huggingface.co/openbmb/cpm-bee-10b) | [GitHub](https://github.com/OpenBMB/CPM-Bee) | OpenBMB | - |
| BLOOM | 176B | 2022-11 | 多语 | CD | [🤗HF](https://huggingface.co/bigscience/bloom) | [GitHub](https://github.com/bigscience-workshop/Megatron-DeepSpeed) | BigScience | [Paper](https://arxiv.org/pdf/2211.05100.pdf) |
| BLOOMZ | 176B | 2022-11 | 多语 | CD | [🤗HF](https://huggingface.co/bigscience/bloomz) | [GitHub](https://github.com/bigscience-workshop/Megatron-DeepSpeed) | BigScience | [Paper](https://arxiv.org/abs/2211.01) |
| Flan-T5-XXL | 11B | 2022-11 | 多语 | ED | [🤗HF](https://huggingface.co/google/flan-t5-xxl) | [GitHub](https://github.com/google-research/t5x) | Google | [Paper](https://arxiv.org/pdf/2210.11416.pdf) |
| CPM-Ant+ | 10B | 2022-10 | 中英 | CD | [BMB](http://openbmb.oss-cn-hongkong.aliyuncs.com/model_center/cpm-ant-plus-10b/cpm-ant-plus-10b.zip) | [GitHub](https://github.com/OpenBMB/CPM-Live) | OpenBMB | [Blog](https://www.openbmb.org/community/blogs/blogpage?id=98afef2ce45f4fe9a4bc15a66d7ccb92) |
| GLM-130B | 130B | 2022-10 | 中英 | ND | [申请](https://docs.google.com/forms/d/e/1FAIpQLSehr5Dh_i3TwACmFFi8QEgIVNYGmSPwV0GueIcsUev0NEfUug/viewform) | [GitHub](https://github.com/THUDM/GLM-130B) | 清华大学 | [Paper](http://arxiv.org/abs/2210.02414) |
| CPM-Ant | 10B | 2022-09 | 中文 | CD | [🤗HF](https://openbmb.oss-cn-hongkong.aliyuncs.com/model_center/cpmlive-10b/cpm_live_10B.zip) | [GitHub](https://github.com/OpenBMB/CPM-Live) | OpenBMB | [Blog](https://www.openbmb.org/community/blogs/blogpage?id=98afef2ce45f4fe9a4bc15a66d7ccb92) |
| GLM | 10B | 2022-09 | 中文 | ND | [🤗HF](https://lfs.aminer.cn/misc/cogview/glm-10b-chinese.zip) | [GitHub](https://github.com/THUDM/GLM) | 清华大学 | [Paper](https://arxiv.org/abs/2103.10360) |
| Yuan-1.0 | 245B | 2021-09 | 中文 | CD | [API](https://air.inspur.com/home) | [GitHub](https://github.com/Shawn-Inspur/Yuan-1.0) | 浪潮 | [Paper](https://arxiv.org/abs/2110.04725) |
| CPM-2 | 10B / 11B / 200B | 2021-06 | 中文 | ED | [申请](https://resource.wudao.baai.ac.cn/home?ind=2&name=WuDao%20WenYuan&id=1394901846484627456) | [GitHub](https://github.com/TsinghuaAI/CPM) | 智源研究院 | [Paper](https://arxiv.org/abs/2106.10715) |
| PanGu-Alpha | 13B / 200B | 2021-05 | 中文 | CD | [🤗HF](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha) | [OpenI](https://openi.pcl.ac.cn/PCL-Platform.Intelligence/PanGu-Alpha) | 鹏城实验室 | [Paper](https://arxiv.org/pdf/2104.12369.pdf) |
| PLUG | 27B | 2021-04 | 中文 | ED | [申请](https://www.alice-mind.com/portal#/) | [GitHub](https://github.com/alibaba/AliceMind) | 阿里巴巴 | - |
| GPT-3 | 13B / 30B | 2021-04 | 中文 | CD | TODO | [ModelScope](https://modelscope.cn/models/damo/nlp_gpt3_text-generation_13B/summary) | 达摩院 | - |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## Domain-Base-LLM

> 各个垂直领域开源基础模型

|       模型        | 大小  | 时间    | 语言 | 领域 |                             下载                             |                           项目地址                           |                          机构/个人                           | 架构 |                             文献                             | 备注 |
| :---------------: | :---: | ------- | :--: | ---- | :---------------------------------------: | :---------------------: | :------------------------------: | :--: | :--------------------: | ---- |
| Qwen-2.5 |        1.5/7B         | 2024-09 | 中英 | 代码 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-coder-66eaa22e6f99801bf65b0c2f) | [Qwen2.5](https://github.com/QwenLM/Qwen2.5) | [QwenLM](https://github.com/QwenLM) |  CD  | [Blog](https://qwenlm.github.io/blog/qwen2.5/) |      |
| Qwen-2.5 |       1.5/7/72B       | 2024-09 | 中英 | 数学 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-math-66eaa240a1b7d5ee65f1da3e) | [Qwen2.5](https://github.com/QwenLM/Qwen2.5) | [QwenLM](https://github.com/QwenLM) |  CD  | [Blog](https://qwenlm.github.io/blog/qwen2.5/) |      |
| Tongyi-Finance-Base |  14B  | 2023-11 | 中文 | 金融 | [ModelScope](https://modelscope.cn/models/TongyiFinance/Tongyi-Finance-14B/summary) | [通义金融-14B](https://modelscope.cn/models/TongyiFinance/Tongyi-Finance-14B/summary) | [通义金融大模型](https://modelscope.cn/organization/TongyiFinance) |  CD  |      |      |
| ChiMed-GPT | 13B | 2023-10 | 中文 | 医疗 | [[🤗HF\]](https://huggingface.co/SYNLP/ChiMed-GPT-1.0) | [ChiMed-GPT](https://github.com/synlp/ChiMed-GPT) | [中国科学技术大学](https://github.com/synlp) | CD | [Paper](https://arxiv.org/abs/2311.06025) |  |
| CodeShell-base |  7B  | 2023-10 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/WisdomShell/CodeShell) | [codeshell](https://github.com/WisdomShell/codeshell) | [WisdomShell](https://github.com/WisdomShell) |  CD  |      |      |
| WiNGPT-base |  7B  | 2023-09 | 中文 | 医学 | [[🤗HF\]](https://huggingface.co/winninghealth/WiNGPT2-7B-Base) | [WiNGPT2](https://github.com/winninghealth/WiNGPT2) | [Winning Health AI Research](https://github.com/winninghealth) |  CD  |      |      |
| XuanYuan | 70B  | 2023-09 | 中文 | 金融 | [[🤗HF\]](https://huggingface.co/Duxiaoman-DI/XuanYuan-70B) | [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan)  | [度小满](https://github.com/Duxiaoman-DI) |  CD  | [Report](https://github.com/Duxiaoman-DI/XuanYuan/blob/main/xuanyuan_70b_report.md) |      |
| CodeLLAma | 7/13/<br/>34B | 2023-08 | 多语 | 代码 | [[🤗HF\]](https://huggingface.co/codellama) | [codellama](https://github.com/facebookresearch/codellama) | [Meta Research](https://github.com/facebookresearch) |  CD  | [Paper](https://arxiv.org/abs/2308.12950) |      |
| educhat-base-002  | 7/13B | 2023-06 | 中英 | 教育 | [[🤗HF\]](https://huggingface.co/butyuhao/educhat-base-002-13b) | [EduChat](https://github.com/icalk-nlp/EduChat) |         [华东师范大学](https://github.com/icalk-nlp)         |  CD  |                                                              |      |
|   AquilaCode-NV   |  7B   | 2023-06 | 中英 | 代码 |     [[🤗HF\]](https://model.baai.ac.cn/model-detail/100099)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila) |          [FlagAI](https://github.com/FlagAI-Open)           |  CD  |                                                              |      |
|   AquilaCode-TS   |  7B   | 2023-06 | 中英 | 代码 |     [[🤗HF\]](https://model.baai.ac.cn/model-detail/100099)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila) |          [FlagAI](https://github.com/FlagAI-Open)           |  CD  |                                                              |      |
|      LaWGPT       |  7B   | 2023-05 | 中英 | 法律 |    [[🤗HF\]](https://huggingface.co/entity303/legal-lora-7b)    | [LawGPT](https://github.com/pengxiao-song/LaWGPT) |      [Pengxiao Song](https://github.com/pengxiao-song)       |  CD  |                                                              |      |
|     CodeGeeX      |  13B  | 2022-06 | 多语 | 代码 | [申请](https://models.aminer.cn/codegeex/download/request) |        [CodeGeeX](https://github.com/THUDM/CodeGeeX)         |             [清华大学](https://github.com/THUDM)             |  CD  |       [blog](https://models.aminer.cn/codegeex/blog/)        |      |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## ChatLLM

> 具备问答和对话等功能的大型语言模型。
>

|           模型           |    大小     | 时间    | 语言 | 领域 |                             下载                             |                           项目地址                           |                          机构/个人                           | 架构 |                             文献                             |
| :----------------------: | :---------: | ------- | :--: | :--: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :--: | :----------------------------------------------------------: |
|       GLM-4.6        | A32/355B | 2025-10 | 中英 |   通用   | [**Hugging Face**](https://huggingface.co/zai-org/GLM-4.5-Base) | [GLM-4.5](https://github.com/zai-org/GLM-4.5) |     [zai-org](https://github.com/zai-org)     | MoE  | [technical blog](https://z.ai/blog/glm-4.6) |
|     **Ling-1T**      |    1T    | 2025-10 | 多语 |   通用   | [**🤗 Huggingface** ](https://huggingface.co/inclusionAI/Ling-1T) |                       /                       | [inclusionAI](https://github.com/inclusionAI) |  CD  |  
| **Qwen3-Next** | A3/80B | 2025-09 | 中英 | 通用 | [**🤗 Huggingface** ](https://huggingface.co/Qwen/Qwen3-Next-80B-A3B-Instruct) | [Qwen3](https://github.com/QwenLM/Qwen3) | [QwenLM](https://github.com/QwenLM) | MoE  | [Qwen3-Next](https://qwen.ai/blog?id=4074cca80393150c248e508aa62983f9cb7d27cd&from=research.latest-advancements-list) |
|   Kimi-k2   | A32B/1T | 2025-08 | 中英 | 通用 |   [HF](https://huggingface.co/moonshotai/Kimi-K2-Instruct)   |   [Kimi-K2](https://github.com/MoonshotAI/Kimi-K2)   | [MoonshotAI](https://github.com/MoonshotAI) | MoE  | **[Paper](https://github.com/MoonshotAI/Kimi-K2/blob/main/tech_report.pdf)** |
| ERNIE-4.5 | A47/300B  A3/21B | 2025-07 | 中英 | 通用 | [**🤗 Huggingface** ](https://huggingface.co/Skywork/Skywork-SWE-32B) |    /     | [BaiDu](https://huggingface.co/baidu) | MoE  | [Technical Report](https://www.arxiv.org/pdf/2506.19290) |
| Qwen-3 | 4/14/30/235B | 2025-05 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/Qwen/qwen3-67dd247413f0e2e4f653967f) |  [Qwen3](https://github.com/QwenLM/Qwen3)  |     [QwenLM](https://github.com/QwenLM)     | CD/MoE |         [blog](https://qwenlm.github.io/blog/qwen3/)         |
|  MiMo  |      7B      | 2025-05 | 中英 | 通用 |           [🤗HF](https://huggingface.co/XiaomiMiMo)           | [MiMo](https://github.com/XiaomiMiMo/MiMo) | [XiaomiMiMo](https://github.com/XiaomiMiMo) |   CD   | [Paper](https://github.com/XiaomiMiMo/MiMo/blob/main/MiMo-7B-Technical-Report.pdf) |
| GLM-4-0414 | 9/32B | 2025-04 | 多语 | 通用 | [🤗HF](https://huggingface.co/collections/THUDM/glm-4-0414-67f3cbcb34dd9d252707cb2e) | [GLM-4](https://github.com/THUDM/GLM-4) | [THUDM](https://github.com/THUDM) |      |      |
| **Moonlight** | A3/16B | 2025-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/moonshotai/Moonlight-16B-A3B) | [Moonlight](https://github.com/MoonshotAI/Moonlight) | [MoonshotAI](https://github.com/MoonshotAI) |  MoE  | [**Tech Report**](https://github.com/MoonshotAI/Moonlight/blob/master/Moonlight.pdf) |
|   phi-4   | 14B  | 2025--01 | 多语 | 通用 |        [🤗HF](https://huggingface.co/microsoft/phi-4)         |                        /                         | [Microsoft](https://huggingface.co/microsoft) |  CD  | [Phi-4 Technical Report](https://arxiv.org/pdf/2412.08905) |
| InternLM3 |  8B  | 2025--01 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/internlm/internlm3-67875827c377690c01a9131d) | [InternLM](https://github.com/InternLM/InternLM) |    [InternLM](https://github.com/InternLM)    |  CD  |    [Technical Report](https://arxiv.org/abs/2403.17297)    |
| deepseek-v3 | 671B | 2024-12 | 多语 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V3) | [DeepSeek-V3](https://github.com/deepseek-ai/DeepSeek-V3) | [deepseek-ai](https://github.com/deepseek-ai) | MoE  | [**Paper Link**](https://github.com/deepseek-ai/DeepSeek-V3/blob/main/DeepSeek_V3.pdf) |
| Megrez-3B-Instruct |  3B  | 2024-12 | 中英 | 通用 | [🤗HF](https://huggingface.co/Infinigence/Megrez-3B-Instruct) | [Infini-Megrez](https://github.com/infinigence/Infini-Megrez) | [infinigence](https://github.com/infinigence) |  CD  |      |
| Athene-V2-Chat  | 72B  | 2024-11 | 中英 |   通用   | [🤗HF](https://huggingface.co/Nexusflow/Athene-V2-Chat)  |    /     | [Nexusflow](https://huggingface.co/Nexusflow) |  CD  | [Blog](https://nexusflow.ai/blogs/athene-v2) |
| Athene-V2-Agent | 72B  | 2024-11 | 中英 | 工具调用 | [🤗HF](https://huggingface.co/Nexusflow/Athene-V2-Agent) |    /     | [Nexusflow](https://huggingface.co/Nexusflow) |  CD  | [Blog](https://nexusflow.ai/blogs/athene-v2) |
| Hunyuan-Large | A52/389B | 2024-11 | 中英 | 通用 | [🤗HF](https://huggingface.co/tencent/Tencent-Hunyuan-Large) | [Tencent-Hunyuan-Large](https://github.com/Tencent/Tencent-Hunyuan-Large) | [Tencent](https://github.com/Tencent) | MoE  | [Paper](https://arxiv.org/abs/2411.02265) |
| Aya-Expanse | 8/32B | 2024-10 | 多语 | 通用 | [🤗HF](https://huggingface.co/collections/CohereForAI/c4ai-aya-expanse-671a83d6b2c07c692beab3c3) |    /     | [Cohere For AI](https://huggingface.co/CohereForAI) |  CD  |      |
|   Granite 3.0   |  1/2/3/8B   | 2024-10 | 多语 | 通用 | [🤗HF](https://huggingface.co/collections/ibm-granite/granite-30-models-66fdb59bbb54785c3512114f) | [granite-3.0-language-models](https://github.com/ibm-granite/granite-3.0-language-models) | [ibm-granite](https://github.com/ibm-granite) |  CD  | [Paper](https://github.com/ibm-granite/granite-3.0-language-models/blob/main/paper.pdf) |
| Granite 3.0-MoE | 1B/3B/A400M | 2024-10 | 多语 | 通用 | [🤗HF](https://huggingface.co/collections/ibm-granite/granite-30-models-66fdb59bbb54785c3512114f) | [granite-3.0-language-models](https://github.com/ibm-granite/granite-3.0-language-models) | [ibm-granite](https://github.com/ibm-granite) | MoE  | [Paper](https://github.com/ibm-granite/granite-3.0-language-models/blob/main/paper.pdf) |
| TeleChat2 | 115B | 2024-09 | 中英 | 通用 | 🤖 [ModelScope](https://modelscope.cn/organization/TeleAI) | [TeleChat2](https://github.com/Tele-AI/TeleChat2) | [Tele-AI](https://github.com/Tele-AI) |  CD  |      |
| Qwen-2.5 | 0.5/1.5/3/7/14/32/72B | 2024-09 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-66e81a666513e518adb90d9e) | [Qwen2.5](https://github.com/QwenLM/Qwen2.5) | [QwenLM](https://github.com/QwenLM) |  CD  | [Blog](https://qwenlm.github.io/blog/qwen2.5/) |
| XVERSE-MoE | 255B/A36B | 2024-09 | 中英 | 通用 | [🤗HF](https://huggingface.co/xverse/XVERSE-MoE-A36B) | [XVERSE-MoE-A36B](https://github.com/xverse-ai/XVERSE-MoE-A36B) | [xverse-ai](https://github.com/xverse-ai) | MoE  |      |
| DeepSeek-V2.5 | 236B/A21B | 2024-09 | 中英 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V2-Chat-0628) | [DeepSeek-V2](https://github.com/deepseek-ai/DeepSeek-V2) | [deepseek-ai](https://github.com/deepseek-ai) | MOE  |          [Paper](https://arxiv.org/abs/2405.04434)           |
|   MiniCPM3    |    4B     | 2024-09 | 中英 | 通用 |      [🤗HF](https://huggingface.co/openbmb/MiniCPM3-4B)       |       [MiniCPM](https://github.com/OpenBMB/MiniCPM)       |     [OpenBMB](https://github.com/OpenBMB)     |  CD  |      [MiniCPM Paper](https://arxiv.org/abs/2404.06395)       |
| C4AI Command R+ 08-2024 | 104B | 2024-08 | 多语 | 通用 | [🤗HF](https://huggingface.co/CohereForAI) | / | [CohereForAI](https://huggingface.co/CohereForAI) | CD | |
| JIUTIAN-Chat | 39/A13B | 2024-07 | 中英 | 通用 | [🤖MS](https://modelscope.cn/models/JiuTian-AI/JIUTIAN-139MoE-chat) | / | [中国移动JiuTian-AI](https://modelscope.cn/organization/JiuTian-AI) | MOE  |      |
| meta-llama-3.1 | 8/70/405B | 2024-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/meta-llama)| [llama3](https://github.com/meta-llama/llama3) | [meta-llama](https://github.com/meta-llama) |  CD  |      |
| internlm2.5-chat |  7B  | 2024-07 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/internlm) | [InternLM](https://github.com/InternLM/InternLM)[](https://camo.githubusercontent.com/f330929a514fa88e296d3f4aa78863614ccc13d6d1903e4d7b23fd85b69cddba/68747470733a2f2f696d672e736869656c64732e696f2f6769746875622f73746172732f496e7465726e4c4d2f496e7465726e4c4d2e7376673f7374796c653d736f6369616c266c6162656c3d53746172) | [InternLM](https://github.com/InternLM) |  CD  | [📜Technical Report](https://arxiv.org/abs/2403.17297) |
| Mistral-large-insruct-2407 | 123B  | 2024-07 | 多语 | 通用 | [🤗HF](https://huggingface.co/mistralai/Mistral-Large-Instruct-2407) |                             /                             |  [Mistral AI](https://huggingface.co/mistralai)   |      |   [blog post](https://mistral.ai/news/mistral-large-2407/)   |
|   DeepSeek-V2-Chat-0628    | 236B  | 2024-07 | 中英 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V2-Chat-0628) | [DeepSeek-V2](https://github.com/deepseek-ai/DeepSeek-V2) |   [deepseek-ai](https://github.com/deepseek-ai)   | MOE  | [Paper](https://github.com/deepseek-ai/DeepSeek-V2/blob/main/deepseek-v2-tech-report.pdf) |
|    C4ai-command-r-plus     | 104B  | 2024-07 | 多语 | 通用 | [🤗HF](https://huggingface.co/CohereForAI/c4ai-command-r-plus) |                             /                             | [CohereForAI](https://huggingface.co/CohereForAI) |  CD  |                                                              |
|        Gemma-2-chat        | 9/27B | 2024-06 | 多语 | 通用 | [🤗HF](https://huggingface.co/collections/google/gemma-2-release-667d6600fd5220e7b967f315) |                             /                             |      [Google](https://huggingface.co/google)      |  CD  |                                                              |
| MAP-NEO-Chat | 2/7B | 2024-06 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/m-a-p/neo-models-66395a5c9662bb58d5d70f04) | [MAP-NEO](https://github.com/multimodal-art-projection/MAP-NEO) | [multimodal-art-projection](https://github.com/multimodal-art-projection) |  CD  | [Paper](https://arxiv.org/abs/2405.19327) |
| GEB-Chat | 1.3B | 2024-06 | 中英 | 通用 | [🤗HF](https://huggingface.co/GEB-AGI/geb-1.3b) |    /     | [GEB-AGI](https://huggingface.co/GEB-AGI) |  CD  | [Paper](https://arxiv.org/pdf/2406.09900) |
| Nemotron-4-Chat | 340B | 2024-06 | 多语 | 通用 | [🤗HF](https://huggingface.co/nvidia) |    /     | [NVIDIA](https://github.com/NVIDIA) |  CD  | [technical report](https://research.nvidia.com/publication/2024-06_nemotron-4-340b). |
| Index-Chat | 1.9B | 2024-06 | 中英 | 通用 | [🤗HF](https://huggingface.co/IndexTeam/Index-1.9B-Chat) | [Index-1.9B](https://github.com/bilibili/Index-1.9B) | [bilibili](https://github.com/bilibili) |  CD  | [Report](https://github.com/bilibili/Index-1.9B/blob/main/Index-1.9B%20%E6%8A%80%E6%9C%AF%E6%8A%A5%E5%91%8A.pdf) |
| Qwen2-MoE  |   57B/A14B    | 2024-06 | 多语 | 通用 | [🤗HF](https://huggingface.co/Qwen) | [Qwen2](https://github.com/QwenLM/Qwen2) | [QwenLM](https://github.com/QwenLM) | MoE  | [Blog](https://qwenlm.github.io/) |
| Qwen2-Chat | 0.5/2/5/7/72B | 2024-06 | 多语 | 通用 | [🤗HF](https://huggingface.co/Qwen) | [Qwen2](https://github.com/QwenLM/Qwen2) | [QwenLM](https://github.com/QwenLM) |  CD  | [Blog](https://qwenlm.github.io/) |
| GLM-4-Chat  |      9B      | 2024-06 | 多语 | 通用 |          [🤗HF](https://huggingface.co/THUDM)           |         [GLM-4](https://github.com/THUDM/GLM-4)         |     [THUDM](https://github.com/THUDM)      |  /   |   |
| Skywork-MoE | 16/A22B/146B | 2024-06 | 中英 | 通用 | [🤗HF](https://huggingface.co/Skywork/Skywork-MoE-Base) | [Skywork-MoE](https://github.com/SkyworkAI/Skywork-MoE) | [SkyworkAI](https://github.com/SkyworkAI)  | MoE  | [Tech Report](https://github.com/SkyworkAI/Skywork-MoE/blob/main/skywork-moe-tech-report.pdf) |
| Yuan2.0 | 40/A3.7B | 2024-05 | 中英 | 通用 | [🤗HF](https://huggingface.co/IEITYuan/Yuan2-M32-hf) | [Yuan2.0-M32](https://github.com/IEIT-Yuan/Yuan2.0-M32) | [IEIT-Yuan](https://github.com/IEIT-Yuan) | MOE  | [Paper](https://arxiv.org/abs/2405.17976) |
| 星辰-Chat |  52B  | 2024-05 | 中英 | 通用 |    [🤗HF](https://hf-mirror.com/Tele-AI/TeleChat-52B)     | [TeleChat-52B](https://github.com/Tele-AI/TeleChat-52B) |    [Tele-AI](https://github.com/Tele-AI)    |  CD  |                                               |
| LingLong  | 317M  | 2024-05 | 中英 | 通用 |  [🤗HF](https://hf-mirror.com/AlumiK/LingLong-317M-Chat)  |   [linglong](https://github.com/nkcs-iclab/linglong)    | [nkcs-iclab](https://github.com/nkcs-iclab) |  CD  |                                               |
|  Sailor   |  14B  | 2024-05 | 7语  | 通用 |    [🤗HF](https://hf-mirror.com/sail/Sailor-14B-Chat)     |   [sailor-llm](https://github.com/sail-sg/sailor-llm)   |    [sail-sg](https://github.com/sail-sg)    |  CD  | [Paper](https://arxiv.org/pdf/2404.03608.pdf) |
| Nanbeige2 | 8/16B | 2024-05 | 中英 | 通用 | [🤗HF](https://hf-mirror.com/Nanbeige/Nanbeige2-16B-Chat) |    [Nanbeige](https://github.com/Nanbeige/Nanbeige)     |   [Nanbeige](https://github.com/Nanbeige)   |  CD  |                                               |
| Yi-1.5-Chat | 6/9/34B | 2024-05 | 中英  | 通用  | [🤗HF](https://huggingface.co/01-ai) | [Yi-1.5](https://github.com/01-ai/Yi-1.5) | [01-ai](https://github.com/01-ai) | CD  | [Paper](https://arxiv.org/abs/2403.04652) |
| DeepSeek-V2-Chat | A21B/236B | 2024-05 | 中英 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V2-Chat) | [DeepSeek-V2](https://github.com/deepseek-ai/DeepSeek-V2) | [deepseek-ai](https://github.com/deepseek-ai) | MOE | [Paper](https://github.com/deepseek-ai/DeepSeek-V2/blob/main/deepseek-v2-tech-report.pdf) |
| XVERSE-MoE | A4.2B/25.8B | 2024-05 | 中英 | 通用 | [🤗HF](https://huggingface.co/xverse/XVERSE-MoE-A4.2B) | [XVERSE-MoE-A4.2B](https://github.com/xverse-ai/XVERSE-MoE-A4.2B) |[xverse-ai](https://github.com/xverse-ai)|MOE||
| Llama3-zh | 8/70B | 2024-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/xianbao/llama3-zh-662ba8503bdfe51948a28403) | / |/|CD|llama3中文列表|
| Llama3-Chinese-Chat | 8B | 2024-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/shenzhi-wang/Llama3-8B-Chinese-Chat) | / |[Shenzhi Wang](https://huggingface.co/shenzhi-wang)|CD||
| Llama-3-Chat | 8/70B | 2024-04 | 多语 | 通用 | [🤗HF](https://hf-mirror.com/meta-llama) | **[llama3](https://github.com/meta-llama/llama3)** |[Meta Llama](https://github.com/meta-llama)|CD||
| Zhinao-Chat | 7B | 2024-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/qihoo360) [ 🤖](https://www.modelscope.cn/models/qihoo360/360Zhinao-7B-Base/summary) | / |[奇虎科技](https://huggingface.co/qihoo360)|CD||
| MiniCPM-MoE | 8x2B | 2024-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/openbmb/MiniCPM-MoE-8x2B) | [MiniCPM](https://github.com/OpenBMB/MiniCPM) |[OpenBMB](https://github.com/OpenBMB)|MoE||
| Nanbeige2-Chat | 8B | 2024-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/Nanbeige/Nanbeige2-8B-Chat) | [Nanbeige](https://github.com/Nanbeige/Nanbeige) |[Nanbeige LLM Lab](https://github.com/Nanbeige)|CD||
| Sailor | 7B | 2024-04 | 多语 | 通用 | [🤗HF](https://huggingface.co/sail/Sailor-4B-Chat) | [sailor-llm](https://github.com/sail-sg/sailor-llm) |[Sea AI Lab](https://github.com/sail-sg)|CD|[Paper](https://arxiv.org/pdf/2404.03608.pdf)|
| Mengzi3-Chat | 13B  | 2024-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/Langboat) | [Mengzi3](https://github.com/Langboat/Mengzi3)  | [Langboat](https://github.com/Langboat) |  CD  |  |
| Qwen-MoE | 2.7B | 2024-03 | 中英 | 通用 | [🤗HF](https://huggingface.co/Qwen/Qwen1.5-MoE-A2.7B-Chat) | [Qwen1.5](https://github.com/QwenLM/Qwen1.5)  | [Qwen](https://github.com/QwenLM) | MoE | [Blog](https://qwenlm.github.io/zh/blog/qwen-moe/) |
| Command-R | 35B | 2024-03 | 多语 | 通用 | [🤗HF](https://huggingface.co/CohereForAI) | / | [CohereForAI](https://huggingface.co/CohereForAI) | CD | |
| Breeze-Instruct | 7B | 2024-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/MediaTek-Research) | / | [MediaTek Research](https://huggingface.co/MediaTek-Research) |  |  |
| aya-101 | 13B | 2024-02 | 多语 | 通用 | [🤗HF](https://hf-mirror.com/CohereForAI/aya-101) | / | [Cohere For AI](https://hf-mirror.com/CohereForAI/aya-101/blob/main/(https://cohere.for.ai)) | CD | [Paper](https://arxiv.org/abs/2402.07827) |
| ChemLLM | 7B | 2024-02 | 多语 | 通用 | [🤗HF](https://hf-mirror.com/CohereForAI/aya-101) | / | [AI4Chem](https://hf-mirror.com/AI4Chem) | CD | [Paper](https://arxiv.org/abs/2402.06852) |
| TowerInstruct | 7/13B | 2024-02 | 多语 | 通用 | [[🤗HF\]](https://hf-mirror.com/Unbabel) | / | [Unbabel](https://hf-mirror.com/Unbabel) | CD |  |
| Qwen1.5-Chat | 0.5/1.8/4/<br/>7/14/32/72/110B | 2024-02 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/Qwen) | [Qwen1.5](https://github.com/QwenLM/Qwen1.5) | [Qwen](https://github.com/QwenLM) | / | [Blog](https://qwenlm.github.io/zh/blog/qwen1.5/) |
| MiniCPM | 2B | 2024-02 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/openbmb) [ModelScope](https://modelscope.cn/organization/OpenBMB) | [MiniCPM](https://github.com/OpenBMB/MiniCPM) | [OpenBMB](https://github.com/OpenBMB) | / | [Report](https://shengdinghu.notion.site/MiniCPM-c805a17c5c8046398914e47f0542095a) |
| **LongAlign-Chat** | 6/7/13B | 2024-02 | 中英 | 通用 | [[🤗HF\]](https://hf-mirror.com/THUDM) | [LongAlign](https://github.com/THUDM/LongAlign) | [THUDM](https://github.com/THUDM) | / | [Paper](https://arxiv.org/abs/2401.18058) |
| Chinese-Mixtral-Chat | 8x7B | 2024-02 | 中英 | 通用 | [[Baidu\]](https://pan.baidu.com/s/1nwJ8JkMTUrCkDEccg7C9Pw?pwd=33kb) [[🤗HF\]](https://huggingface.co/hfl/chinese-mixtral) | [Chinese-Mixtral](https://github.com/ymcui/Chinese-Mixtral) | [Yiming Cui](https://github.com/ymcui) | MOE |  |
| iFlytekSpark-Chat | 13B | 2024-01 | 中英 | 通用 | [mindspore](https://xihe.mindspore.cn/modelzoo/iflytek/introduce) | / | [科大讯飞]() | CD |  |
| rwkv-5-world | 0.1/1/<br/>3/7B | 2023-01 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/BlinkDL) | [RWKV-LM](https://github.com/BlinkDL/RWKV-LM) | [BlinkDL](https://github.com/BlinkDL) |  | [URL](https://wiki.rwkv.com/) |
| Orion-Chat | 14B | 2024-01 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/OrionStarAI) | [Orion](https://github.com/OrionStarAI/Orion) | [OrionStarAI](https://github.com/OrionStarAI) | CD | [Paper](https://github.com/OrionStarAI/Orion/blob/master/doc/Orion14B_v3.pdf) |
| internlm2-chat | 7/20B | 2024-01 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/internlm) | [InternLM](https://github.com/InternLM/InternLM) | [InternLM](https://github.com/InternLM) | CD | [Report](https://github.com/InternLM/InternLM/issues/new) |
| Chinese-Mixtral | 8x7B | 2023-01 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/HIT-SCIR/Chinese-Mixtral-8x7B) | / | [HIT-SCIR](https://huggingface.co/HIT-SCIR) | CD-MOE |  |
| Telechat | 7/12B | 2024-01 | 中英 | 通用 | [[🤗HF\]](https://hf-mirror.com/Tele-AI) | [Telechat](https://github.com/Tele-AI/Telechat)x  | [Tele-AI](https://github.com/Tele-AI) | CD | [Report](https://arxiv.org/abs/2401.03804) |
| kagentlms | 7/13B | 2024-01 | 中英 | 通用 | [[🤗HF\]](https://hf-mirror.com/kwaikeg) | [KwaiAgents](https://github.com/KwaiKEG/KwaiAgents) | [KwaiKEG](https://github.com/KwaiKEG) |  |  |
|  YaYi2-Chat  |   30B    | 2023-12 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/wenge-research) | [YAYI2](https://github.com/wenge-research/YAYI2) | [wenge-research](https://github.com/wenge-research) |  CD  | [Paper](https://arxiv.org/abs/2312.14862) |
| SUS-Chat | 34/72B | 2023-12 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/SUSTech) | [SUS-Chat](https://github.com/SUSTech-IDEA/SUS-Chat) | [SUSTech-IDEA](https://github.com/SUSTech-IDEA) | CD |  |
| Aquila2-Chat | 7/34/70B | 2023-12 | 中英 | 通用 |  [[🤗HF\]](https://huggingface.co/BAAI)   | [Aquila2](https://github.com/FlagAI-Open/Aquila2)  |    [FlagAI](https://github.com/FlagAI-Open)     |  CD  |  |
| Alaya-Chat | 7B | 2023-12 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/DataCanvas) | [Alaya](https://github.com/DataCanvasIO/Alaya) | [DataCanvas](https://github.com/DataCanvasIO) | CD |  |
| Qwen-Chat | 1.8/7/<br/>14/72B | 2023-12 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/Qwen) | [Qwen](https://github.com/QwenLM/Qwen)  | [阿里云](https://github.com/QwenLM) |  CD  | [Paper](https://arxiv.org/abs/2309.16609) [Report](https://github.com/QwenLM/Qwen-7B/blob/main/tech_memo.md) [Report2](https://qianwen-res.oss-cn-beijing.aliyuncs.com/QWEN_TECHNICAL_REPORT.pdf) |
| DeepSeek-Chat | 7/67B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/deepseek-ai) | [DeepSeek-LLM](https://github.com/deepseek-ai/DeepSeek-LLM) | [deepseek-ai](https://github.com/deepseek-ai) | CD |  |
| Yi-Chat | 6/34B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/01-ai) | [Yi](https://github.com/01-ai/Yi)  | [01.AI](https://github.com/01-ai) | CD |  |
| Alaya-Chat | 7B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/DataCanvas/Alaya-7B-Chat) | [Alaya](https://github.com/DataCanvasIO/Alaya) | [DataCanvasIO](https://github.com/DataCanvasIO) | CD |  |
| OrionStar-Yi-Chat | 34B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/OrionStarAI/OrionStar-Yi-34B-Chat) | [OrionStar-Yi-34B-Chat](https://github.com/OrionStarAI/OrionStar-Yi-34B-Chat) | [OrionStarAI](https://github.com/OrionStarAI) | CD |  |
| Nanbeige-Chat | 16B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/Nanbeige) | [Nanbeige](https://github.com/Nanbeige/Nanbeige) | [Nanbeige LLM Lab](https://github.com/Nanbeige) | CD |  |
| OpenChat 3.5 | 7B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/openchat/openchat_3.5) | [openchat](https://github.com/imoneoi/openchat) | [OpenChat](https://github.com/imoneoi) | CD | [Paper](https://arxiv.org/pdf/2309.11235.pdf) |
|          XVERSE-Chat    |     7/13B     | 2023-11 | 多语 | 通用 |       [[🤗HF\]](https://huggingface.co/xverse)       | [XVERSE](https://github.com/xverse-ai/XVERSE-13B) |           [元象科技](https://github.com/xverse-ai)           |  CD  |                                                              |
| AndesGPT | 7B | 2023-11 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/OPPOResearchInstitute/AndesGPT-7B) | [AndesGPT-7B](https://github.com/OPPO-Mente-Lab/AndesGPT-7B) | [OPPO-Mente-Lab](https://github.com/OPPO-Mente-Lab) | CD |  |
| SeaLLM-Chat | 13B  | 2023-11 | 多语 | 通用 |    [[🤗HF\]](https://huggingface.co/SeaLLMs/SeaLLM-Chat-13b)    |        [SeaLLMs](https://github.com/SeaLLMs/SeaLLMs)         |        [SeaLLMs](https://github.com/SeaLLMs)        |  CD  |  |
| BlueLM | 7B | 2023-11 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/vivo-ai) | [BlueLM](https://github.com/vivo-ai-lab/BlueLM) | [vivo AI Lab](https://github.com/vivo-ai-lab) | CD |  |
| Skywork-chat | 13B  | 2023-10 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/Skywork) | [Skywork](https://github.com/SkyworkAI/Skywork) |   [SkyworkAI](https://github.com/SkyworkAI)   |  CD  | [Paper](https://arxiv.org/abs/2310.16713) |
| Zephyr | 7B | 2023-10 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/HuggingFaceH4/zephyr-7b-beta) | [alignment-handbook](https://github.com/huggingface/alignment-handbook) | [Hugging Face H4](https://huggingface.co/HuggingFaceH4) | CD | [Paper](https://arxiv.org/abs/2310.16944) |
| Mistral | 7B | 2023-10 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/mistralai) | [mistral-src](https://github.com/mistralai/mistral-src) | [Mistral AI](https://github.com/mistralai) | CD | [Paper](https://arxiv.org/abs/2310.06825) |
| chatglm3 | 6B | 2023-10 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/THUDM) | [ChatGLM3](https://github.com/THUDM/ChatGLM3) | [THUDM](https://github.com/THUDM) | ND |  |
| Zhiyin-chat | 7B | 2023-10 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/HCCL-NLP/Zhiyin-7B-Chat) | [Zhiyin](https://github.com/HCCL-NLP/Zhiyin) | [中科院声学所](https://github.com/HCCL-NLP) | CD |  |
|        Ziya2-Chat        |     13B     | 2023-10 | 中英 | 通用 | [[🤗HF\]](https://modelscope.cn/models/Fengshenbang/Ziya2-13B-Chat/summary) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) |          [IDEA研究院](https://github.com/IDEA-CCNL)          |  CD  |                                                              |
|         Vulture          |   40/180B   | 2023-10 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/vilm/vulture-40b) |                              /                               |            [VILM-AI](https://huggingface.co/vilm)            |      |                           [TODO]()                           |
|         Vulture          | 3/7/<br/>40/180B | 2023-09 | 多语 | 通用 |             [[🤗HF\]](https://huggingface.co/vilm)              |                              /                               |                [VILM](https://www.vilm.org/)                 |  CD  |                                                              |
|     Colossal-LLaMA-2     |     7B      | 2023-09 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/hpcai-tech/Colossal-LLaMA-2-7b-base) | [ColossalAI](https://github.com/hpcaitech/ColossalAI) |         [HPC-AI Tech](https://github.com/hpcaitech)          |  CD  | [Blog](https://www.hpc-ai.tech/blog/one-half-day-of-training-using-a-few-hundred-dollars-yields-similar-results-to-mainstream-large-models-open-source-and-commercial-free-domain-specific-llm-solution) |
|       OpenBA-chat        |     15B     | 2023-09 | 中英 | 通用 |                           [TODO]()                           | [OpenBA](https://github.com/OpenNLG/OpenBA) |         [OpenNLG Group](https://github.com/OpenNLG)          |  ED  |          [Paper](https://arxiv.org/abs/2309.10706)           |
|       WeMix-LLaMA2       |    7/70B    | 2023-09 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/Alpha-VLLM/WeMix-LLaMA2-7B) | [WeMix-LLM](https://github.com/Alpha-VLLM/WeMix-LLM) |         [Alpha-VLLM](https://github.com/Alpha-VLLM)          |  CD  |                                                              |
|      Stable Beluga       |  7/13/70B   | 2023-09 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/stabilityai/StableBeluga-7B) |                              /                               |       [Stability AI](https://github.com/Stability-AI)        |  CD  |                                                              |
|      TigerBot-chat       |     70B     | 2023-09 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/TigerResearch/tigerbot-70b-chat) | [TigerBot](https://github.com/TigerResearch/TigerBot)  |         [虎博科技](https://github.com/TigerResearch)         |  CD  | [Paper](https://github.com/TigerResearch/TigerBot/wiki/TigerBot%E2%80%9070B%E5%8F%91%E5%B8%83%EF%BC%81) |
|     Openbuddy_llama      |     70B     | 2023-09 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/OpenBuddy/openbuddy-llama2-70b-v10.1-bf16) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy) |          [OpenBuddy](https://github.com/OpenBuddy)           |  CD  |                                                              |
|     falcon-180B-chat     |    180B     | 2023-09 | 多语 | 通用 |    [[🤗HF\]](https://huggingface.co/tiiuae/falcon-180B-chat)    |                              /                               | [Technology Innovation Institute](https://github.com/tiiuae) |  CD  |                                                              |
|        Baichuan2         |    7/13B    | 2023-09 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/baichuan-inc/Baichuan2-7B-Chat) | [Baichuan2](https://github.com/baichuan-inc/Baichuan2) |         [百川智能](https://github.com/baichuan-inc)          |  CD  |                                                              |
|   Chinese-Alpaca-2-16K   |    7/13B    | 2023-09 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/ziqingyang/chinese-alpaca-2-7b-16k) | [Chinese-LLaMA-Alpaca-2](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |
|     InternLM-Chat-8k     |     7B      | 2023-08 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/internlm/internlm-chat-7b-8k)  | [InternLM](https://github.com/InternLM/InternLM) |      [上海人工智能实验室](https://github.com/InternLM)       |  CD  | [report](https://github.com/InternLM/InternLM-techreport/tree/main) |
|    InternLM-Chat-v1.1    |     7B      | 2023-08 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/internlm/internlm-chat-7b-v1_1) | [InternLM](https://github.com/InternLM/InternLM) |      [上海人工智能实验室](https://github.com/InternLM)       |  CD  | [report](https://github.com/InternLM/InternLM-techreport/tree/main) |
|       YuLan-Chat-2       |     13B     | 2023-08 | 中英 | 通用 |  [[🤗HF\]](https://huggingface.co/yulan-team/YuLan-Chat-2-13b)  | [YuLan-Chat](https://github.com/RUC-GSAI/YuLan-Chat) |         [中国人民大学](https://github.com/RUC-GSAI)          |  CD  |                                                              |
|          falcon          |    7/40B    | 2023-06 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/tiiuae/falcon-7b) |         [[🤗HF\]](https://huggingface.co/tiiuae)         | [Technology Innovation Institute](https://github.com/tiiuae) |  CD  |                                                              |
|          Toucan          |     7B      | 2023-08 | 中英 | 通用 | [[🤗HF\]](https://1drv.ms/f/s!Ar5igoMgwOq4gdowvr5NQDHOQp2OxQ?e=dzYSuE) | [Toucan-LLM](https://github.com/kendryte/Toucan-LLM) |           [Kendryte](https://github.com/kendryte)            |  CD  |                                                              |
|          Zhuzhi          |     6B      | 2023-08 | 中英 | 通用 |    [[🤗HF\]](https://huggingface.co/emotibot-inc/Zhuzhi-6B)     | [Zhuzhi-6B](https://github.com/emotibot-inc/Zhuzhi-6B) |         [竹间智能](https://github.com/emotibot-inc)          |  ND  |                                                              |
|           Atom           |     7B      | 2023-08 | 中英 | 通用 |       [[🤗HF\]](https://huggingface.co/FlagAlpha/Atom-7B)       | [Llama2-Chinese](https://github.com/FlagAlpha/Llama2-Chinese) |          [FlagAlpha](https://github.com/FlagAlpha)           |  CD  |                                                              |
|        openbuddy         | 3/7/<br/>13/40B | 2023-08 | 多语 | 通用 | [[🤗HF\]](https://github.com/OpenBuddy/OpenBuddy/blob/main/models.md) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy) |          [OpenBuddy](https://github.com/OpenBuddy)           |  CD  |                                                              |
|     Aquila-Chat-33B      |     33B     | 2023-08 | 中英 | 通用 |                           [TODO]()                           | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila) |           [FlagAI](https://github.com/FlagAI-Open)           |  CD  |                                                              |
|     vicuna-V1.5-16K      |    7/13B    | 2023-08 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/lmsys/vicuna-7b-v1.5-16k) | [FastChat](https://github.com/lm-sys/FastChat) |             [lm-sys](https://github.com/lm-sys)              |  CD  |          [Paper](https://arxiv.org/abs/2306.05685)           |
|       vicuna-V1.5        |    7/13B    | 2023-08 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/lmsys/vicuna-7b-v1.5) | [FastChat](https://github.com/lm-sys/FastChat) |             [lm-sys](https://github.com/lm-sys)              |  CD  |          [Paper](https://arxiv.org/abs/2306.05685)           |
|     Chinese-Alpaca-2     |     13B     | 2023-08 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/ziqingyang/chinese-alpaca-2-lora-13b) | [Chinese-LLaMA-Alpaca-2](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |
|      WizardLM-V1.0       |     70B     | 2023-08 | 多语 | 通用 |  [[🤗HF\]](https://huggingface.co/WizardLM/WizardLM-70B-V1.0)   | [WizardLM](https://github.com/nlpxucan/WizardLM) |           [operatorx](https://github.com/nlpxucan)           |  CD  |                                                              |
|    TigerBot-chat-13B     |     13B     | 2023-07 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/TigerResearch/tigerbot-13b-chat) | [TigerBot](https://github.com/TigerResearch/TigerBot) |         [虎博科技](https://github.com/TigerResearch)         |  CD  |                                                              |
|          huozi           |     7B      | 2023-08 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/HIT-SCIR/huozi-7b-sft) | [huozi](https://github.com/HIT-SCIR/huozi) |            [哈工大](https://github.com/HIT-SCIR)             |  CD  |                                                              |
|     Chinese-Alpaca-2     |     7B      | 2023-07 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/ziqingyang/chinese-alpaca-2-7b) | [Chinese-LLaMA-Alpaca-2](https://github.com/ymcui/Chinese-LLaMA-Alpaca-2) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |
|           AntX           |    7/13B    | 2023-07 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/AntX-ai/AntX-7B) |                              /                               |          [AntX.ai](https://huggingface.co/AntX-ai)           |  CD  |                                                              |
|          BatGPT          |     15B     | 2023-07 | 中英 | 通用 |   [[🤗HF\]](https://huggingface.co/MLP-lab/BatGPT-15B-sirius)   | [BatGPT](https://github.com/zcli-charlie/BatGPT) |        [上海交通大学](https://huggingface.co/MLP-lab)        |  ND  |          [Paper](https://arxiv.org/abs/2307.00360)           |
|      WizardLM-V1.2       |     13B     | 2023-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/WizardLM/WizardLM-13B-V1.2) | [WizardLM](https://github.com/nlpxucan/WizardLM) |           [operatorx](https://github.com/nlpxucan)           |  CD  |          [Paper](https://arxiv.org/pdf/2304.12244)           |
|   llama2-Chinese-chat    |     13B     | 2023-07 | 中英 | 通用 | [[🤗HF\]](https://www.codewithgpu.com/m/file/llama2-13b-Chinese-chat) | [llama2-Chinese-chat](https://github.com/CrazyBoyM/llama2-Chinese-chat) |            [Ke Bai](https://github.com/CrazyBoyM)            |  CD  |                                                              |
|        Jiang-chat        |     13B     | 2023-07 | 中文 | 通用 |        [[🤗HF\]](https://huggingface.co/kdf/jiang-chat)         |                              /                               |            [知未智能](https://huggingface.co/kdf)            |  CD  |                                                              |
|   Llama2-chinese-chat    |    7/13B    | 2023-07 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/FlagAlpha/Llama2-Chinese-7b-Chat) | [Llama2-Chinese](https://github.com/FlagAlpha/Llama2-Chinese) |          [FlagAlpha](https://github.com/FlagAlpha)           |  CD  |                                                              |
|           LL7M           |     7B      | 2023-07 | 多语 | 通用 |      [[🤗HF\]](https://huggingface.co/JosephusCheung/LL7M)      |                              /                               |    [Joseph Cheung](https://huggingface.co/JosephusCheung)    |  CD  |                                                              |
|     Chinese-Llama-2      |     7B      | 2023-07 | 中英 | 通用 |  [[🤗HF\]](https://huggingface.co/LinkSoul/Chinese-Llama-2-7b)  | [Chinese-Llama-2-7b](https://github.com/LinkSoul-AI/Chinese-Llama-2-7b) |        [LinkSoul-AI](https://github.com/LinkSoul-AI)         |  CD  |                                                              |
|       Llama2-chat        |  7/13/70B   | 2023-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/llamaste/Llama-2-7b-chat) | [llama](https://github.com/facebookresearch/llama) |         [Meta](https://github.com/facebookresearch)          |  CD  | [Paper](https://scontent-hkg4-1.xx.fbcdn.net/v/t39.2365-6/10000000_663429262362723_1696968207443577320_n.pdf?_nc_cat=101&ccb=1-7&_nc_sid=3c67a6&_nc_ohc=5ol-jUSglG4AX-br54S&_nc_ht=scontent-hkg4-1.xx&oh=00_AfDzh9f2kFTRk-FIieoySi12fhBjvJP4Bv-ZJTxRtdoXJg&oe=64BBB691) |
|       PolyLM-chat        |     13B     | 2023-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/DAMO-NLP-MT/polylm-multialpaca-13b) | [PolyLM](https://modelscope.cn/models/damo/nlp_polylm_13b_text_generation/summary) |         [达摩院](https://huggingface.co/DAMO-NLP-MT)         |  CD  |        [Paper](https://arxiv.org/pdf/2307.06018.pdf)         |
|    Baichuan-13B-chat     |     13B     | 2023-07 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/baichuan-inc/Baichuan-13B-Chat) | [Baichuan-13B](https://github.com/baichuan-inc/Baichuan-13B) |         [百川智能](https://github.com/baichuan-inc)          |  CD  |                                                              |
|       vicuna-V1.3        |  7/13/33B   | 2023-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/lmsys/vicuna-7b-v1.3) | [FastChat](https://github.com/lm-sys/FastChat) |             [lm-sys](https://github.com/lm-sys)              |  CD  |          [Paper](https://arxiv.org/abs/2306.05685)           |
|      WizardLM-V1.0       |  7/13/30B   | 2023-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/WizardLM/WizardLM-7B-V1.0) | [WizardLM](https://github.com/nlpxucan/WizardLM) |           [operatorx](https://github.com/nlpxucan)           |  CD  |          [Paper](https://arxiv.org/pdf/2304.12244)           |
|     TigerBot-v2-sft      |     7B      | 2023-07 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/TigerResearch/tigerbot-7b-sft-v2) | [TigerBot](https://github.com/TigerResearch/TigerBot) |         [虎博科技](https://github.com/TigerResearch)         |  CD  |                                                              |
|      InternLM-chat       |    7/20B    | 2023-07 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/internlm/internlm-chat-7b) | [InternLM](https://github.com/InternLM/InternLM) |      [上海人工智能实验室](https://github.com/InternLM)       |  CD  | [report](https://github.com/InternLM/InternLM-techreport/tree/main) |
|       vicuna汉化版       |     33B     | 2023-07 | 中文 | 通用 | [baidu-hiks](https://pan.baidu.com/s/1EH19ablXVLYQP1f-IaPS-Q?pwd=hiks) | [chinese-StableVicuna](https://github.com/ziwang-com/chinese-StableVicuna) |         [ziwang-com](https://github.com/ziwang-com)          |  CD  |                                                              |
|         CuteGPT          |     13B     | 2023-07 | 中英 | 通用 |  [[🤗HF\]](https://huggingface.co/XuYipei/kw-cutegpt-13b-base)  | [CuteGPT](https://github.com/Abbey4799/CuteGPT) |         [复旦大学知识工场](http://kw.fudan.edu.cn/)          |  CD  |                                                              |
|         MPT-chat         |    7/30B    | 2023-06 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/mosaicml/mpt-7b-chat) | [llm-foundry](https://github.com/mosaicml/llm-foundry) |           [MosaicML](https://github.com/mosaicml)            |  CD  |                                                              |
|         ChatGLM2         |     6B      | 2023-06 | 中英 | 通用 |       [[🤗HF\]](https://huggingface.co/THUDM/chatglm2-6b)       | [ChatGLM2-6B](https://github.com/THUDM/ChatGLM2-6B) |             [清华大学](https://github.com/THUDM)             |  ND  |                                                              |
|         BayLing          |    7/13B    | 2023-06 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/ICTNLP/bayling-13b-v1.1) | [BayLing](https://github.com/ictnlp/BayLing) |           [中国科学院](https://github.com/ictnlp)            |  CD  |                                                              |
|        ZhiXi-Diff        |     13B     | 2023-06 | 中英 | 通用 |     [[🤗HF\]](https://huggingface.co/zjunlp/zhixi-13b-diff)     | [KnowLLM](https://github.com/zjunlp/KnowLM) |            [浙江大学](https://github.com/zjunlp)             |  CD  |                                                              |
|          Anima           |     33B     | 2023-06 | 中文 | 通用 |       [[🤗HF\]](https://huggingface.co/lyogavin/Anima33B)       | [Anima](https://github.com/lyogavin/Anima) |           [Gavin Li](https://github.com/lyogavin)            |  CD  |                                                              |
|    OpenLLaMA-Chinese     |   3/7/13B   | 2023-06 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/FittenTech/openllama-chinese-13b) | [OpenLLaMA-Chinese](https://github.com/FittenTech/OpenLLaMA-Chinese) |         [FittenTech](https://github.com/FittenTech)          |  CD  |                                                              |
| openbuddy-falcon-7b-v1.5 |     7B      | 2023-06 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/OpenBuddy/openbuddy-falcon-7b-v1.5-fp16) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy) |          [OpenBuddy](https://github.com/OpenBuddy)           |  CD  |                                                              |
|       AtomGPT_chat       |     13B     | 2023-06 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/AtomEchoAI/AtomGPT_8k_chat) | [AtomGPT](https://github.com/AtomEcho/AtomGPT) |           [原子回声](https://github.com/AtomEcho)            |  CD  |                                                              |
|        AquilaChat        |     7B      | 2023-06 | 中英 | 通用 |     [[🤗HF\]](https://model.baai.ac.cn/model-detail/100101)     | [Aquila](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/Aquila) |           [FlagAI](https://github.com/FlagAI-Open)           |  CD  |                                                              |
|        YuLan-Chat        |   13/65B    | 2023-06 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/RUCAIBox/YuLan-Chat-65b-delta) | [YuLan-Chat](https://github.com/RUC-GSAI/YuLan-Chat) |         [中国人民大学](https://github.com/RUC-GSAI)          |  CD  |                                                              |
|      Chinese-Alpaca      |     33B     | 2023-06 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/ziqingyang/chinese-alpaca-lora-33b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |
|       TigerBot-sft       |   7/180B    | 2023-06 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/TigerResearch/tigerbot-7b-sft) | [TigerBot](https://github.com/TigerResearch/TigerBot) |         [虎博科技](https://github.com/TigerResearch)         |  CD  |                                                              |
|         ChatYuan         |     7B      | 2023-06 | 中英 | 通用 |   [[🤗HF\]](https://huggingface.co/tiansz/ChatYuan-7B-merge)    | [ChatYuan-7B](https://github.com/clue-ai/ChatYuan-7B) |             [ClueAI](https://github.com/clue-ai)             |  CD  |                                                              |
|      Panda-Instruct      |     13B     | 2023-05 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/chitanda/llama-panda-zh-13b-coig-delta) | [pandallm](https://github.com/dandelionsllm/pandallm) |      [dandelionsllm](https://github.com/dandelionsllm)       |  CD  |                                                              |
|      Panda-Instruct      |     7B      | 2023-05 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/chitanda/llama-panda-zh-coig-7b-delta) | [pandallm](https://github.com/dandelionsllm/pandallm) |      [dandelionsllm](https://github.com/dandelionsllm)       |  CD  |                                                              |
|        BiLLa-SFT         |     7B      | 2023-05 | 中英 | 通用 |    [[🤗HF\]](https://huggingface.co/Neutralzz/BiLLa-7B-SFT)     | [BiLLa](https://github.com/Neutralzz/BiLLa) |          [Zhongli Li](https://github.com/Neutralzz)          |  CD  |                                                              |
|      Ziya-LLaMA-v1       |     13B     | 2023-05 | 中英 | 通用 |  [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1)  | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) |          [IDEA研究院](https://github.com/IDEA-CCNL)          |  CD  |  [Blog](https://mp.weixin.qq.com/s/IeXgq8blGoeVbpIlAUCAjA)   |
|      BLOOMChat V1.0      |    176B     | 2023-05 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/sambanovasystems/BLOOMChat-176B-v1) |     [bloomchat](https://github.com/sambanova/bloomchat)      |          [SambaNova Systems](https://sambanova.ai/)          |  CD  | [Blog](https://sambanova.ai/blog/introducing-bloomchat-176b-the-multilingual-chat-based-llm/) |
|          BiLLa           |     7B      | 2023-05 | 中英 | 通用 |          [[🤗HF\]](https://github.com/Neutralzz/BiLLa)          | [BiLLa](https://github.com/Neutralzz/BiLLa) |          [Zhongli Li](https://github.com/Neutralzz)          |  CD  |                                                              |
|        Bactrian-X        |    7/13B    | 2023-05 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/MBZUAI/bactrian-x-13b-lora) | [bactrian-x](https://github.com/mbzuai-nlp/bactrian-x) |           [MBZUAI](https://github.com/mbzuai-nlp)            |  CD  |                                                              |
|       Bactrian-ZH        |     7B      | 2023-05 | 中文 | 通用 |        [[🤗HF\]](https://huggingface.co/haonan-li)  | [bactrian-x](https://github.com/mbzuai-nlp/bactrian-x) |           [MBZUAI](https://github.com/mbzuai-nlp)            |  CD  |                                                              |
|         ChatFlow         |    7/13B    | 2023-05 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/Linly-AI/ChatFlow-13B) | [Linly](https://github.com/CVI-SZU/Linly) |    [深圳大学计算机视觉研究所](https://github.com/CVI-SZU)    |  CD  |                                                              |
|        OpenBuddy         |    7/13B    | 2023-05 | 多语 | 通用 | [[🤗HF\]](https://github.com/OpenBuddy/OpenBuddy/blob/main/models.md) | [OpenBuddy](https://github.com/OpenBuddy/OpenBuddy) |          [OpenBuddy](https://github.com/OpenBuddy)           |  CD  |                                                              |
|      YuYan-dialogue      |     11B     | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/FUXI/yuyan-dialogue/tree/main) |                              /                               |           [网易伏羲](https://huggingface.co/FUXI)            |  CD  |   [paper](https://aclanthology.org/2022.naacl-industry.8/)   |
| Moss-moon-003-sft-plugin |     16B     | 2023-04 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/fnlp/moss-moon-003-sft-plugin) | [MOSS](https://github.com/OpenLMLab/MOSS) |           [复旦大学](https://github.com/OpenLMLab)           |  CD  |                                                              |
|    moss-moon-003-sft     |     16B     | 2023-04 | 中英 | 通用 |    [[🤗HF\]](https://huggingface.co/fnlp/moss-moon-003-sft)     | [MOSS](https://github.com/OpenLMLab/MOSS) |           [复旦大学](https://github.com/OpenLMLab)           |  CD  |                                                              |
|       RWKV-4-Raven       |   3/7/14B   | 2023-04 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/BlinkDL/rwkv-4-raven/tree/main) | [ChatRWKV](https://github.com/BlinkDL/ChatRWKV) |            [BlinkDL](https://github.com/BlinkDL)             | RNN  |        [Blog](https://zhuanlan.zhihu.com/p/618011122)        |
|    Phoenix-inst-chat     |     7B      | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/FreedomIntelligence/phoenix-inst-chat-7b) | [LLMZoo](https://github.com/FreedomIntelligence/LLMZoo) |    [香港中文大学](https://github.com/FreedomIntelligence)    |  CD  |                                                              |
|       Phoenix-chat       |     7B      | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/FreedomIntelligence/phoenix-chat-7b) | [LLMZoo](https://github.com/FreedomIntelligence/LLMZoo) |    [香港中文大学](https://github.com/FreedomIntelligence)    |  CD  |                                                              |
|         ChatPLUG         |    3.7B     | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://modelscope.cn/models/damo/ChatPLUG-3.7B/summary) | [ChatPLUG](https://github.com/X-PLUG/ChatPLUG) |            [阿里巴巴](https://github.com/X-PLUG)             |  ED  |        [Paper](https://arxiv.org/pdf/2304.07849.pdf)         |
|      Chinese-Alpaca      |     13B     | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/ziqingyang/chinese-alpaca-lora-13b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |
|       BELLE-LLAMA        |     13B     | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/BelleGroup/BELLE-LLaMA-EXT-13B) | [BELLE](https://github.com/LianjiaTech/BELLE) |            [贝壳](https://github.com/LianjiaTech)            |  CD  |                                                              |
|       LLaMA-tuned        | 7/13/<br/>33/65B | 2023-04 | 中文 | 通用 | [[🤗HF\]](https://drive.google.com/file/d/1x5JLae3akVkfFeDhSe3TEyUbPn_GNFyb/view?usp=share_link) | [LMFlow](https://github.com/OptimalScale/LMFlow) |       [香港科技大学](https://github.com/OptimalScale)        |  CD  |                                                              |
|      Chinese-Vicuna      |    7/13B    | 2023-03 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/Chinese-Vicuna/Chinese-Vicuna-lora-13b-belle-and-guanaco) | [Chinese-Vicuna](https://github.com/Facico/Chinese-Vicuna) |             [Facico](https://github.com/Facico)              |  CD  |                                                              |
|       ChatYuan-V2        |    0.7B     | 2023-03 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/ClueAI/ChatYuan-large-v2/tree/main) | [ChatYuan](https://github.com/clue-ai/ChatYuan) |            [元语智能](https://github.com/clue-ai)            |  ED  |                                                              |
|      Chinese-Alpaca      |     7B      | 2023-03 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/ziqingyang/chinese-alpaca-lora-7b) | [Chinese-LLaMA-Alpaca](https://github.com/ymcui/Chinese-LLaMA-Alpaca) |            [Yiming Cui](https://github.com/ymcui)            |  CD  |                                                              |
|          Luotuo          |     7B      | 2023-03 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/silk-road/luotuo-lora-7b-0.3)  | [Chinese-alpaca-lora](https://github.com/LC1332/Chinese-alpaca-lora) |                         华中师范大学                         |  CD  |                                                              |
|       BELLE-LLAMA        |     7B      | 2023-03 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/BelleGroup/BELLE-LLaMA-EXT-7B) | [BELLE](https://github.com/LianjiaTech/BELLE) |            [贝壳](https://github.com/LianjiaTech)            |  CD  |                                                              |
|         ChatGLM          |     6B      | 2023-03 | 中英 | 通用 |       [[🤗HF\]](https://huggingface.co/THUDM/chatglm-6b)        | [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B) |             [清华大学](https://github.com/THUDM)             |  ND  |                                                              |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## Domain-ChatLLM

> 开源的垂直领域对话大模型

|           模型           |  大小   | 时间    | 语言 |     领域     |                             下载                             |                           项目地址                           |                       机构/个人                        | 架构 |                             文献                             |
| :----------------------: | :-----: | ------- | :--: | :----------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------: | :--: | :----------------------------------------------------------: |
| **Qwen3-Coder-Next**  |   /    | 2026-02 | 中英 | 代码 | [**🤗 Huggingface** ](https://huggingface.co/Qwen/Qwen3-Coder-Next) |                       /                       | [QwenLM](https://github.com/QwenLM) |  /  |                                             |
| **KAT-Dev-72B-Exp**  |   72B    | 2025-10 | 多语 | 软件工程 | [**🤗 Huggingface** ](https://huggingface.co/Kwaipilot/KAT-Dev-72B-Exp) |                       /                       | [Kwaipilot](https://huggingface.co/Kwaipilot) |  CD  |                                             |
| KwaiCoder-23B-A4B-v1 |  A4/23B  | 2025-10 | 多语 | 软件工程 | [**🤗 Huggingface** ](https://huggingface.co/Kwaipilot/KwaiCoder-23B-A4B-v1) |                       /                       | [Kwaipilot](https://huggingface.co/Kwaipilot) |  CD  |                                             |
| Qwen3-Coder | A3/30B  | 2025-08 | 中英 | 代码 | [**🤗 Huggingface** ](https://huggingface.co/Qwen/Qwen3-Coder-30B-A3B-Instruct) | [Qwen3-Coder](https://github.com/QwenLM/Qwen3-Coder) |     [QwenLM](https://github.com/QwenLM)     | MoE  |          [Arxiv](https://arxiv.org/abs/2505.09388)           |
| Skywork-SWE | 32B  | 2025-06 | 中英 | 代码 | [**🤗 Huggingface** ](https://huggingface.co/Skywork/Skywork-SWE-32B) |    /     | [SkyworkAI](https://github.com/SkyworkAI) |  CD  | [Technical Report](https://www.arxiv.org/pdf/2506.19290) |
| Kimi-Dev | 72B  | 2025-06 | 中英 | 代码 | [**🤗 Huggingface** ](https://huggingface.co/moonshotai/Kimi-Dev-72B) | [Kimi-Dev](https://github.com/MoonshotAI/Kimi-Dev) | [MoonshotAI](https://github.com/MoonshotAI) |  CD  |      |
|   Qwen-coder-2.5   | 0.5/1.5/14/32B | 2024-11 | 中英 | 代码 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-coder-66eaa22e6f99801bf65b0c2f) |   [Qwen2.5-Coder](https://github.com/QwenLM/Qwen2.5-Coder)   |        [QwenLM](https://github.com/QwenLM)        |  CD  | [Paper](https://arxiv.org/abs/2409.12186) |
| OpenCoder-Instruct |     1.5/8B     | 2024-11 | 中英 | 代码 | [🤗HF](https://huggingface.co/collections/infly/opencoder-672cec44bbb86c39910fb55e) | [OpenCoder-llm](https://github.com/OpenCoder-llm/OpenCoder-llm) | [OpenCoder-llm](https://github.com/OpenCoder-llm) |  CD  | [Paper](https://arxiv.org/abs/2411.04905) |
| 珠算 | 2.7B | 2024-09 | 中英 | 代码 | [🤗HF](https://huggingface.co/HIT-SCIR/Abacus) | [Abacus](https://github.com/HIT-SCIR/Abacus) | [HIT-SCIR](https://github.com/HIT-SCIR) |  CD  |      |
| Qwen-2.5-code |        1.5/7B         | 2024-09 | 中英 | 代码 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-coder-66eaa22e6f99801bf65b0c2f) | [Qwen2.5](https://github.com/QwenLM/Qwen2.5) | [QwenLM](https://github.com/QwenLM) |  CD  | [Blog](https://qwenlm.github.io/blog/qwen2.5/) |      |
| Qwen-2.5-math |       1.5/7/72B       | 2024-09 | 中英 | 数学 | [🤗HF](https://huggingface.co/collections/Qwen/qwen25-math-66eaa240a1b7d5ee65f1da3e) | [Qwen2.5](https://github.com/QwenLM/Qwen2.5) | [QwenLM](https://github.com/QwenLM) |  CD  | [Blog](https://qwenlm.github.io/blog/qwen2.5/) |      |
|   Yi-Coder    |  1.5/9B   | 2024-09 | 中英 | 代码 | [🤗 Hugging Face](https://huggingface.co/01-ai/Yi-Coder-9B-Chat) • [🤖 ModelScope](https://www.modelscope.cn/models/01ai/Yi-Coder-9B-Chat) • [🟣 wisemodel](https://wisemodel.cn/models/01.AI/Yi-Coder-9B-Chat) |       [Yi-Coder](https://github.com/01-ai/Yi-Coder)       |       [01-ai](https://github.com/01-ai)       |  CD  | [Paper](https://arxiv.org/abs/2403.04652) [Blog](https://01-ai.github.io/blog.html?post=en/2024-09-05-A-Small-but-Mighty-LLM-for-Code.md) |
| CodeGeeX4 |  9B  | 2024-07 | 多语 | 代码 | [🤗HF](https://huggingface.co/THUDM/codegeex4-all-9b) | **[CodeGeeX4](https://github.com/THUDM/CodeGeeX4)** | [THUDM](https://github.com/THUDM) |      |        |
| DeepSeek-Coder-V2 | A16B/236B | 2024-06 | 中英 | 代码 | [🤗HF](https://huggingface.co/deepseek-ai) | [DeepSeek-V2](https://github.com/deepseek-ai/DeepSeek-V2) | [deepseek-ai](https://github.com/deepseek-ai) | MoE  | [Paper](https://github.com/deepseek-ai/DeepSeek-V2/blob/main/deepseek-v2-tech-report.pdf) |
|  AutoCoder  |   6.7/33B    | 2024-06 |  /   | 代码 |    [🤗HF](https://huggingface.co/Bin12345/AutoCoder)    |  [AutoCoder](https://github.com/bin123apple/AutoCoder)  | [Bin Lei](https://huggingface.co/Bin12345) |  CD  |          [Paper](https://arxiv.org/abs/2405.14906)           |
| Codestral | 22B  | 2024-05 |  /   | 代码 | [🤗HF](https://hf-mirror.com/mistralai) |    /     | [mistralai](https://github.com/mistralai) |  /   | [Blog](https://mistral.ai/news/codestral/) |
| CodeQwen1.5-Chat | 7B | 2024-04 | 中英 | 代码 | [🤗HF](https://hf-mirror.com/Qwen/CodeQwen1.5-7B-Chat) | **[Qwen1.5](https://github.com/QwenLM/Qwen1.5)** |[Qwen](https://github.com/QwenLM)|CD|[Blog](https://qwenlm.github.io/blog/codeqwen1.5/)|
| codegemma | 2/7B | 2024-04 | 多语 | 代码 | [🤗HF](https://huggingface.co/google/codegemma-7b) | / |[Google](https://huggingface.co/google)|||
| WaveCoder | 6.7B | 2024-04 | 多语 | 代码 | [🤗HF](https://huggingface.co/microsoft/wavecoder-ds-6.7b) | [WaveCoder](https://github.com/microsoft/WaveCoder) |[microsoft](https://huggingface.co/microsoft)||[Paper](https://arxiv.org/abs/2312.14187)|
| ChemDFM | 13B | 2024-03 | 中英 | 化学 | [🤗HF](https://huggingface.co/OpenDFM) | / | [OpenDFM](https://huggingface.co/OpenDFM) | CD | [Paper](https://arxiv.org/abs/2401.14818) |
| starcoder2 | 3/7/15B | 2024-02 | 中英 | 代码 | [🤗HF](https://huggingface.co/bigcode) | [starcoder2](https://github.com/bigcode-project/starcoder2) | [bigcode-project](https://github.com/bigcode-project) | CD | [Paper](https://drive.google.com/file/d/17iGn3c-sYNiLyRSY-A85QOzgzGnGiVI3/view) |
| TuringMM-Chat | 34B | 2024-02 | 中英 | 教育 | [🤗HuggingFace](https://huggingface.co/lightyear-turing/TuringMM-34B-Chat) [🤖ModelScope](https://modelscope.cn/models/lightyearturing/TuringMM-34B-Chat/summary) | / | [光年无限](https://modelscope.cn/models/lightyearturing/TuringMM-34B-Chat/summary) | CD |  |
| deepseek-moe | 16B | 2024-01 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/deepseek-ai) | [DeepSeekMoE](https://github.com/deepseek-ai/DeepSeek-MoE) | [DeepSeek](https://github.com/deepseek-ai) | CD-MOE |  |
| Code Millenials | 1/3/<br/>13/34B | 2023-01 | 多语 | 代码 | [[🤗HF\]](https://huggingface.co/budecosystem) | [code-millenials](https://github.com/BudEcosystem/code-millenials) | [BudEcosystem](https://github.com/BudEcosystem) | CD |  |
| WizardCoder | 15/33B | 2024-01 | 多语 | 代码 | [[🤗HF\]](https://hf-mirror.com/WizardLM) | [WizardLM](https://github.com/nlpxucan/WizardLM) | [operatorx](https://github.com/nlpxucan) |  CD  | [Paper](https://arxiv.org/abs/2306.08568) |
| DeepSeek-Coder | 1/7/33B | 2023-11 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/deepseek-ai) | [DeepSeek-Coder](https://github.com/deepseek-ai/DeepSeek-Coder) | [deepseek-ai](https://github.com/deepseek-ai) |  | [Blog](https://mp.weixin.qq.com/s/BPW-kMeQNmVPpgvTlbXU1A) |
| Phind | 34B | 2023-10 | 多语 | 代码 | [[🤗HF\]](https://huggingface.co/Phind) | / | [Phind](Phind) | CD | [Blog](https://www.phind.com/blog/phind-model-beats-gpt4-fast) [zh](https://mp.weixin.qq.com/s/fSVPRjNpWPVrLVA59PrIBA) |
| Tongyi-Finance-Chat | 14B | 2023-11 | 中文 | 金融 | [ModelScope](https://modelscope.cn/models/TongyiFinance/Tongyi-Finance-14B-Chat/summary) | [通义金融-14B-Chat](https://modelscope.cn/models/TongyiFinance/Tongyi-Finance-14B-Chat/summary) | [通义金融大模型](https://modelscope.cn/organization/TongyiFinance) | CD |  |
| Skywork-math | 13B | 2023-10 | 中文 | 数学 | [[🤗HF\]](https://huggingface.co/Skywork) | [Skywork](https://github.com/SkyworkAI/Skywork) | [SkyworkAI](https://github.com/SkyworkAI) | CD | [Paper](https://arxiv.org/abs/2310.16713) |
| XuanYuan-Chat | 70B | 2023-10 | 中英 | 金融 | [[🤗HF\]](https://huggingface.co/Duxiaoman-DI/XuanYuan-70B-Chat) | [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan) | [Duxiaoman度小满](https://github.com/Duxiaoman-DI) | CD |  |
| zhilu | 13B | 2023-10 | 中英 | 金融 | [[🤗HF\]](https://huggingface.co/SYSU-MUCFC-FinTech-Research-Center) | / | [SYSU-MUCFC-FinTech-Research-Center](https://huggingface.co/SYSU-MUCFC-FinTech-Research-Center) | CD |  |
| TestGPT | 7B | 2023-10 | 中文 | 测试 | [[🤗HF\]](https://huggingface.co/codefuse-ai/TestGPT-7B) | [Test-Agent](https://github.com/codefuse-ai/Test-Agent) | [codefuse-ai](https://github.com/codefuse-ai) | CD |  |
| cross | 7/13B | 2023-10 | 多语 | 数学 | [[🤗HF\]](https://huggingface.co/Mathoctopus) | / | [Mathoctopus](https://huggingface.co/Mathoctopus) | CD |  |
| CodeFuse | 13/14/<br/>15/34B | 2023-10 | 中文 | 代码 | [[🤗HF\]](https://huggingface.co/codefuse-ai) | [MFTCoder](https://github.com/codefuse-ai/MFTCoder) | [codefuse-ai](https://github.com/codefuse-ai) | CD |  |
| Taiyi | 7B | 2023-10 | 中英 | 医学 | [[🤗HF\]](https://huggingface.co/DUTIR-BioNLP/Taiyi-LLM) | [Taiyi-LLM](https://github.com/DUTIR-BioNLP/Taiyi-LLM) | [DUTIR-BioNLP](https://github.com/DUTIR-BioNLP) | CD |  |
| CodeShell-chat | 7B | 2023-10 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/WisdomShell/CodeShell-7B-Chat) | [codeshell](https://github.com/WisdomShell/codeshell) | [WisdomShell](https://github.com/WisdomShell) | CD |  |
| DISC-LawLLM | 13B | 2023-09 | 中文 | 法律 | [[🤗HF\]](https://huggingface.co/ShengbinYue/DISC-LawLLM) | / | [ShengbinYue](https://huggingface.co/ShengbinYue) | CD | [Report](https://arxiv.org/abs/2309.11325) |
| WiNGPT-chat | 7B | 2023-09 | 中文 | 医学 | [[🤗HF\]](https://huggingface.co/winninghealth/WiNGPT2-7B-Chat) | [WiNGPT2](https://github.com/winninghealth/WiNGPT2) | [Winning Health AI Research](https://github.com/winninghealth) | CD |  |
| ziya-coding | 15/34B | 2023-09 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Ziya-Coding-34B-v1.0) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) |          [IDEA研究院](https://github.com/IDEA-CCNL)          | CD |  |
| AgriGPT | 6/13b | 2023-09 | 中文 | 农业 | [[🤗HF\]](https://huggingface.co/AgriGPTs/AgriGPT-13B) | [AgriGPTs](https://github.com/AgriGPTs/AgriGPTs) | [AgriGPTs](https://github.com/AgriGPTs) |  |  |
| XuanYuan-chat | 70B  | 2023-09 | 中文 | 金融 | [TODO]() | [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan) | [度小满](https://github.com/Duxiaoman-DI) |  CD  | [Report](https://github.com/Duxiaoman-DI/XuanYuan/blob/main/xuanyuan_70b_report.md) |
| 夫子•明察 | 6B | 2023-09 | 中文 | 司法 | [[🤗HF\]](https://huggingface.co/SDUIRLab/fuzi.mingcha-v1.0) | [fuzi.mingcha](https://github.com/irlab-sdu/fuzi.mingcha) | [山东大学](https://github.com/irlab-sdu) | ND |  |
| 仲景 | 13B | 2023-09 | 中文 | 医学 | [[🤗HF\]](https://huggingface.co/Suprit) | [Zhongjing](https://github.com/SupritYoung/Zhongjing) | [Songhua Yang](https://github.com/SupritYoung) | CD | [Paper](https://arxiv.org/abs/2308.03549) |
| CodeFuse | 13/34B | 2023-09 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/codefuse-ai/CodeFuse-13B) | [MFTCoder](https://github.com/codefuse-ai/MFTCoder) | [codefuse-ai](https://github.com/codefuse-ai) | CD |  |
| EcomGPT | 7B | 2023-09 | 中英 | 电商 | [TODO]() | [EcomGPT](https://github.com/Alibaba-NLP/EcomGPT) | [Alibaba](https://github.com/Alibaba-NLP) |  |  |
| DISC-MedLLM | 13B | 2023-08 | 中文 | 医疗 | [[🤗HF\]](https://huggingface.co/Flmc/DISC-MedLLM) | [DISC-MedLLM](https://github.com/FudanDISC/DISC-MedLLM) | [FudanDISC](https://github.com/FudanDISC) | CD | [Paper](https://arxiv.org/abs/2308.14346) |
| K2 | 7B | 2023-08 | 中英 | 科学 | [[🤗HF\]](https://huggingface.co/daven3/k2_fp_delta) | [k2](https://github.com/davendw49/k2) | [daven](https://github.com/davendw49) | CD |  |
| CodeLLAma | 7/13/34B | 2023-08 | 多语 | 代码 | [[🤗HF\]](https://huggingface.co/codellama) | [codellama](https://github.com/facebookresearch/codellama) | [Meta Research](https://github.com/facebookresearch) | CD | [Paper](https://arxiv.org/abs/2308.12950) |
| sqlcoder | 15B | 2023-08 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/defog/sqlcoder) | [sqlcoder](https://github.com/defog-ai/sqlcoder) | [Defog.ai](https://github.com/defog-ai) | CD |  |
| 智海-录问 |  7B  | 2023-08 | 中文 | 法律 | [[🤗HF\]](https://pan.baidu.com/s/16lwM2rPnSq9u-UbtWbZgig) | [wisdomInterrogatory](https://github.com/zhihaiLLM/wisdomInterrogatory) | [zhihaiLLM](https://github.com/zhihaiLLM) |  CD  |      |
| WizardMath-V1.0 | 7/13/70B | 2023-08 | 多语 | 数学 | [[🤗HF\]](https://huggingface.co/WizardLM/WizardMath-7B-V1.0) | [WizardLM](https://github.com/nlpxucan/WizardLM) | [operatorx](https://github.com/nlpxucan) | CD |  |
| QiaoBan | 7B | 2023-08 | 中文 | 情感 | [[🤗HF\]](https://huggingface.co/tomxyz/qiaoban_bc) | [QiaoBen](https://github.com/HIT-SCIR-SC/QiaoBan) | [哈尔滨工业大学](https://github.com/HIT-SCIR-SC) |  |  |
| HuangDi | 13B | 2023-08 | 中文 | 中医 | [[🤗HF\]](https://pan.baidu.com/s/1Mzlk5FREpTPa4M7KnMooqQ?pwd=erit) | [HuangDI](https://github.com/Zlasejd/HuangDI) | [Zlasejd](https://github.com/Zlasejd) | CD |  |
| ZhongJing |  | 2023-08 | 中文 | 中医 | [TODO]() | [CMLM-ZhongJing](https://github.com/pariskang/CMLM-ZhongJing) | [复旦大学](pariskang) |  |  |
| TCMLLM | 6B | 2023-08 | 中文 | 中医 | [[🤗HF\]](https://pan.baidu.com/s/1QFx-206Ww9Xt-7_Z0RF85g) | [TCMLLM](https://github.com/2020MEAI/TCMLLM) | [2020MEAI](https://github.com/2020MEAI) | ND |  |
| AutoAudit | 7B | 2023-07 | 中文 | 安全 | [[🤗HF\]](https://github.com/ddzipp/AutoAudit/blob/main) | [AutoAudit](https://github.com/ddzipp/AutoAudit) | [Jiaying Li](https://github.com/ddzipp) | CD |  |
| Lychee | 10B | 2023-07 | 中文 | 法律 | [[🤗HF\]](https://huggingface.co/law-llm/law-glm-10b) | [lychee_law](https://github.com/davidpig/lychee_law) | [davidpig](https://github.com/davidpig) | ND |  |
| IvyGPT | 6B | 2023-07 | 中文 | 医学 | [[🤗HF\]](https://huggingface.co/wangrongsheng/IvyGPT-35) | [IvyGPT](https://github.com/WangRongsheng/IvyGPT) | [WangRongsheng](https://github.com/WangRongsheng) |  |  |
| MING | 7B | 2023-07 | 中文 | 医学 | [[🤗HF\]](https://huggingface.co/BlueZeros/MING-7B) | [MING](https://github.com/MediaBrain-SJTU/MING) | [上海交通大学](https://github.com/MediaBrain-SJTU) | CD |  |
| Mozi | 7B | 2023-07 | 中英 | 科技 | [[🤗HF\]](https://huggingface.co/DataHammer/mozi_llama_7b) | [science-llm](https://github.com/gmftbyGMFTBY/science-llm) | [GMFTBY](https://github.com/gmftbyGMFTBY) | CD |  |
| StarGLM | 6B | 2023-07 | 中文 | 天文 | [[🤗HF\]](https://github.com/Yu-Yang-Li/StarGLM) | [StarGLM](https://github.com/Yu-Yang-Li/StarGLM) | [LI YUYANG](https://github.com/Yu-Yang-Li) | ND |  |
| TransGPT | 7B | 2023-07 | 中英 | 交通 | [[🤗HF\]](https://huggingface.co/DUOMO-Lab/TransGPT-v0) | [TransGPT](https://github.com/DUOMO/TransGPT) | [北京交通大学](https://github.com/DUOMO) | CD |  |
| CodeGeeX2 | 6B | 2023-07 | 中英 | 代码 | [[🤗HF\]](https://huggingface.co/THUDM/codegeex2-6b) | [CodeGeeX2](https://github.com/THUDM/CodeGeeX2) | [清华大学](https://github.com/THUDM) | ND |  |
|           Yayi-llama2           |   7/13B    | 2023-07 | 中英 | 舆情 |    [[🤗HF\]](https://huggingface.co/wenge-research/yayi-7b-llama2)    | [Yayi](https://github.com/wenge-research/YaYi) |     [中科闻歌](https://github.com/wenge-research)      |  CD  | |
| Ziya-Writing |   13B    | 2023-07 | 中英 | 写作 | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Ziya-Writing-LLaMa-13B-v1) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) | [IDEA研究院](https://github.com/IDEA-CCNL)  |  CD  |  |
| MindChat | 13B | 2023-07 | 中文 | 心理 | [[🤗HF\]](https://modelscope.cn/models/X-D-Lab/MindChat-Baichuan-13B/summary) | [MindChat](https://github.com/X-D-Lab/MindChat) | [华东理工大学](https://github.com/X-D-Lab) | CD |  |
|     ShenNong-TCM-LLM     |   7B    | 2023-07 | 中英 |     医学     |                           [[🤗HF\]]()                           | [ShenNong-TCM-LLM](https://github.com/michael-wzhu/ShenNong-TCM-LLM) |    [michael-wzhu](https://github.com/michael-wzhu)     |  CD  |                                                              |
|         ailawyer         |   13B   | 2023-07 | 中英 |     法律     |        [[🤗HF\]](https://huggingface.co/openkg/ailawyer)        | [JurisLMs](https://github.com/seudl/JurisLMs) |        [openkg](https://huggingface.co/openkg)         |  CD  |                                                              |
|     educhat      | 7B/13B  | 2023-06 | 中英 |     教育     | [[🤗HF\]](https://huggingface.co/ecnu-icalk/educhat-sft-002-13b) | [EduChat](https://github.com/icalk-nlp/EduChat) |      [华东师范大学](https://github.com/icalk-nlp)      |  CD  |                                                              |
|        Sunsimiao         |   7B    | 2023-06 | 中英 |     医学     | [[🤗HF\]](https://modelscope.cn/models/AI-ModelScope/Sunsimiao/files) | [Sunsimiao](https://github.com/X-D-Lab/Sunsimiao) |       [华东理工大学](https://github.com/X-D-Lab)       |  CD  |                                                              |
|       Media LLaMA        |   7B    | 2023-06 | 中文 |    媒体    | [baidu](https://pan.baidu.com/s/1tEuj0SvwJK4czQPCE6gI9w?pwd=onfo) | [Media-LLaMA](https://github.com/IMOSR/Media-LLaMA) |       [智媒开源研究院](https://github.com/IMOSR)       |  CD  |                                                              |
|          PULSE           |  7/14B  | 2023-06 | 中文 |     医学     | [[🤗HF\]](https://huggingface.co/OpenMEDLab/PULSE-7bv5) | [PULSE](https://github.com/openmedlab/PULSE) |      [OpenMEDLab](https://github.com/OpenMEDLab)       |  CD  |                                                              |
|         ChatLaw          | 13/33B  | 2023-06 | 中文 |     法律     | [[🤗HF\]](https://huggingface.co/JessyTsu1/ChatLaw-13B) | [ChatLaw](https://github.com/PKU-YuanGroup/ChatLaw) |      [北京大学](https://github.com/PKU-YuanGroup)      |  CD  |                                                              |
|          BaoLuo          |   6B    | 2023-06 | 中文 |     法律     | [[🤗HF\]](https://huggingface.co/xuanxuanzl/BaoLuo-LawAssistant-sftglm-6b) | [BaoLuo-LawAssisant](https://github.com/xuanxuanzl/BaoLuo-LawAssistant) |         [LeiZi](https://github.com/xuanxuanzl)         |  ND  |                                                              |
|         CoLLaMA          |   7B    | 2023-06 | 中英 |     代码     |      [[🤗HF\]](https://huggingface.co/DaliahX/CoLLaMA-7b)       | [CoLLaMA](https://github.com/Denilah/CoLLaMA) |         [Denilah](https://github.com/Denilah)          |  CD  |                                                              |
|         TechGPT          |   7B    | 2023-06 | 中英 |     教育     |       [[🤗HF\]](https://huggingface.co/neukg/TechGPT-7B)        | [TechGPT](https://github.com/neukg/TechGPT) |          [东北大学](https://github.com/neukg)          |  CD  |                                                              |
|           Yayi           |   7B    | 2023-06 | 中英 | 舆情 |    [[🤗HF\]](https://huggingface.co/wenge-research/yayi-7b)     | [Yayi](https://github.com/wenge-research/YaYi) |     [中科闻歌](https://github.com/wenge-research)      |  CD  |                                                              |
|          MeChat          |   6B    | 2023-06 | 中文 |     医学     |      [[🤗HF\]](https://huggingface.co/qiuhuachuan/MeChat)       | [smile](https://github.com/qiuhuachuan/smile) |     [qiuhuachuan](https://github.com/qiuhuachuan)      |  ND  |                                                              |
|       ziya-medical       |   13b   | 2023-06 | 中英 |     医学     | [[🤗HF\]](https://huggingface.co/shibing624/ziya-llama-13b-medical-lora) | [MedicalGPT](https://github.com/shibing624/MedicalGPT) |        [Ming Xu](https://github.com/shibing624)        |  CD  |                                                              |
|          Taoli           |   7B    | 2023-06 | 中英 |     教育     |                          [待开源]()                          | [taoli](https://github.com/blcuicall/taoli) |      [北京语言大学](https://github.com/blcuicall)      |  CD  |                                                              |
|       Lawyer-llama       |   13B   | 2023-06 | 中英 |     法律     | [[🤗HF\]](https://huggingface.co/pkupie/lawyer-llama-13b-beta1.0) | [lawyer-llama](https://github.com/AndrewZhe/lawyer-llama) |      [Quzhe Huang](https://github.com/AndrewZhe)       |  CD  |                                                              |
|       QiZhen-CaMA        |   13B   | 2023-06 | 中英 |     医学     | [[🤗HF\]](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) | [QiZhenGPT](https://github.com/CMKRG/QiZhenGPT) |          [浙江大学](https://github.com/CMKRG)          |  CD  |                                                              |
|         扁鹊-2.0         |   6B    | 2023-06 | 中文 |     医学     |       [[🤗HF\]](https://huggingface.co/scutcyr/BianQue-2)       | [BianQue](https://github.com/scutcyr/BianQue) |       [华南理工大学](https://github.com/scutcyr)       |  ND  |                                                              |
|         SoulChat         |   6B    | 2023-06 | 中文 |     心理     |       [[🤗HF\]](https://huggingface.co/scutcyr/SoulChat)        | [SoulChat](https://github.com/scutcyr/SoulChat) |       [华南理工大学](https://github.com/scutcyr)       |  ND  |                                                              |
|          HanFei          |   7B    | 2023-05 | 中文 |     法律     | [baidu-d6t5](https://pan.baidu.com/s/1PkRXUo9sNRQmoXHcW7Aeeg?pwd=d6t5) | [HanFei](https://github.com/siat-nlp/HanFei) |  [中国科学院深圳先进院](https://github.com/siat-nlp)   |  CD  |                                                              |
|      QiZhen      |   6B    | 2023-05 | 中英 |     医学     | [[baidu\]](https://pan.baidu.com/s/1KQIF-dUsL7Nrj8UeNuFUiw?pwd=ivgg) | [QiZhenGPT](https://github.com/CMKRG/QiZhenGPT) |          [浙江大学](https://github.com/CMKRG)          |  CD  |                                                              |
|     ChatMed-Consult      |   7B    | 2023-05 | 中英 |     医学     |  [[🤗HF\]](https://huggingface.co/michaelwzhu/ChatMed-Consult)  | [ChatMed](https://github.com/michael-wzhu/ChatMed) |    [michael-wzhu](https://github.com/michael-wzhu)     |  CD  |                                                              |
|      LaWGPT-beta1.1      |   7B    | 2023-05 | 中英 |     法律     |  [[🤗HF\]](https://huggingface.co/entity303/lawgpt-lora-7b-v2)  | [LawGPT](https://github.com/pengxiao-song/LaWGPT) |   [Pengxiao Song](https://github.com/pengxiao-song)    |  CD  |                                                              |
|        Cornucopia        |   7B    | 2023-05 | 中英 |     金融     | [[🤗HF\]](https://huggingface.co/yuyangmu125/lora-llama-fin-Linly-zh) | [Cornucopia-LLaMA-Fin-Chinese](https://github.com/jerry1993-tech/Cornucopia-LLaMA-Fin-Chinese) |     [yuyangmu](https://github.com/jerry1993-tech)      |  CD  |                                                              |
|        HuatuoGPT         |   7B    | 2023-05 | 中文 |     医学     | [[🤗HF\]](https://huggingface.co/FreedomIntelligence/HuatuoGPT-v1) | [HuatuoGPT](https://github.com/FreedomIntelligence/HuatuoGPT) | [香港中文大学](https://github.com/FreedomIntelligence) |  CD  |        [Paper](https://arxiv.org/pdf/2305.15075.pdf)         |
|         LexiLaw          |   6B    | 2023-05 | 中文 |     法律     |         [[🤗HF\]](https://github.com/CSHaitao/LexiLaw)          |        [LexiLaw](https://github.com/CSHaitao/LexiLaw)        |        [Haitao Li](https://github.com/CSHaitao)        |  ND  |          [Paper](https://arxiv.org/abs/2305.12002)           |
|         XuanYuan         |  176B   | 2023-05 | 中文 |     金融     |    [申请](https://huggingface.co/xyz-nlp/XuanYuan2.0)    | [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan) |       [度小满](https://github.com/Duxiaoman-DI)        |  CD  |          [Paper](https://arxiv.org/abs/2305.12002)           |
|          LawGPT          |   6B    | 2023-05 | 中文 |     法律     |     [[🤗HF\]](https://github.com/LiuHC0428/LAW-GPT) | [LAW-GPT](https://github.com/LiuHC0428/LAW-GPT) |      [hongchengliu](https://github.com/LiuHC0428)      |  N   |                                                              |
|         扁鹊-1.0         |  0.7B   | 2023-04 | 中文 |     医学     |      [[🤗HF\]](https://huggingface.co/scutcyr/BianQue-1.0)      |        [BianQue](https://github.com/scutcyr/BianQue)         |         [scutcyr](https://github.com/scutcyr)          |  ED  |                                                              |
|       ChatGLM-Med        |   6B    | 2023-04 | 中文 |     医学     | [[🤗HF\]](https://drive.google.com/drive/folders/1ZQSN56DloRGQ-Qj7IwzY4jV3ZHKMe9Bc) | [Med-ChatGLM](https://github.com/SCIR-HI/Med-ChatGLM) |      [哈尔滨工业大学](https://github.com/SCIR-HI)      |  ED  |                                                              |
|         BenTsao          |   7B    | 2023-04 | 中文 |     医学     | [[🤗HF\]](https://huggingface.co/thinksoso/lora-llama-med) | [Huatuo-Llama-Med-Chinese](https://github.com/SCIR-HI/Huatuo-Llama-Med-Chinese) |      [哈尔滨工业大学](https://github.com/SCIR-HI)      |  CD  |                                                              |
|        DoctorGLM         |   6B    | 2023-04 | 中文 |     医学     |                          [TODO]()                          | [DoctorGLM](https://github.com/xionghonglin/DoctorGLM) |    [xionghonglin](https://github.com/xionghonglin)     |  ND  |                                                              |
|         Firefly          |   1/2/7B   | 2023-04 | 中文 |     文化     | [[🤗HF\]](https://huggingface.co/YeungNLP/firefly-bloom-7b1-qlora-sft) | [Firefly](https://github.com/yangjianxin1/Firefly) |    [Yang JianXin](https://github.com/yangjianxin1)     |  CD  |                                                              |
|         ChatRWKV         |   7B    | 2023-01 | 中英 |     小说     | [[🤗HF\]](https://huggingface.co/BlinkDL/rwkv-4-pile-7b/tree/main) | [ChatRWKV](https://github.com/BlinkDL/ChatRWKV) |         [BlinkDL](https://github.com/BlinkDL)          | RNN  |        [Blog](https://zhuanlan.zhihu.com/p/609154637)        |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## MultiModal-ChatLLM

> 收集包含中文的多模态大模型，具备对话等功能。

|           模型           | 大小  |  时间   |                           语言模型                           |                          非语言模型                          | 语言 |   领域    |                             下载                             |                           项目地址                           |                        机构/个人                         |                             文献                             |
| :----------------------: | :---: | :-----: | :----------------------------------------------------------: | :----------------------------------------------------------: | :--: | :-------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :------------------------------------------------------: | :----------------------------------------------------------: |
| Gemma-4-IT | E2B/E4B/26B A4B/31B | 2026-04 | Gemma-4 LM (CD+Hybrid) | 文本+图像(全量)+音频(E2B/E4B) | 多语(35+) | 通用 | [🤗 HF](https://huggingface.co/collections/google/gemma-4) | - | [Google DeepMind](https://huggingface.co/google) | [Model Card](https://ai.google.dev/gemma/docs/core/model_card_4) |
| Qianfan-OCR | 4B | 2026-03 | [Qwen3-4B](https://huggingface.co/Qwen/Qwen3-4B) | Qianfan-ViT, 24层, AnyResolution(最大4K) | 中英 | 文档 | [🤗 HF](https://huggingface.co/baidu/Qianfan-OCR) | [GitHub](https://github.com/baidubce/Qianfan-VL) | [百度](https://github.com/baidubce) | [arXiv](https://arxiv.org/abs/2603.13398) |
| GLM-OCR | / | 2026-02 | / | / | 中英 | 文图 | [🤗 HF](https://huggingface.co/zai-org/GLM-OCR) | / | [zai-org](https://github.com/zai-org) | / |
| Ace-Step1.5 | / | 2026-02 | / | / | 中英 | 文音 | [🤗 HF](https://huggingface.co/ACE-Step/Ace-Step1.5) | / | [ACE-Step](https://github.com/ACE-Step) | / |
| HunyuanImage-3.0-Instruct | / | 2026-02 | / | / | 中英 | 文图 | [🤗 HF](https://huggingface.co/tencent/HunyuanImage-3.0-Instruct) | / | [Tencent](https://github.com/Tencent) | / |
| AutoGLM-Phone |  9B  | 2025-12 |    **AutoGLM**    |  **AutoGLM**  | 中英 | Agent | [🤗 HF](https://huggingface.co/zai-org/AutoGLM-Phone-9B) | [Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM) |   [zai-org](https://github.com/zai-org)   | [**Paper Link**](https://github.com/deepseek-ai/DeepSeek-OCR/blob/main/DeepSeek_OCR_paper.pdf) |
|  Dolphin-v2   |  3B  | 2025-12 | **Qwen2.5-VL-3B** | Qwen2.5-VL-3B | 中英 | 文图  |   [🤗 HF](https://huggingface.co/ByteDance/Dolphin-v2)   |     [Dolphin](https://github.com/bytedance/Dolphin)     | [bytedance](https://github.com/bytedance) |          [arXiv](https://arxiv.org/abs/2505.14059)           |
| DeepSeek-OCR |  3B  | 2025-10 |    /     |     /      | 中英 | 文图 | [🤗 HF](https://huggingface.co/deepseek-ai/DeepSeek-OCR) | [DeepSeek-OCR](https://github.com/deepseek-ai/DeepSeek-OCR) | [deepseek-ai](https://github.com/deepseek-ai) | [**Paper Link**](https://github.com/deepseek-ai/DeepSeek-OCR/blob/main/DeepSeek_OCR_paper.pdf) |
|      VoxCPM      | 0.5B | 2025-09 | [MiniCPM-4](https://huggingface.co/openbmb/MiniCPM4-0.5B) |     /      | 中英 | 文音 |      [🤗 HF](https://huggingface.co/openbmb/VoxCPM-0.5B)      |         [VoxCPM](https://github.com/OpenBMB/VoxCPM)          |            [OpenBMB](https://github.com/OpenBMB)             |                              /                               |
|    VibeVoice     | 1.5B | 2025-09 | [Qwen2.5-1.5B](https://huggingface.co/Qwen/Qwen2.5-1.5B)  |     /      | 中英 | 文音 |   [🤗 HF](https://huggingface.co/microsoft/VibeVoice-1.5B)    |     [VibeVoice](https://github.com/microsoft/VibeVoice)      |          [microsoft](https://github.com/microsoft)           | [VibeVoice Technical Report](https://arxiv.org/abs/2508.19205) |
|   HunyuanImage   | 17B  | 2025-09 |                             /                             |     /      | 中英 | 文图 |   [🤗 HF](https://huggingface.co/tencent/HunyuanImage-2.1)    | [HunyuanImage-2.1](https://github.com/Tencent-Hunyuan/HunyuanImage-2.1) |    [Tencent-Hunyuan](https://github.com/Tencent-Hunyuan)     |                              /                               |
| PromptEnhancerV2 | 32B  | 2025-09 |                             /                             |     /      | 中英 | 文图 | [🤗 HF](https://huggingface.co/PromptEnhancer/PromptEnhancer-32B) | [PromptEnhancer](https://github.com/Hunyuan-PromptEnhancer/PromptEnhancer) | [Hunyuan-PromptEnhancer](https://github.com/Hunyuan-PromptEnhancer) | [report](https://hunyuan-promptenhancer.github.io/) [paper](https://www.arxiv.org/abs/2509.04545) |
| **Qwen-Image** | 20B  | 2025-08 |    /     |     /      | 中英 | 文图 | [🤗 HF](https://huggingface.co/Qwen/Qwen-Image) | [Qwen-Image](https://github.com/QwenLM/Qwen-Image) | [QwenLM](https://github.com/QwenLM) | [Tech Report](https://qianwen-res.oss-cn-beijing.aliyuncs.com/Qwen-Image/Qwen_Image.pdf) |
| ERNIE-4.5-VL | A47/424B | 2025-07 |    /     |     /      | 中英 | 文图 | [🤗 HF](https://huggingface.co/baidu) |    /     | [BaiDu](https://huggingface.co/baidu) | [**📄 Tech Report** ](https://arxiv.org/abs/2504.07491) |
|   Dolphin   | A3/16B | 2025-05 |  MBart   | Swin Transformer | 中英 |  文图  | [🤗 HF](https://huggingface.co/moonshotai/Kimi-VL-A3B-Instruct) | [Dolphin](https://github.com/bytedance/Dolphin) | [bytedance](https://github.com/bytedance) | [arXiv](https://arxiv.org/abs/2505.14059). |
| Wan2.1-VACE |  14B   | 2025-05 |    /     |        /         | 中英 | 文图视 |    [🤗 HF](https://huggingface.co/Wan-AI/Wan2.1-VACE-14B)     |  [Wan2.1](https://github.com/Wan-Video/Wan2.1)  | [Wan-Video](https://github.com/Wan-Video) | [arXiv](https://arxiv.org/abs/2503.20314)  |
| Kimi-VL | A3/16B | 2025-04 |                          /                           |     /      | 多语 | 文图 | [🤗 HF](https://huggingface.co/moonshotai/Kimi-VL-A3B-Instruct) | [Kimi-VL](https://github.com/MoonshotAI/Kimi-VL) |  [MoonshotAI](https://github.com/MoonshotAI)  |     [**Tech Report** ](https://arxiv.org/abs/2504.07491)     |
|        Aya Vision         | 8/32B | 2025-03 | [C4AI Command R7B](https://huggingface.co/CohereForAI/c4ai-command-r7b-12-2024) | [SigLIP2-patch14-384](https://huggingface.co/google/siglip2-so400m-patch14-384) | 多语 | 文图 | [🤗 HF](https://huggingface.co/collections/CohereForAI/c4ai-aya-vision-67c4ccd395ca064308ee1484) |                       /                       | [Cohere For AI](https://huggingface.co/CohereForAI) |                                                              |
| Phi-4-multimodal-instruct | 5.6B  | 2025-03 |                              /                               |                              /                               | 多语 | 文图 | [🤗 HF](https://huggingface.co/microsoft/Phi-4-multimodal-instruct) |                       /                       |    [Microsoft](https://huggingface.co/microsoft)    | [Phi-4-multimodal Technical Report](https://aka.ms/phi-4-multimodal/techreport) |
|         CogView4          |  6B   | 2025-03 |     [GLM-4-9B](https://huggingface.co/THUDM/glm-4-9b-hf)     |                              /                               | 中英 | 文图 |       [🤗 HF](https://huggingface.co/THUDM/CogView4-6B)       | [CogView4](https://github.com/THUDM/CogView4) |          [THUDM](https://github.com/THUDM)          |          [arxiv](https://arxiv.org/pdf/2403.05121)           |
|     Wan2.1      | 1.3/14B | 2025-02 |    /     |     /      | 中英 | 文视图 |           [🤗 HF](https://huggingface.co/Wan-AI)           |     [Wan2.1](https://github.com/Wan-Video/Wan2.1)      |  [Wan-Video](https://github.com/Wan-Video)  |                     /                     |
| Step-Audio-Chat |  130B   | 2025-02 |  Step-1  |     /      | 多语 |  文音  | [🤗 HF](https://huggingface.co/stepfun-ai/Step-Audio-Chat) | [Step-Audio](https://github.com/stepfun-ai/Step-Audio) | [stepfun-ai](https://github.com/stepfun-ai) | [Paper](https://arxiv.org/abs/2502.11946) |
|   Ovis2   | 1/4/16/34B | 2025-02 |   Qwen2.5    |                         aimv2-large                         | 中英 | 文图视 | [🤗 HF](https://huggingface.co/collections/AIDC-AI/ovis2-67ab36c7e497429034874464) |    [Ovis](https://github.com/AIDC-AI/Ovis)    |     [AIDC-AI](https://github.com/AIDC-AI)     |          [Paper](https://arxiv.org/abs/2405.20797)           |
| Janus-Pro |   1.5/7B   | 2025-02 | deepseek-llm | [SigLIP-L](https://huggingface.co/timm/ViT-L-16-SigLIP-384) | 中英 |  文图  |   [🤗 HF](https://huggingface.co/deepseek-ai/Janus-Pro-7B)    | [Janus](https://github.com/deepseek-ai/Janus) | [deepseek-ai](https://github.com/deepseek-ai) | [paper](https://github.com/deepseek-ai/Janus/blob/main/janus_pro_tech_report.pdf) |
|  OuteTTS  |      | 2025-01 | Qwen2.5-0.5B |                    OLMo-1B                     | 多语 |  文音  | [🤗 HF](https://huggingface.co/collections/OuteAI/outetts-03-6786b1ebc7aeb757bc17a2fa) |    [OuteTTS](https://github.com/edwko/OuteTTS)    |              [edwko](https://github.com/edwko)               | [Blog](https://www.outeai.com/blog) |
| MiniCPM-o |  8B  | 2025-01 |  Qwen2.5-7B  | SigLip-400M、Whisper-medium-300M, ChatTTS-200M | 中英 | 文音图 | [🤗 HF]( https://huggingface.co/collections/openbmb/multimodal-models-65d48fa84e358ce02a92d004) | [MiniCPM-o](https://github.com/OpenBMB/MiniCPM-o) | [ ](https://github.com/edwko/OuteTTS)  [OpenBMB](https://github.com/OpenBMB) |                                     |
| Sa2VA | 1/4/8B | 2024-12 | Qwen2.5  | InternVL2.5 | 中英 | 文视图 | [🤗 HF]( https://huggingface.co/collections/ByteDance/sa2va-model-zoo-677e3084d71b5f108d00e093) | [Sa2VA](https://github.com/magic-research/Sa2VA) | [magic-research](https://github.com/magic-research)/ [Sa2VA](https://github.com/magic-research/Sa2VA) | [Paper](https://arxiv.org/abs/2501.04001) |
| QVQ-72B-Preview | 72B  | 2024-12 |    /     |    /     | 中英 | 文视图 | [🤗 HF](https://huggingface.co/collections/Qwen/qvq-676448c820912236342b9888) | [Qwen2-VL](https://github.com/QwenLM/Qwen2-VL) | [QwenLM](https://github.com/QwenLM) | [Blog](https://qwenlm.github.io/zh/blog/qvq-72b-preview/) |
| Megrez-3B-Omni |     3B     | 2024-12 | Megrez-3B-Instruct | SigLip-400M/Qwen2-Audio/whisper-large-v3 | 中英 | 文音图 | [🤗 HF](https://huggingface.co/Infinigence/Megrez-3B-Omni) | [Infini-Megrez-Omni](https://github.com/infinigence/Infini-Megrez-Omni) | [infinigence](https://github.com/infinigence) |                                           |
|  DeepSeek-VL2  | 1/2.8/4.5B | 2024-12 |         /          |                    /                     |      |  文图  |  [🤗 HF](https://huggingface.co/deepseek-ai/deepseek-vl2)  | [DeepSeek-VL2](https://github.com/deepseek-ai/DeepSeek-VL2)  | [deepseek-ai](https://github.com/deepseek-ai) | [Paper](https://arxiv.org/abs/2412.10302) |
| InternVL 2.5 | 2/4/8/26/38/78B | 2024-12 | Qwen-2.5 | InternVit | 多语 | 文图 | [🤗 HF](https://huggingface.co/collections/OpenGVLab/internvl-25-673e1019b66e2218f68d7c1c) | [InternVL](https://github.com/OpenGVLab/InternVL) | [OpenGVLab](https://github.com/OpenGVLab) | [blog](https://internvl.github.io/blog/) |
| Pixtral-Large-Instruct | 124B | 2024-11 | [Mistral-Large-Instruct-2407](https://huggingface.co/mistralai/Mistral-Large-Instruct-2407) | / | 多语 | 文图 | [🤗 Huggingface](https://huggingface.co/mistralai/Pixtral-Large-Instruct-2411) | / | [mistralai](https://huggingface.co/mistralai) | [Pixtral Large blog post](https://mistral.ai/news/pixtral-large/) |
| fish-agent | 3B | 2024-11 | Qwen-2.5 | / | 多语 | 文音 | [🤗 Huggingface](https://huggingface.co/fishaudio) | [fish-speech](https://github.com/fishaudio/fish-speech) | [fishaudio](https://github.com/fishaudio) |  |
| GLM-4-Voice | 9B | 2024-10 | [GLM-4-9B](https://github.com/THUDM/GLM-4) | [Whisper](https://github.com/openai/whisper) | 中英 | 文音 | [🤗 Huggingface](https://huggingface.co/THUDM/glm-4-voice-9b) | [GLM-4-Voice](https://github.com/THUDM/GLM-4-Voice) | [THUDM](https://github.com/THUDM) |  |
| Pangea | 7B | 2024-10 | [Qwen2-7B-Instruct](https://huggingface.co/Qwen/Qwen2-7B-Instruct) | [LLaVA-NeXT](https://github.com/LLaVA-VL/LLaVA-NeXT) | 多语 | 图文 | [🤗HF](https://huggingface.co/neulab/Pangea-7B) | [Pangea](https://github.com/neulab/Pangea) | [neulab](https://github.com/neulab) | [Paper](https://arxiv.org/abs/2410.16153) |
| GOT-OCR-2.0 | / | 2024-09 | Qwen | / | 中英 | 图文 | [🤗HF](https://huggingface.co/stepfun-ai/GOT-OCR2_0) | [GOT-OCR2.0](https://github.com/Ucas-HaoranWei/GOT-OCR2.0) | [**StepFun-AI**](https://huggingface.co/stepfun-ai) | [Paper](https://arxiv.org/abs/2409.01704) |
| Ovis-1.6 | 9B | 2024-09 | Gemma2-9B-It | Siglip-400M | 中英 | 图文 | [🤗](https://huggingface.co/AIDC-AI/Ovis1.6-Gemma2-9B) | [Ovis](https://github.com/AIDC-AI/Ovis) | [AIDC-AI](https://github.com/AIDC-AI) | [Paper](https://arxiv.org/abs/2405.20797) |
| Qwen2-VL | 2/7/72B | 2024-08 | / | / | 多语 | 图文视 | [🤗](https://huggingface.co/Qwen/Qwen2-VL-7B-Instruct) [🤖](https://modelscope.cn/models/qwen/Qwen2-VL-7B-Instruct) | [Qwen2-VL](https://github.com/QwenLM/Qwen2-VL) | [QwenLM](https://github.com/QwenLM) |  |
| CogVideoX | 2/5B | 2024-08 | / | / | 中英 | 文视 | [🤗 link](https://huggingface.co/THUDM/CogVideoX-2b) | [CogVideo](https://github.com/THUDM/CogVideo) | [THUDM](https://github.com/THUDM) |  |
| MiniCPM-V 2.6 | 8B | 2024-08 |  Qwen2-7B  | SigLip-400M | 中英 | 文图视 | [🤗 link](https://huggingface.co/openbmb/MiniCPM-V-2_6) | [MiniCPM-V](https://github.com/OpenBMB/MiniCPM-V) | [OpenBMB](https://github.com/OpenBMB) |  |
| InternVL2 | 1/2/4/8/26/40/76B | 2024-07 |  Qwen2/internlm2/llama3  | [InternViT](https://huggingface.co/OpenGVLab/InternViT-6B-448px-V1-5) | 中英 | 文图 | [🤗 link](https://huggingface.co/collections/OpenGVLab/internvl-20-667d3961ab5eb12c7ed1463e) [🤖 link](https://modelscope.cn/organization/OpenGVLab) | [InternVL](https://github.com/OpenGVLab/InternVL) | [OpenGVLab](https://github.com/OpenGVLab) | [report](https://arxiv.org/abs/2404.16821) |
| Qwen2-Audio | 8.2B | 2024-07 |  Qwen2   | Whisper-large-V3 | 中英 | 文音 | [🤗HF](https://huggingface.co/Qwen/Qwen-Audio) | [Qwen2-Audio](https://github.com/QwenLM/Qwen2-Audio) | [QwenLM](https://github.com/QwenLM) | [report](https://arxiv.org/abs/2407.10759) |
| **Kolors** | / | 2024-07 | ChatGLM3-Base | / | 中英 | 文图 | [🤗HF](https://huggingface.co/Kwai-Kolors/Kolors) | [Kolors](https://github.com/Kwai-Kolors/Kolors) | [Kwai-Kolors](https://github.com/Kwai-Kolors) | [Paper](https://github.com/Kwai-Kolors/Kolors/blob/master/imgs/Kolors_paper.pdf) |
| ChatTTS | / | 2024-06 | / | / | 中英 | 文音 | [🤗HF](https://huggingface.co/2Noise/ChatTTS) | [ChatTTS](https://github.com/2noise/ChatTTS) | [2noise](https://github.com/2noise) | / |
| GLM-4V | 9B | 2024-06 | GLM-4 | / | 多语 | 文图 | [🤗HF](https://huggingface.co/THUDM/glm-4v-9b) | [GLM-4](https://github.com/THUDM/GLM-4) | [THUDM](https://github.com/THUDM) | / |
| HunyuanDiT | 1.5B | 2024-05 | multilingual T5 encoder | CLIP | 中英 | 文图 | [🤗](https://hf-mirror.com/Tencent-Hunyuan/HunyuanDiT) | **[HunyuanDiT](https://github.com/Tencent/HunyuanDiT)** | [Tencent](https://github.com/Tencent) | [Paper](https://arxiv.org/abs/2405.08748) |
| **CogVLM2** |  | 2024-05 | Meta-Llama-3-8B-Instruct | / | 中英 | 文图 | [🤗](https://hf-mirror.com/THUDM/cogvlm2-llama3-chat-19B) | [CogVLM](https://github.com/THUDM/CogVLM) | [Skip to content](https://github.com/THUDM#start-of-content) |  |
| 360VL | 8/70B | 2024-05 | LLama3 | CLIP-ViT | 中英 | 文图 | [🤗](https://hf-mirror.com/qihoo360) | [360VL](https://github.com/360CVGroup/360VL) | [360CVGroup](https://github.com/360CVGroup) |  |
| **XVERSE-V** | 13B | 2024-05 | **XVERSE-13B-Chat** | **clip-vit-large-patch14-224** | 中英 | 文图 | [🤖](https://modelscope.cn/models/xverse/XVERSE-V-13B/summary) | [XVERSE-V-13B](https://github.com/xverse-ai/XVERSE-V-13B) | [xverse-ai](https://github.com/xverse-ai) |  |
| MiniCPM-V 2.0 | 2.8B | 2024-04 | [MiniCPM-2.4B](https://github.com/OpenBMB/MiniCPM/) | SigLip-400M | 中英 | 文图 | [🤗](https://huggingface.co/openbmb/OmniLMM-12B/) [🤖](http://120.92.209.146:8081/) | **[MiniCPM-V](https://github.com/OpenBMB/MiniCPM-V)** | [OpenBMB](https://github.com/OpenBMB) | [Blog](https://openbmb.vercel.app/minicpm-v-2) |
| **Qwen-Audio** | 7B | 2024-03 | [Qwen-7B](https://github.com/QwenLM/Qwen) | [Whisper-large-v2](https://github.com/openai/whisper) | 中英 | 文音 | [🤗HF](https://huggingface.co/Qwen/Qwen-Audio) | [Qwen-Audio](https://github.com/QwenLM/Qwen-Audio)  | [Qwen](https://github.com/QwenLM) | [Paper](http://arxiv.org/abs/2311.07919) |
| DeepSeek-VL | 1.3/7B | 2024-03 | DeepSeek | SigLip/SAM | 中英 | 图文 | [🤗HF](https://huggingface.co/deepseek-ai/deepseek-vl-7b-chat) | [DeepSeek-VL](https://github.com/deepseek-ai/DeepSeek-VL) | [deepseek-ai](https://github.com/deepseek-ai) | [Paper](https://arxiv.org/abs/2403.05525) |
| **OmniLMM** | 3/12B | 2024-02 | MiniCPM | SigLip | 中英 | 图文 | [🤗HF](https://huggingface.co/openbmb/MiniCPM-V) | [OmniLMM](https://github.com/OpenBMB/OmniLMM) | [[OpenBMB](https://github.com/OpenBMB)](https://github.com/01-ai) |  |
| **MiniCPM-V** | 3B | 2024-02 | MiniCPM-2.4B | SigLip-400M | 中英 | 图文 | [🤗HF](https://huggingface.co/openbmb/MiniCPM-V) | [OmniLMM](https://github.com/OpenBMB/OmniLMM) | [[OpenBMB](https://github.com/OpenBMB)](https://github.com/01-ai) |  |
| Yi-VL | 6/34B | 2024-01 | Yi | [CLIP-VIT](https://huggingface.co/laion/CLIP-ViT-H-14-laion2B-s32B-b79K) | 中英 | 图文 | [[🤗HF\]](https://huggingface.co/01-ai) | [Yi](https://github.com/01-ai/Yi) | [01-ai](https://github.com/01-ai) |  |
| Lyrics | 14B | 2023-12 | / | / | 中英 | 图文 | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Ziya-Visual-Lyrics-14B) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) | [IDEA研究院](https://github.com/IDEA-CCNL) |  |
| Qwen-Audio | 7B | 2023-12 | [Qwen-7B](https://github.com/QwenLM/Qwen) | [Whisper-large-v2](https://github.com/openai/whisper) | 中英 | 文音 | [[🤗HF\]](https://huggingface.co/Qwen) | [Qwen-Audio](https://github.com/QwenLM/Qwen-Audio) | [Qwen](https://github.com/QwenLM) | [Paper](http://arxiv.org/abs/2311.07919) |
| SPHINX | 13B | 2023-10 | / | / | 中英 | 图文 | [[🤗HF\]](https://huggingface.co/Alpha-VLLM/SPHINX) | [LLaMA2-Accessory](https://github.com/Alpha-VLLM/LLaMA2-Accessory) | [Alpha-VLLM](https://github.com/Alpha-VLLM) |  |
| Skywork-MM | 13B | 2023-10 | / | / | 中英 | 图文 | [[🤗HF\]](https://huggingface.co/Skywork) | [Skywork](https://github.com/SkyworkAI/Skywork) | [SkyworkAI](https://github.com/SkyworkAI) | [Paper](https://github.com/will-singularity/Skywork-MM/blob/main/skywork_mm.pdf) |
| CogVLM | 7/14B | 2023-10 | Qwen | ViT | 中英 | 图文 | [[🤗HF\]](https://huggingface.co/CausalLM) | / | [CausalLM](https://huggingface.co/CausalLM) |  |
|           fuyu           |  8B   | 2023-10 |                              /                               |                              /                               | 中英 |   图文    |         [[🤗HF\]](https://huggingface.co/adept/fuyu-8b)         |                              /                               |      [Adept AI Labs](https://huggingface.co/adept)       |          [Blog](https://www.adept.ai/blog/fuyu-8b)           |
|       Ziya-Visual        |  14B  | 2023-10 |                            LLaMA                             |                         InstructBLIP                         | 中英 |   图文    | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Ziya-Visual-14B-Chat) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) |        [IDEA研究院](https://github.com/IDEA-CCNL)        |          [Paper](https://arxiv.org/abs/2310.08166)           |
|          CogVLM          |  17B  | 2023-10 |                         EVA2-CLIP-E                          |                         Vicuna-v1.5                          | 中英 |   图文    |                           [TODO]()                           | [CogVLM](https://github.com/THUDM/CogVLM) |            [THUDM](https://github.com/THUDM)             | [Paper](https://github.com/THUDM/CogVLM/blob/main/assets/cogvlm-paper.pdf) |
|         idefics          | 9/80B | 2023-10 |     [LLaMA](https://huggingface.co/huggyllama/llama-65b)     | [CLIP-ViT](https://huggingface.co/laion/CLIP-ViT-H-14-laion2B-s32B-b79K) | 中英 |   图文    |  [[🤗HF\]](https://huggingface.co/HuggingFaceM4/idefics-9b)   |                              /                               |  [HuggingFaceM4](https://huggingface.co/HuggingFaceM4)   | [log](https://github.com/huggingface/m4-logs/blob/master/memos/README.md) |
|    InternLM-XComposer    |  7B   | 2023-10 |  [InternLM](https://github.com/InternLM/InternLM/tree/main)  |                           EVA-CLIP                           | 中英 |   图文    | [[🤗HF\]](https://huggingface.co/internlm/internlm-xcomposer-vl-7b) | [InternLM-XComposer](https://github.com/InternLM/InternLM-XComposer) |         [InternLM](https://github.com/InternLM)          |        [Report](https://arxiv.org/pdf/2309.15112.pdf)        |
|        WeMix-LLM         |  13B  | 2023-09 |                            LLama2                            |                              /                               | 中英 |   图文    | [[🤗HF\]](https://huggingface.co/Alpha-VLLM/WeMix-LLaMA2-13B-MM) | [WeMix-LLM](https://github.com/Alpha-VLLM/WeMix-LLM) |       [Alpha-VLLM](https://github.com/Alpha-VLLM)        |                                                              |
|          Vally           | 7/13B | 2023-08 |                  BelleGroup/BELLE-LLaMA-EXT                  |            OFA-Sys/chinese-clip-vit-large-patch14            | 中英 |   图文    | [[🤗HF\]](https://huggingface.co/Zhaoziwang/chinese_valley7b_v1) [[🤗HF\]](https://huggingface.co/Zhaoziwang/chinese_valley13b_v1) | [Valley](https://github.com/RupertLuo/Valley) |          [罗瑞璞](https://github.com/RupertLuo)          |          [Paper](https://arxiv.org/abs/2306.07207)           |
|         SALMONN          |   /   | 2023-08 |                              /                               |                              /                               | 中英 |   语音    |                           [TODO]()                           | [SALMONN](https://github.com/bytedance/SALMONN) |        [Bytedance](https://github.com/bytedance)         |                                                              |
|         IDEFICS          | 9/80B | 2023-08 |     [llama](https://huggingface.co/huggyllama/llama-65b)     | [CLIP-ViT](https://huggingface.co/laion/CLIP-ViT-H-14-laion2B-s32B-b79K) | 中英 | 图文-通用 | [[🤗HF\]](https://huggingface.co/HuggingFaceM4/idefics-9b) | [m4-logs](https://github.com/huggingface/m4-logs) |  [HuggingFaceM4](https://huggingface.co/HuggingFaceM4)   |      [Paper](https://huggingface.co/papers/2306.16527)       |
|         Qwen-VL          |  7B   | 2023-08 |         [Qwen-7B](https://github.com/QwenLM/Qwen-7B)         | [Openclip ViT-bigG](https://github.com/mlfoundations/open_clip) | 中英 |   通用    |         [[🤗HF\]](https://huggingface.co/Qwen/Qwen-VL)          | [Qwen-VL](https://github.com/QwenLM/Qwen-VL) |           [阿里云](https://github.com/QwenLM)            |                                                              |
|       Qwen-VL-chat       |  7B   | 2023-08 |         [Qwen-7B](https://github.com/QwenLM/Qwen-7B)         | [Openclip ViT-bigG](https://github.com/mlfoundations/open_clip) | 中英 |   通用    |       [[🤗HF\]](https://huggingface.co/Qwen/Qwen-VL-Chat)       | [Qwen-VL](https://github.com/QwenLM/Qwen-VL) |           [阿里云](https://github.com/QwenLM)            |                                                              |
|          LLasM           |  7B   | 2023-07 | [Chinese-Llama2](https://github.com/LinkSoul-AI/Chinese-Llama-2-7b) |                       whisper-large-v2                       | 中英 |   语音    |    [[🤗HF\]](https://huggingface.co/LinkSoul/LLaSM-Cllama2)     | [LLaSM](https://github.com/LinkSoul-AI/LLaSM) |        [北京灵琐](https://github.com/LinkSoul-AI)        |                                                              |
|      Chinese-LLaVA       |  7B   | 2023-07 | [Chinese-Llama2](https://github.com/LinkSoul-AI/Chinese-Llama-2-7b) |                           Clip-vit                           | 中英 |   视觉    | [[🤗HF\]](https://huggingface.co/LinkSoul/Chinese-LLaVA-Cllama2) | [Chinese-LLaVA](https://github.com/LinkSoul-AI/Chinese-LLaVA) |        [北京灵琐](https://github.com/LinkSoul-AI)        |                                                              |
|        RemoteGLM         |  6B   | 2023-07 |                         VisualGLM-6B                         |                         VisualGLM-6B                         | 中文 |   遥感    |                           [TODO]()                           | [RemoteGLM](https://github.com/lzw-lzw/RemoteGLM) |          [lzw-lzw](https://github.com/lzw-lzw)           |                                                              |
|        VisualCLA         |  7B   | 2023-07 | [Chinese-Alpaca-Plus](https://github.com/ymcui/Chinese-LLaMA-Alpaca/wiki/%E6%A8%A1%E5%9E%8B%E5%90%88%E5%B9%B6%E4%B8%8E%E8%BD%AC%E6%8D%A2) | [CLIP-ViT-L/14](https://huggingface.co/openai/clip-vit-large-patch14) | 中文 |   视觉    | [[🤗HF\]](https://pan.baidu.com/s/1bBF5QHoZxHRnWeTPHL19CQ?pwd=xxbg) | [Visual-Chinese-LLaMA-Alpaca](https://github.com/airaria/Visual-Chinese-LLaMA-Alpaca) |        [Ziqing Yang](https://github.com/airaria)         |                                                              |
|          yuren           |  7B   | 2023-07 | [baichuan-7B](https://huggingface.co/baichuan-inc/baichuan-7B) | [CLIP](https://huggingface.co/laion/CLIP-ViT-L-14-DataComp.XL-s13B-b90K) | 中英 |   视觉    |   [[🤗HF\]](https://huggingface.co/pleisto/yuren-baichuan-7b)   | [yuren-baichuan-7b](https://github.com/pleisto/yuren-baichuan-7b) |          [Pleisto](https://github.com/pleisto)           |                                                              |
|       VisCPM-Chat        |  10B  | 2023-06 |                           CPM-Bee                            |                           Q-Former                           | 中英 |   视觉    |      [[🤗HF\]](https://huggingface.co/openbmb/VisCPM-Chat)      | [VisCPM](https://github.com/OpenBMB/VisCPM) |          [OpenBMB](https://github.com/OpenBMB)           |                                                              |
|       VisCPM-Paint       |  10B  | 2023-06 |                           CPM-Bee                            | [Stable Diffusion 2.1](https://github.com/Stability-AI/stablediffusion) | 中英 |   视觉    |     [[🤗HF\]](https://huggingface.co/openbmb/VisCPM-Paint)      | [VisCPM](https://github.com/OpenBMB/VisCPM) |          [OpenBMB](https://github.com/OpenBMB)           |                                                              |
|        XrayPULSE         |  7B   | 2023-06 |         [PULSE](https://github.com/openmedlab/PULSE)         |       [MedCLIP](https://github.com/RyanWangZf/MedCLIP)       | 中文 |   医学    | [[🤗HF\]](https://drive.google.com/file/d/1VsO61-3DFuK4ysGPvoD4_JZaRFKvAJR_/view?usp=drive_link) | [XrayPULSE](https://github.com/openmedlab/XrayPULSE) |       [OpenMEDLab](https://github.com/OpenMEDLab)        |                                                              |
|         SEEChat          |  6B   | 2023-06 |        [ChatGLM](https://github.com/THUDM/ChatGLM-6B)        |                           CLIP-ViT                           | 中文 |     /     |        [[🤗HF\]](https://github.com/360CVGroup/SEEChat)         | [SEEChat](https://github.com/360CVGroup/SEEChat) |           [360](https://github.com/360CVGroup)           |                                                              |
| Ziya-BLIP2-14B-Visual-v1 |  14B  | 2023-06 | [LLaMA-13B](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1) |                            BLIP2                             | 中英 |   通用    | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Ziya-BLIP2-14B-Visual-v1) | [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM) |        [IDEA研究院](https://github.com/IDEA-CCNL)        |                                                              |
|    Video-LLaMA-BiLLA     |  7B   | 2023-05 | [BiLLa-7B]([BiLLa-7B](https://huggingface.co/Neutralzz/BiLLa-7B-SFT)) |    [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4)     | 中英 |   通用    | [[🤗HF\]](https://huggingface.co/DAMO-NLP-SG/Video-LLaMA-Series/resolve/main/finetune-billa7b-zh.pth) | [Video-LLaMA](https://github.com/DAMO-NLP-SG/Video-LLaMA) |    [达摩院多语言NLP](https://github.com/DAMO-NLP-SG)     |          [Paper](https://arxiv.org/abs/2306.02858)           |
|     Video-LLaMA-Ziya     |  13B  | 2023-05 | [Ziya-13B](https://huggingface.co/IDEA-CCNL/Ziya-LLaMA-13B-v1) |    [MiniGPT-4](https://github.com/Vision-CAIR/MiniGPT-4)     | 中英 |   通用    | [[🤗HF\]](https://huggingface.co/DAMO-NLP-SG/Video-LLaMA-Series/resolve/main/finetune-ziya13b-zh.pth) | [Video-LLaMA](https://github.com/DAMO-NLP-SG/Video-LLaMA) |    [达摩院多语言NLP](https://github.com/DAMO-NLP-SG)     |          [Paper](https://arxiv.org/abs/2306.02858)           |
|         XrayGLM          |  6B   | 2023-05 |      [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)       |      [BLIP2-Qformer](https://arxiv.org/abs/2301.12597)       | 中英 |   医学    | [[🤗HF\]](https://huggingface.co/wangrongsheng/XrayGLM-300) | [XrayGLM](https://github.com/WangRongsheng/XrayGLM) | [澳门理工大学](https://www.mpu.edu.mo/esca/zh/index.php) |                                                              |
|          X-LLM           |       | 2023-05 |        [ChatGLM](https://github.com/THUDM/ChatGLM-6B)        |          [ViT-g](https://arxiv.org/abs/2106.04560)           | 中文 |     /     |                           [TODO]()                           | [X-LLM](https://github.com/phellonchen/X-LLM) |     [中科院自动化所](https://github.com/phellonchen)     |        [Paper](https://arxiv.org/pdf/2305.04160.pdf)         |
|        VisualGLM         |  6B   | 2023-05 |      [ChatGLM-6B](https://github.com/THUDM/ChatGLM-6B)       |      [BLIP2-Qformer](https://arxiv.org/abs/2301.12597)       | 中英 |   视觉    |      [[🤗HF\]](https://huggingface.co/THUDM/visualglm-6b)       | [VisualGLM-6B](https://github.com/THUDM/VisualGLM-6B) |           [清华大学](https://github.com/THUDM)           |                                                              |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## ReasoningLLM

> 收集推理能力比较突出的中文大模型

|      模型       | 大小 | 时间    | 语言 | 领域 |                             下载                             |                           项目地址                           |                 机构/个人                 | 结构 |                      文                       |
| :-------------: | :--: | ------- | :--: | :--: | :----------------------------------------------------------: | :----------------------------------------------------------: | :---------------------------------------: | :--: | :-------------------------------------------: |
| MiniMax-M2.7 | A10/230B | 2026-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/MiniMaxAI/MiniMax-M2.7) | [GitHub](https://github.com/MiniMax-AI/MiniMax-M2.7) | [MiniMax-AI](https://github.com/MiniMax-AI) | MoE | [Blog](https://www.minimax.io/news/minimax-m27-en) |
| Qwen3.5 | 0.5/2/4/9/27/35/122/397B | 2026-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/Qwen/qwen35) | [Qwen3.5](https://github.com/QwenLM/Qwen3.5) | [QwenLM](https://github.com/QwenLM) | MoE | [Blog](https://qwen.ai/blog?id=qwen3.5) |
| Step-3.5-Flash | / | 2026-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/stepfun-ai/Step-3.5-Flash) | / | [stepfun-ai](https://github.com/stepfun-ai) | / | / |
| GLM-5 | A40/744B | 2026-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/zai-org/GLM-5) | / | [zai-org](https://github.com/zai-org) | / | [blog](https://z.ai/blog/glm-5) |
| MiniMax-M2.5 | / | 2026-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/MiniMaxAI/MiniMax-M2.5) | / | [MiniMaxAI](https://huggingface.co/MiniMaxAI) | / | / |
| Kimi-K2.5 | 1T | 2026-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/moonshotai/Kimi-K2.5) | / | [moonshotai](https://huggingface.co/moonshotai) | moe | [paper](https://arxiv.org/abs/2602.02276) |
| Ring-2.5-1T | 1T | 2026-02 | 中英 | 通用 | [🤗HF](https://huggingface.co/inclusionAI/Ring-2.5-1T) | / | [inclusionAI](https://huggingface.co/inclusionAI) | / | / |
| DeepSeek-V3.2 | / | 2025-12 | 中英 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-V3.2) | [DeepSeek-V3.2-Exp](https://github.com/deepseek-ai/DeepSeek-V3.2-Exp) | [deepseek-ai](https://github.com/deepseek-ai) | MoE | [**Technical Report**](https://huggingface.co/deepseek-ai/DeepSeek-V3.2/blob/main/assets/paper.pdf) |
| **Tongyi DeepResearch** | A3/30B | 2025-09 | 中英 | 通用 | [🤗HF](https://huggingface.co/Alibaba-NLP/Tongyi-DeepResearch-30B-A3B) | [DeepResearch](https://github.com/Alibaba-NLP/DeepResearch) | [Alibaba-NLP](https://github.com/Alibaba-NLP)[<br/>](https://github.com/Alibaba-NLP/DeepResearch) | MoE | [Tech Blog](https://tongyi-agent.github.io/blog/introducing-tongyi-deep-research) |
| **Qwen3-Next** | A3/80B | 2025-09 | 中英 | 通用 | [🤗HF](https://huggingface.co/Qwen/Qwen3-Next-80B-A3B-Thinking) | [Qwen3](https://github.com/QwenLM/Qwen3) | [QwenLM](https://github.com/QwenLM) | MoE | [Qwen3-Next](https://qwen.ai/blog?id=4074cca80393150c248e508aa62983f9cb7d27cd&from=research.latest-advancements-list) |
| Magistral Small 1.2 | 24B | 2025-09 | 多语 | 通用 | [**Hugging Face**](https://huggingface.co/baichuan-inc/Baichuan-M2-32B) | / | [mistralai](https://huggingface.co/mistralai) | CD | [blog post](https://mistral.ai/news/magistral/) |
| gpt-oss-20B | A2/20B | 2025-08 | 中英 | 通用 | [🤗HF](https://huggingface.co/openai/gpt-oss-20b) | [gpt-oss](https://github.com/openai/gpt-oss) | [openai](https://github.com/openai) | MoE | [**OpenAI blog**](https://openai.com/index/introducing-gpt-oss/) |
| gpt-oss-120B | A5/120B | 2025-08 | 中英 | 通用 | [🤗HF](https://huggingface.co/tencent/Hunyuan-0.5B-Instruct) | [gpt-oss](https://github.com/openai/gpt-oss) | [openai](https://github.com/openai) | MoE | [**OpenAI blog**](https://openai.com/index/introducing-gpt-oss/) |
| Baichuan-M2 | 32B | 2025-08 | 中英 | 医疗 | [**Hugging Face**](https://huggingface.co/baichuan-inc/Baichuan-M2-32B) | [Baichuan-M2-32B](https://github.com/baichuan-inc/Baichuan-M2-32B) | [baichuan-inc](https://github.com/baichuan-inc) | CD | [technical blog](https://www.baichuan-ai.com/blog/baichuan-M2) |
| **Ovis2.5** | 2/9B | 2025-08 | 中英 | 多模态 | [🤗HF](https://huggingface.co/AIDC-AI/Ovis2.5-9B) | [Ovis](https://github.com/AIDC-AI/Ovis) | [AIDC-AI](https://github.com/AIDC-AI) | CD | [Paper](https://arxiv.org/abs/2405.20797) |
| GLM-4.5V | 108B | 2025-07 | 中英 |  多模态  | [**Hugging Face**](https://huggingface.co/zai-org/GLM-4.5V) |     [GLM-V](https://github.com/zai-org/GLM-V)     |         [zai-org](https://github.com/zai-org)         | MoE  | [Paper](https://arxiv.org/abs/2507.01006) |
| GLM-4.5 | A32/355B | 2025-07 | 中英 | 通用 | [**Hugging Face**](https://huggingface.co/zai-org/GLM-4.5-Base) | [GLM-4.5](https://github.com/zai-org/GLM-4.5) | [zai-org](https://github.com/zai-org) | MoE | [technical blog](https://z.ai/blog/glm-4.5) |
| GLM-4.5-Air | 106B-A12B | 2025-07 | 中英 |  通用  | [**Hugging Face**](https://huggingface.co/zai-org/GLM-4.5-Base) |     [GLM-4.5](https://github.com/zai-org/GLM-4.5)     |         [zai-org](https://github.com/zai-org)         | MoE  | [technical blog](https://z.ai/blog/glm-4.5) |
| Hunyuan | 0.5/4/7B | 2025-07 | 中英 | 通用 | [🤗HF](https://huggingface.co/tencent/Hunyuan-0.5B-Instruct) | [Tencent-Hunyuan](https://github.com/Tencent-Hunyuan) | [Tencent-Hunyuan](https://github.com/Tencent-Hunyuan) | / | / |
| Qwen3-Thinking-2507 | A3/30B | 2025-07 | 中英 | 通用 | [**🤗 Huggingface** ](https://huggingface.co/Qwen/Qwen3-30B-A3B-Thinking-2507) | [Qwen3](https://github.com/QwenLM/Qwen3) | [QwenLM](https://github.com/QwenLM) | MoE | [Paper](https://arxiv.org/abs/2505.09388) |
| Step3 | A38/321B | 2025-07 | 中英 | 多模态 | [HF](https://huggingface.co/stepfun-ai/step3) | [Step3](https://github.com/stepfun-ai/Step3) | [stepfun-ai](https://github.com/stepfun-ai) | MoE | [Paper](https://arxiv.org/abs/2507.19427) |
| Dhanishtha-2.0 | 14B | 2025-07 | 多语 | 通用 | [**Hugging Face**](https://huggingface.co/HelpingAI/Dhanishtha-2.0-preview) | / | [HelpingAI](https://huggingface.co/HelpingAI) | CD | / |
| GLM-4.1V-Thinking | 9B | 2025-07 | 中英 | 多模态 |    [🤗HF](https://huggingface.co/THUDM/GLM-4.1V-9B-Thinking)    |  [GLM-4.1V-Thinking](https://github.com/THUDM/GLM-4.1V-Thinking)  |   [THUDM](https://github.com/THUDM)   | / | [paper](https://arxiv.org/abs/2507.01006) |
| Kimi-VL-Thinking-2506 | A3B | 2025-06 | 中英 | 多模态 | [🤗HF](https://huggingface.co/moonshotai/Kimi-VL-A3B-Thinking-2506) | [Kimi-VL](https://github.com/MoonshotAI/Kimi-VL) | [MoonshotAI](https://github.com/MoonshotAI/Kimi-VL) | / | [**📄 Tech Report** ](https://arxiv.org/abs/2504.07491) |
| Hunyuan-A13B | A13/80B | 2025-06 | 中英 | 通用 | [**Hugging Face**](https://huggingface.co/tencent/Hunyuan-A13B-Instruct) | [Hunyuan-A13B](https://github.com/Tencent-Hunyuan/Hunyuan-A13B) | [Tencent-Hunyuan](https://github.com/Tencent-Hunyuan) | MoE | [**Technical Report**](https://github.com/Tencent-Hunyuan/Hunyuan-A13B/blob/main/report/Hunyuan_A13B_Technical_Report.pdf) |
| LongWriter-Zero | 32B | 2025-06 | 中英 | / |    [🤗HF](https://huggingface.co/THU-KEG/LongWriter-Zero-32B)    |  /  |   [THU-KEG](https://github.com/THU-KEG)   | / | [Paper](https://arxiv.org/abs/2506.18841) |
| MiniMax-M1 | A46/456B | 2025-06 | 中英 | 通用 |    [🤗HF](https://huggingface.co/MiniMaxAI)    |  [MiniMax-M1](https://github.com/MiniMax-AI/MiniMax-M1)  |   [MiniMax-AI](https://github.com/MiniMax-AI)   | MoE  | [Paper](https://arxiv.org/abs/2506.13585) |
| DeepSeek-R1-0528 | A37/671B | 2025-05 | 中英 | 通用 |    [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-R1)    |  [DeepSeek-R1](https://github.com/deepseek-ai/DeepSeek-R1)  |   [deepseek-ai](https://github.com/deepseek-ai)   | MoE  | [**Paper Link**👁️](https://github.com/deepseek-ai/DeepSeek-R1/blob/main/DeepSeek_R1.pdf) |
|   QwenLong-L1    |   32B    | 2025-05 | 中英 | 通用 | [🤗HF](https://huggingface.co/Tongyi-Zhiwen/QwenLong-L1-32B) | [QwenLong-L1](https://github.com/Tongyi-Zhiwen/QwenLong-L1) | [Tongyi-Zhiwen](https://github.com/Tongyi-Zhiwen) |  CD  | [Paper](https://arxiv.org/abs/2505.17667) |
| GLM-Z1-0414 | 32B | 2025-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/THUDM/glm-4-0414-67f3cbcb34dd9d252707cb2e) | [GLM-4](https://github.com/THUDM/GLM-4) | [THUDM](https://github.com/THUDM) |  |  |
|    DeepCoder     | 1.5/14B | 2025-04 | 中英 | 代码 | [🤗HF](https://huggingface.co/agentica-org/DeepCoder-14B-Preview) | [rllm](https://github.com/agentica-project/rllm) | [agentica-project](https://github.com/agentica-project) | CD |  |
| Kimi-VL-Thinking | A3/16B | 2025-04 | 中英 | 多模态 | [🤗HF](https://huggingface.co/moonshotai/Kimi-VL-A3B-Thinking) | [Kimi-VL](https://github.com/MoonshotAI/Kimi-VL) | [MoonshotAI](https://github.com/MoonshotAI) |  MoE  | [**Tech Report** ](https://arxiv.org/abs/2504.07491) |
| Skywork-OR1 | 7/32B | 2025-04 | 中英 | 通用 | [🤗HF](https://huggingface.co/Skywork/Skywork-OR1-32B-Preview) | [Skywork-OR1](https://github.com/SkyworkAI/Skywork-OR1) | [SkyworkAI](https://github.com/SkyworkAI)/ | MoE | [Notion Blog](https://capricious-hydrogen-41c.notion.site/Skywork-Open-Reaonser-Series-1d0bc9ae823a80459b46c149e4f51680) |
| Skywork-R1V | 38B | 2025-03 | 中英 | 多模态 | [🤗HF](https://huggingface.co/Skywork/Skywork-R1V-38B) | [Skywork-R1V](https://github.com/SkyworkAI/Skywork-R1V) | [SkyworkAI](https://github.com/SkyworkAI) | CD | [Paper](https://github.com/SkyworkAI/Skywork-R1V/blob/main/Skywork_R1V.pdf) |
| Fin-R1 | 7B | 2025-03 | 中英 | 金融 | [🤗HF](https://huggingface.co/SUFE-AIFLM-Lab/Fin-R1) | [Fin-R1](https://github.com/SUFE-AIFLM-Lab/Fin-R1) | [SUFE-AIFLM-Lab](https://github.com/SUFE-AIFLM-Lab) |  CD  | [Paper](https://arxiv.org/abs/2503.16252) |
| QwQ-32B | 32B  | 2025-03 | 中英 | 通用 | [🤗HF](https://huggingface.co/Qwen/QwQ-32B) |    /     | [QwenLM](https://github.com/QwenLM) |  CD  | [📑 blog](https://qwenlm.github.io/blog/qwq-32b/) |
| DeepSeek-R1 | A37/671B | 2025-01 | 中英 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-R1) | [DeepSeek-R1](https://github.com/deepseek-ai/DeepSeek-R1) | [deepseek-ai](https://github.com/deepseek-ai) |  MoE  | [**Paper Link**👁️](https://github.com/deepseek-ai/DeepSeek-R1/blob/main/DeepSeek_R1.pdf) |
| DeepSeek-R1-Zero | A37/671B | 2025-01 | 中英 | 通用 | [🤗HF](https://huggingface.co/deepseek-ai/DeepSeek-R1-Zero) | [DeepSeek-R1](https://github.com/deepseek-ai/DeepSeek-R1) | [deepseek-ai](https://github.com/deepseek-ai) | MoE | [**Paper Link**👁️](https://github.com/deepseek-ai/DeepSeek-R1/blob/main/DeepSeek_R1.pdf) |
| DeepSeek-R1-Distill-Qwen | 1.5/7/14/32B | 2025-01 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/deepseek-ai/deepseek-r1-678e1e131c0169c0bc89728d) | [DeepSeek-R1](https://github.com/deepseek-ai/DeepSeek-R1) | [deepseek-ai](https://github.com/deepseek-ai) | MoE | [**Paper Link**👁️](https://github.com/deepseek-ai/DeepSeek-R1/blob/main/DeepSeek_R1.pdf) |
| MiniMax-Text-01 | A46/456B | 2025-01 | 中英 | 通用 | [🤗HF](https://huggingface.co/MiniMaxAI/MiniMax-Text-01) | [MiniMax-01](https://github.com/MiniMax-AI/MiniMax-01) | [MiniMax-AI](https://github.com/MiniMax-AI) |  MoE  | [Paper](https://arxiv.org/abs/2501.08313) |
| MiniMax-VL-01 | A46/456B | 2025-01 | 中英 | 多模态 |                              [🤗HF](https://huggingface.co/MiniMaxAI/MiniMax-VL-01)                              | [MiniMax-01](https://github.com/MiniMax-AI/MiniMax-01) | [MiniMax-AI](https://github.com/MiniMax-AI) | MoE | [Paper](https://arxiv.org/abs/2501.08313) |
| Sky-T1 | 32B | 2025-01 | 中英 | 通用 | [🤗HF](https://huggingface.co/NovaSky-AI/Sky-T1-32B-Preview) | [SkyThought](https://github.com/NovaSky-AI/SkyThought) | [NovaSky-AI](https://github.com/NovaSky-AI) |  CD  | [Blog](https://novasky-ai.github.io/posts/sky-t1/) |
| Search-O1 |  | 2025-01 | 中英 | 通用 |                              /                              | [Search-o1](https://github.com/sunnynexus/Search-o1) | [sunnynexus](https://github.com/sunnynexus) | CD | [Paper](https://arxiv.org/abs/2501.05366) |
| HuatuoGPT-o1 | 7/8/70/72B | 2025-01 | 中英 | 医疗 | [🤗HF](https://huggingface.co/collections/FreedomIntelligence/huatuogpt-o1-677261a3711767cce7c64e13) | [HuatuoGPT-o1](https://github.com/FreedomIntelligence/HuatuoGPT-o1) | [FreedomIntelligence](https://github.com/FreedomIntelligence)/ |  CD  | [Paper](https://arxiv.org/pdf/2412.18925) |
| QwQ-32B-Preview | 32B  | 2024-11 | 中英 | 通用 |      [🤗HF](https://huggingface.co/Qwen/QwQ-32B-Preview)      |                              /                               |    [QwenLM](https://github.com/QwenLM)    |  CD  |                                               |
|    Marco-o1     |  7B  | 2024-11 | 中英 | 通用 |        [🤗HF](https://huggingface.co/AIDC-AI/Marco-o1)        |       [Marco-o1](https://github.com/AIDC-AI/Marco-o1)        |   [AIDC-AI](https://github.com/AIDC-AI)   |  CD  | [**Paper**](https://arxiv.org/abs/2411.14405) |
| Skywork-01-Open |  8B  | 2024-11 | 中英 | 通用 | [🤗HF](https://huggingface.co/collections/Skywork/skywork-o1-open-67453df58e12f6c3934738d0) | [skywork-o1-prm-inference](https://github.com/SkyworkAI/skywork-o1-prm-inference) | [SkyworkAI](https://github.com/SkyworkAI) |  CD  | [Blog](https://nexusflow.ai/blogs/athene-v2)  |
|     HK-01aw     |  8B  | 2024-11 | 中文 | 法律 |       [🤗HF](https://huggingface.co/HKAIR-Lab/HK-O1aw)        |       [HK-O1aw](https://github.com/HKAIR-Lab/HK-O1aw)        | [HKAIR-Lab](https://github.com/HKAIR-Lab) |  CD  |                                               |
| QVQ-72B-Preview | 72B  | 2024-12 | 中英 | 多模 | [🤗 HF](https://huggingface.co/collections/Qwen/qvq-676448c820912236342b9888) | [Qwen2-VL](https://github.com/QwenLM/Qwen2-VL) | [QwenLM](https://github.com/QwenLM) |  |[Blog](https://qwenlm.github.io/zh/blog/qvq-72b-preview/)|

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 中文指令数据集

> 收集包含中文的指令数据集，用于微调语言模型。

|            名称            | 大小  | 时间    | 语言 |                             下载                             |                           项目地址                           |                             作者                             |                     备注                      |
| :------------------------: | :---: | ------- | :--: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :-------------------------------------------: |
|         FinCorpus          |  50G  | 2023-09 | 中文 | [dataset](https://huggingface.co/datasets/Duxiaoman-DI/FinCorpus) |     [XuanYuan](https://github.com/Duxiaoman-DI/XuanYuan)     |          [度小满](https://github.com/Duxiaoman-DI)           |                   金融领域                    |
|        TransGPT-sft        | 346k  | 2023-07 | 中文 | [dataset](https://huggingface.co/datasets/DUOMO-Lab/TransGPT-sft) |        [TransGPT](https://github.com/DUOMO/TransGPT)         |           [北京交通大学](https://github.com/DUOMO)           |                                               |
|        TransGPT-pt         |  58k  | 2023-07 | 中文 | [dataset](https://huggingface.co/datasets/DUOMO-Lab/TransGPT-pt) |        [TransGPT](https://github.com/DUOMO/TransGPT)         |           [北京交通大学](https://github.com/DUOMO)           |                                               |
|  ShareGPT-Chinese-English  |  90K  | 2023-07 | 中英 | [dataset](https://huggingface.co/datasets/shareAI/ShareGPT-Chinese-English-90k) | [llama2-Chinese-chat](https://github.com/CrazyBoyM/llama2-Chinese-chat) |            [Ke Bai](https://github.com/CrazyBoyM)            |                                               |
|  educhat-sft-002-data-osm  | 400w  | 2023-06 | 中英 | [dataset](https://huggingface.co/datasets/ecnu-icalk/educhat-sft-002-data-osm) |       [EduChat](https://github.com/icalk-nlp/EduChat)        |         [华东师范大学](https://github.com/icalk-nlp)         |                     教育                      |
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

### Embedding

> MTEB排行榜:  https://huggingface.co/spaces/mteb/leaderboard [镜像](https://hf-mirror.com/spaces/mteb/leaderboard)

|           模型           |  大小   | 时间    | 语言 |     领域     |                             下载                             |                           项目地址                           |                       机构/个人                        |                             文                             |
| :----------------------: | :-----: | ------- | :--: | :----------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------: | :----------------------------------------------------------: |
| Qwen3-Embedding | 0.6/4/8B | 2025-06 | 多语 | 通用 | [[🤗HF]](https://huggingface.co/Qwen/Qwen3-Embedding-0.6B) | [Qwen3-Embedding](https://github.com/QwenLM/Qwen3-Embedding) | [QwenLM](https://github.com/QwenLM) | [Arxiv](https://arxiv.org/abs/2506.05176) |
| JinaColBERT V2 | large | 2024-08 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/jinaai/jina-colbert-v2) | / | [Jina AI](https://huggingface.co/jinaai) | [Paper](https://arxiv.org/abs/2408.16672) |
| Conan-embedding-v1 | large | 2024-08 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/TencentBAC/Conan-embedding-v1) | / | [TencentABC](https://huggingface.co/TencentBAC) | [Paper](https://arxiv.org/abs/2408.15710) |
| xiaobu-v2 | large | 2024-07 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/lier007/xiaobu-embedding-v2) | / | [lier007](https://huggingface.co/lier007) |  |
| zpoint_large | Large | 2024-06 | 中文 | 通用 | [[🤗HF\]](https://huggingface.co/iampanda/zpoint_large_embedding_zh) | / | [**yang**](https://huggingface.co/iampanda) |  |
| BCE | 279M | 2024-01 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/maidalun1020/bce-embedding-base_v1) | [BCEmbedding](https://github.com/netease-youdao/BCEmbedding) | [netease-youdao](https://github.com/netease-youdao) |  |
| Cohere | Base | 2023-09 | 多语 | 通用 | [[🤗HF\]](https://huggingface.co/Cohere) | / | [Cohere](https://huggingface.co/Cohere) | [Blog](https://txt.cohere.com/introducing-embed-v3/) |
| jina | Base | 2023-10 | 中英 | 通用 | [[🤗HF\]](https://huggingface.co/jinaai/jina-embeddings-v2-base-zh) | / | [Jina AI](https://huggingface.co/jinaai) |  |
| Dmeta | **400MB** | 2024-02 | 中文 | 通用 | [[🤗HF\]](https://hf-mirror.com/DMetaSoul/Dmeta-embedding) | / | [DMetaSoul](https://hf-mirror.com/DMetaSoul) |  |
| bge-m3 |  | 2024-02 | 中文 | 通用 | [[🤗HF\]](https://hf-mirror.com/BAAI) | / | [BAAI](https://hf-mirror.com/BAAI) | [Paper](https://arxiv.org/pdf/2402.03216.pdf) |
| tao-8k |  | 2023-11 | 中文 | 通用 | [[🤗HF\]](https://hf-mirror.com/amu) |  | [amu](https://hf-mirror.com/amu) |  |
| bge | s/b/l | 2023-10 | 中文 | 通用 | [[🤗HF\]](https://hf-mirror.com/BAAI) | / | [BAAI](https://hf-mirror.com/BAAI) |  |
| gte-zh | s/b/l | 2023-08 | 中文 | 通用 | [[🤗HF\]](https://hf-mirror.com/DMetaSoul/Dmeta-embedding) | / | Alibaba DAMO | [Paper](arXiv:2308.03281) |
| m3e | s/b/l | 2023-06 | 中文 | 通用 | [[🤗HF\]](https://hf-mirror.com/moka-ai) | / | [Moka-AI](https://hf-mirror.com/moka-ai) |  |
| LaBSE |  |  | 多语 | 通用 | [[🤗HF\]](https://hf-mirror.com/sentence-transformers/LaBSE) | / | [Sentence Transformers](https://hf-mirror.com/sentence-transformers) | |

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 大模型评估基准

### 1. C-Eval 

C-Eval 是一个全面的中文基础模型评估套件。它包含了13948个多项选择题，涵盖了52个不同的学科和四个难度级别，查看[论文](https://arxiv.org/abs/2305.08322)了解更多细节。

[[官方网站](https://cevalbenchmark.com/)]   [[Github](https://github.com/SJTU-LIT/ceval)]  [[论文](https://arxiv.org/abs/2305.08322)] 

### 2. FlagEval 

FlagEval是一个面向AI基础模型的评测工具包。我们的目标是探索和集合科学、公正、开放的基础模型评测基准、方法及工具，对多领域（如语言、语音、视觉及多模态）的基础模型进行多维度（如准确性、效率、鲁棒性等）的评测。我们希望通过对基础模型的评测，加深对基础模型的理解，促进相关的技术创新及产业应用。

[[官方网站](https://cevalbenchmark.com/)]   [[Github](https://github.com/FlagOpen/FlagEval)] 

### 3. SuperCLUElyb 

SuperCLUE琅琊榜，这是一个中文通用大模型对战评价基准，它以众包的方式提供匿名、随机的对战。在本文中，我们发布了初步的结果和基于Elo评级系统的排行榜，Elo评级是国际象棋和其他竞技游戏中广泛使用的评级系统。我们邀请整个社区加入这项工作，贡献新的模型，并通过提问和投票选出你最喜欢的答案来评估它们。

[[官方网站](https://www.superclueai.com/)]   [[Github](https://github.com/CLUEbenchmark/SuperCLUElyb)]

### 4. XiezhiBenchmark 

该基准包括来自13个不同学科的516个学科的220,000个多项选择题，以及15,000个来自单一学科和多个学科的问题。我们对47个最新的大型语言模型在Xiezhi上进行了评估，结果表明在科学、工程、农学、医学和艺术等领域，大型语言模型的表现超过了人类的平均水平，但在经济学、法学、教育学、文学、历史和管理学等领域，人类的表现仍然远远超过了大型语言模型。

[[官方网站]()]   [[Github](https://github.com/mikegu721/xiezhibenchmark)] [[论文](https://arxiv.org/abs/2306.05783)]

### 5. Open LLM Leaderboard

由HuggingFace组织的一个LLM评测榜单，目前已评估了较多主流的开源LLM模型，以英文为主。主要目标是跟踪、排名和评估最新的大语言模型和聊天机器人，让所有人方便的观察到开源社区的进展和评估这些模型。这个排行榜有一个关键优势，社区中的任何成员都可以提交模型，并在 Hugging Face 的 GPU 集群上自动评估。

[[官方网站](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)] 

### 6. 中文大模型安全评测平台 

大模型安全测评依托于一套系统的安全评测框架，涵盖了仇恨言论、偏见歧视言论、犯罪违法、隐私、伦理道德等八大类别，包括细粒度划分的40余个二级安全类别。

[[官方网站](http://coai.cs.tsinghua.edu.cn/leaderboard/)]   [[Github](https://github.com/thu-coai/Safety-Prompts)] [[论文](https://arxiv.org/abs/2304.10436)]

### 7. OpenCompass大语言模型评测 

OpenCompass 是一款开源、高效、全面的评测大模型体系及开放平台。我们提供完整开源可复现的评测框架，支持大语言模型、多模态模型各类模型的一站式评测。利用分布式技术，即使面对千亿参数模型也能在数小时内完成评测。基于多个不同维度的高认可度数据集开放多样化的评测方式，包括零样本评测、小样本评测和思维链评测，全方位量化模型各个维度能力。

[[官方网站](https://opencompass.org.cn/)]   [[Github](https://github.com/open-compass/opencompass)]

<p align="right">[<a href="#top">Back to Top</a>]</p>

## 在线体验大模型

> **注**：需要申请或者注册方可体验,更多见[Github](https://github.com/wgwang/LLMs-In-China)

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

1. 🤗[HuggingFace](https://huggingface.co/): The AI community building the future.
* 模型下载地址: [https://huggingface.co/models](https://huggingface.co/models)

2. [ModelScope](https://modelscope.cn/home): ModelScope平台是以模型为中心的模型开源社区
* 模型下载地址:[https://modelscope.cn/models](https://modelscope.cn/models)

3. [flagopen](https://flagopen.baai.ac.cn/#/home): flagopen飞智大模型技术开源体系
* 模型下载地址: [https://model.baai.ac.cn/models](https://model.baai.ac.cn/models)

4. [始智AI](https://wisemodel.cn/home): 中国AI开源创新社区
* 模型下载地址: [https://wisemodel.cn/models](https://wisemodel.cn/models)

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

## Other-Awesome

| 序号 | 名称 | 说明 | 作者/组织 | Stars | 地址 |
| :---: | :--- | :--- | :--- | :--- | :--- |
| 1 | Awesome-Chatgpt | ChatGPT资源、工具、应用和用法 | awesome-chatgpt | ![GitHub stars](https://img.shields.io/github/stars/awesome-chatgpt/awesome-chatgpt?style=flat-square) | [GitHub](https://github.com/awesome-chatgpt/awesome-chatgpt) |
| 2 | Awesome-ChatGPT-Prompts | ChatGPT模型Prompts示例集 | f | ![GitHub stars](https://img.shields.io/github/stars/f/awesome-chatgpt-prompts?style=flat-square) | [GitHub](https://github.com/f/awesome-chatgpt-prompts) |
| 3 | Awesome-LLM | 大型语言模型相关资料精选列表 | Hannibal046 | ![GitHub stars](https://img.shields.io/github/stars/Hannibal046/Awesome-LLM?style=flat-square) | [GitHub](https://github.com/Hannibal046/Awesome-LLM) |
| 4 | Awesome-LangChain | LangChain相关应用列表 | kyrolabs | ![GitHub stars](https://img.shields.io/github/stars/kyrolabs/awesome-langchain?style=flat-square) | [GitHub](https://github.com/kyrolabs/awesome-langchain) |
| 5 | Awesome-Open-Gpt | GPT开源精选项目合集（170+）| EwingYangs | ![GitHub stars](https://img.shields.io/github/stars/EwingYangs/awesome-open-gpt?style=flat-square) | [GitHub](https://github.com/EwingYangs/awesome-open-gpt) |
| 6 | Awesome-Multimodal-LLMs | 多模态大语言模型（MLLM）精选列表 | BradyFU | ![GitHub stars](https://img.shields.io/github/stars/BradyFU/Awesome-Multimodal-Large-Language-Models?style=flat-square) | [GitHub](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models) |
| 7 | Awesome-Transformer-Attention | Vision Transformer & Attention论文列表 | cmhungsteve | ![GitHub stars](https://img.shields.io/github/stars/cmhungsteve/Awesome-Transformer-Attention?style=flat-square) | [GitHub](https://github.com/cmhungsteve/Awesome-Transformer-Attention) |
| 8 | Awesome-Prompt-Engineering | Prompt Engineering精选资源 | promptslab | ![GitHub stars](https://img.shields.io/github/stars/promptslab/Awesome-Prompt-Engineering?style=flat-square) | [GitHub](https://github.com/promptslab/Awesome-Prompt-Engineering) |
| 9 | Awesome-AITools | AI相关实用工具整理 | ikaijua | ![GitHub stars](https://img.shields.io/github/stars/ikaijua/Awesome-AITools?style=flat-square) | [GitHub](https://github.com/ikaijua/Awesome-AITools) |
| 10 | Awesome-Chinese-LLM | 中文LLM开源模型、应用、数据集及教程 | HqWu-HITCS | ![GitHub stars](https://img.shields.io/github/stars/HqWu-HITCS/Awesome-Chinese-LLM?style=flat-square) | [GitHub](https://github.com/HqWu-HITCS/Awesome-Chinese-LLM) |
| 11 | Awesome-LLM4Tool | 大语言模型工具相关论文和资源 | OpenGVLab | ![GitHub stars](https://img.shields.io/github/stars/OpenGVLab/Awesome-LLM4Tool?style=flat-square) | [GitHub](https://github.com/OpenGVLab/Awesome-LLM4Tool) |
| 12 | Awesome LLM Security | LLM安全相关工具、文档和项目 | corca-ai | ![GitHub stars](https://img.shields.io/github/stars/corca-ai/awesome-llm-security?style=flat-square) | [GitHub](https://github.com/corca-ai/awesome-llm-security) |
| 13 | Awesome AI Agents | AI Agent开源和闭源项目列表 | e2b-dev | ![GitHub stars](https://img.shields.io/github/stars/e2b-dev/awesome-ai-agents?style=flat-square) | [GitHub](https://github.com/e2b-dev/awesome-ai-agents) |
| 14 | Awesome-LLM-Notes | LLM相关笔记 | kyaiooiayk | ![GitHub stars](https://img.shields.io/github/stars/kyaiooiayk/Awesome-LLM-Large-Language-Models-Notes?style=flat-square) | [GitHub](https://github.com/kyaiooiayk/Awesome-LLM-Large-Language-Models-Notes) |
| 15 | Awesome-Efficient-LLM | 高效大语言模型精选列表 | horseee | ![GitHub stars](https://img.shields.io/github/stars/horseee/Awesome-Efficient-LLM?style=flat-square) | [GitHub](https://github.com/horseee/Awesome-Efficient-LLM) |
| 16 | Awesome Datasets for LLM | LLM训练数据集精选 | Zjh-819 | ![GitHub stars](https://img.shields.io/github/stars/Zjh-819/LLMDataHub?style=flat-square) | [GitHub](https://github.com/Zjh-819/LLMDataHub) |
| 17 | Awesome-Align-LLM-Human | LLMs与人类对齐的论文和资源 | GaryYufei | ![GitHub stars](https://img.shields.io/github/stars/GaryYufei/AlignLLMHumanSurvey?style=flat-square) | [GitHub](https://github.com/GaryYufei/AlignLLMHumanSurvey) |
| 18 | Awesome RLHF | 强化学习与人类反馈（RLHF）论文 | opendilab | ![GitHub stars](https://img.shields.io/github/stars/opendilab/awesome-RLHF?style=flat-square) | [GitHub](https://github.com/opendilab/awesome-RLHF) |
| 19 | Prompt-in-context-learning | Prompt上下文学习工程指南 | EgoAlpha | ![GitHub stars](https://img.shields.io/github/stars/EgoAlpha/prompt-in-context-learning?style=flat-square) | [GitHub](https://github.com/EgoAlpha/prompt-in-context-learning) |
| 20 | Awesome Instruction Learning | 指令学习论文和数据集阅读列表 | RenzeLou | ![GitHub stars](https://img.shields.io/github/stars/RenzeLou/awesome-instruction-learning?style=flat-square) | [GitHub](https://github.com/RenzeLou/awesome-instruction-learning) |
| 21 | Awesome-Foundation-Models | 视觉和语言任务基础模型列表 | uncbiag | ![GitHub stars](https://img.shields.io/github/stars/uncbiag/Awesome-Foundation-Models?style=flat-square) | [GitHub](https://github.com/uncbiag/Awesome-Foundation-Models) |
| 22 | Awesome-AI-Devtools | AI驱动的开发者工具列表 | jamesmurdza | ![GitHub stars](https://img.shields.io/github/stars/jamesmurdza/awesome-ai-devtools?style=flat-square) | [GitHub](https://github.com/jamesmurdza/awesome-ai-devtools) |
| 23 | Awesome-Autonomous-GPT | 自主AI Agent相关项目资源 | ScarletPan | ![GitHub stars](https://img.shields.io/github/stars/ScarletPan/awesome-autonomous-gpt?style=flat-square) | [GitHub](https://github.com/ScarletPan/awesome-autonomous-gpt) |
| 24 | Awesome-Papers-Autonomous-Agent | 自主Agent相关论文集 | lafmdp | ![GitHub stars](https://img.shields.io/github/stars/lafmdp/Awesome-Papers-Autonomous-Agent?style=flat-square) | [GitHub](https://github.com/lafmdp/Awesome-Papers-Autonomous-Agent) |
| 25 | Awesome-Code-LLM | 代码LLM综合研究 | codefuse-ai | ![GitHub stars](https://img.shields.io/github/stars/codefuse-ai/Awesome-Code-LLM?style=flat-square) | [GitHub](https://github.com/codefuse-ai/Awesome-Code-LLM) |
| 26 | Awesome-LLM-Compression | LLM压缩研究论文和工具 | HuangOwen | ![GitHub stars](https://img.shields.io/github/stars/HuangOwen/Awesome-LLM-Compression?style=flat-square) | [GitHub](https://github.com/HuangOwen/Awesome-LLM-Compression) |
| 27 | Autonomous-Agents | 自主Agent（LLMs）| tmgthb | ![GitHub stars](https://img.shields.io/github/stars/tmgthb/Autonomous-Agents?style=flat-square) | [GitHub](https://github.com/tmgthb/Autonomous-Agents) |
| 28 | Awesome-Large-Multimodal-Agents | 大型多模态Agent | jun0wanan | ![GitHub stars](https://img.shields.io/github/stars/jun0wanan/awesome-large-multimodal-agents?style=flat-square) | [GitHub](https://github.com/jun0wanan/awesome-large-multimodal-agents) |
| 29 | Awesome-LLM-Prompt-Optimization | LLM提示调优和自动优化论文 | jxzhangjhu | ![GitHub stars](https://img.shields.io/github/stars/jxzhangjhu/Awesome-LLM-Prompt-Optimization?style=flat-square) | [GitHub](https://github.com/jxzhangjhu/Awesome-LLM-Prompt-Optimization) |
| 30 | Awesome-LLMs-Datasets | LLMs文本数据集大列表 | lmmlzn | ![GitHub stars](https://img.shields.io/github/stars/lmmlzn/Awesome-LLMs-Datasets?style=flat-square) | [GitHub](https://github.com/lmmlzn/Awesome-LLMs-Datasets) |
| 31 | Awesome-RAG-Survey | RAG相关论文分类收集 | hymie122 | ![GitHub stars](https://img.shields.io/github/stars/hymie122/RAG-Survey?style=flat-square) | [GitHub](https://github.com/hymie122/RAG-Survey) |
| 32 | Awesome-Tool-LLM | 工具增强的语言模型论文 | zorazrw | ![GitHub stars](https://img.shields.io/github/stars/zorazrw/awesome-tool-llm?style=flat-square) | [GitHub](https://github.com/zorazrw/awesome-tool-llm) |
| 33 | LLM-Tool-Survey | 工具学习与LLMs相关论文 | quchangle1 | ![GitHub stars](https://img.shields.io/github/stars/quchangle1/LLM-Tool-Survey?style=flat-square) | [GitHub](https://github.com/quchangle1/LLM-Tool-Survey) |
| 34 | Awesome-Foundation-Model-Leaderboards | 基础模型排行榜和开发工具 | SAILResearch | ![GitHub stars](https://img.shields.io/github/stars/SAILResearch/awesome-foundation-model-leaderboards?style=flat-square) | [GitHub](https://github.com/SAILResearch/awesome-foundation-model-leaderboards) |
| 35 | Awesome-LLM-KV-Cache | LLM KV Cache论文和代码精选 | Zefan-Cai | ![GitHub stars](https://img.shields.io/github/stars/Zefan-Cai/Awesome-LLM-KV-Cache?style=flat-square) | [GitHub](https://github.com/Zefan-Cai/Awesome-LLM-KV-Cache) |
| 36 | Awesome-LLM-Strawberry | OpenAI Strawberry(o1)和推理论文 | hijkzzz | ![GitHub stars](https://img.shields.io/github/stars/hijkzzz/Awesome-LLM-Strawberry?style=flat-square) | [GitHub](https://github.com/hijkzzz/Awesome-LLM-Strawberry) |
| 37 | Awesome-LLM-Resourses | 全世界最好的LLM资料总结 | WangRongsheng | ![GitHub stars](https://img.shields.io/github/stars/WangRongsheng/awesome-LLM-resourses?style=flat-square) | [GitHub](https://github.com/WangRongsheng/awesome-LLM-resourses) |
| 38 | Awesome-LLM-Reasoning-Openai-o1-Survey | OpenAI o1相关工作和技术背景 | wjn1996 | ![GitHub stars](https://img.shields.io/github/stars/wjn1996/Awesome-LLM-Reasoning-Openai-o1-Survey?style=flat-square) | [GitHub](https://github.com/wjn1996/Awesome-LLM-Reasoning-Openai-o1-Survey) |
| 39 | Awesome-LLM-Reasoning | 解锁LLM和MLLM推理能力的论文资源 | atfortes | ![GitHub stars](https://img.shields.io/github/stars/atfortes/Awesome-LLM-Reasoning?style=flat-square) | [GitHub](https://github.com/atfortes/Awesome-LLM-Reasoning) |
| 40 | Awesome-Computer-Use-Agents | 计算机使用Agent论文和博客 | ranpox | ![GitHub stars](https://img.shields.io/github/stars/ranpox/awesome-computer-use?style=flat-square) | [GitHub](https://github.com/ranpox/awesome-computer-use) |
| 41 | LLM_MultiAgents_Survey_Papers | LLM多智能体调研论文 | taichengguo | ![GitHub stars](https://img.shields.io/github/stars/taichengguo/LLM_MultiAgents_Survey_Papers?style=flat-square) | [GitHub](https://github.com/taichengguo/LLM_MultiAgents_Survey_Papers) |
| 42 | Awesome_Think_With_Images | 让LVLMs用图像思考的研究 | zhaochen0110 | ![GitHub stars](https://img.shields.io/github/stars/zhaochen0110/Awesome_Think_With_Images?style=flat-square) | [GitHub](https://github.com/zhaochen0110/Awesome_Think_With_Images) |
| 43 | Awesome Label-free RL Papers | 无标签强化学习论文 | QingyangZhang | ![GitHub stars](https://img.shields.io/github/stars/QingyangZhang/Label-Free-RLVR?style=flat-square) | [GitHub](https://github.com/QingyangZhang/Label-Free-RLVR) |
| 44 | Awesome-AI-Agent-Papers | AI智能体研究论文集合 | masamasa59 | ![GitHub stars](https://img.shields.io/github/stars/masamasa59/ai-agent-papers?style=flat-square) | [GitHub](https://github.com/masamasa59/ai-agent-papers) |
| 45 | Awesome-Large-Search-Models | 搜索导向型大语言模型研究 | Wu-Zongyu | ![GitHub stars](https://img.shields.io/github/stars/Wu-Zongyu/Awesome-Large-Search-Models?style=flat-square) | [GitHub](https://github.com/Wu-Zongyu/Awesome-Large-Search-Models) |
| 46 | Awesome-Deep-Research | Agent深度研究资源 | DavidZWZ | ![GitHub stars](https://img.shields.io/github/stars/DavidZWZ/Awesome-Deep-Research?style=flat-square) | [GitHub](https://github.com/DavidZWZ/Awesome-Deep-Research) |
| 47 | Reading-List-of-LLM-Based-Data-Science-Agent | LLM数据科学Agent阅读列表 | Stephen-SMJ | ![GitHub stars](https://img.shields.io/github/stars/Stephen-SMJ/Reading-List-of-LLM-Based-Data-Science-Agent?style=flat-square) | [GitHub](https://github.com/Stephen-SMJ/Reading-List-of-LLM-Based-Data-Science-Agent) |
| 48 | Awesome-Agents | 开源AI Agent工具和产品 | kyrolabs | ![GitHub stars](https://img.shields.io/github/stars/kyrolabs/awesome-agents?style=flat-square) | [GitHub](https://github.com/kyrolabs/awesome-agents) |
| 49 | Awesome-OpenClaw-Skills | OpenClaw社区构建的技能 | VoltAgent | ![GitHub stars](https://img.shields.io/github/stars/VoltAgent/awesome-openclaw-skills?style=flat-square) | [GitHub](https://github.com/VoltAgent/awesome-openclaw-skills) |
| 50 | Awesome-Claude-Code | Claude Code相关技能和工具 | hesreallyhim | ![GitHub stars](https://img.shields.io/github/stars/hesreallyhim/awesome-claude-code?style=flat-square) | [GitHub](https://github.com/hesreallyhim/awesome-claude-code) |
| 51 | Awesome-Claude-Skills | Claude技能、资源和工具 | ComposioHQ | ![GitHub stars](https://img.shields.io/github/stars/ComposioHQ/awesome-claude-skills?style=flat-square) | [GitHub](https://github.com/ComposioHQ/awesome-claude-skills) |

<p align="right">[<a href="#top">Back to Top</a>]</p>


## NLU系列


<p align="right">[<a href="#top">Back to Top</a>]</p>


## NLU系列

### BERT

+ 2018 | BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding | Jacob Devlin, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1810.04805)
+ 2019 | Pre-Training with Whole Word Masking for Chinese BERT | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1906.08101)

| 模型            | 版本  | TensorFlow                                                   | PyTorch                                                      | 作者                                                  | 源地址                                                       | 应用领域     |
| --------------- | ----- | ------------------------------------------------------------ | ------------------------------------------------------------ | ----------------------------------------------------- | ------------------------------------------------------------ | ------------ |
| BERT-Base | base | [Google Drive](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip) | - | Google Research | [GitHub](https://github.com/google-research/bert) | 通用 |
| BERT-wwm | base | [Google Drive](https://drive.google.com/open?id=1RoTQsXp2hkQ1gSRVylRIJfQxJUgkfJMW) · [讯飞云](http://pan.iflytek.com/#/link/A2483AD206EF85FD91569B498A3C3879) | [Google Drive](https://drive.google.com/open?id=1AQitrjbvCWc51SYiLN-cJq4e0WiNN4KY) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| BERT-wwm-ext | base | [Google Drive](https://drive.google.com/open?id=1buMLEjdtrXE2c4G1rpsNGWEx7lUQ0RHi) · [讯飞云](http://pan.iflytek.com/#/link/653637473FFF242C3869D77026C9BDB5) | [Google Drive](https://drive.google.com/open?id=1iNeYFhCBJWeUsIlnW_2K6SMwXkM4gLb_) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| bert-base-民事 | base | [阿里云](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/ms.zip) | - | THUNLP | [GitHub](https://github.com/thunlp/OpenCLaP) | 司法 |
| bert-base-刑事 | base | [阿里云](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/xs.zip) | - | THUNLP | [GitHub](https://github.com/thunlp/OpenCLaP) | 司法 |
| BAAI-JDAI-BERT | base | [京东云](https://jdai009.s3.cn-north-1.jdcloud-oss.com/jd-aig/open/models/nlp_baai/20190918/JDAI-BERT.tar.gz) | - | JDAI | [GitHub](https://github.com/jd-aig/nlp_baai) | 电商客服对话 |
| FinBERT | base | [Google Drive](https://drive.google.com/file/d/193B4sT63mMeh4zfge0FJbbFY447KiJXp/view?usp=sharing) · [百度网盘](https://pan.baidu.com/share/init?surl=D-pVJyW6bbJSre5RxotJkA) | [Google Drive](https://drive.google.com/file/d/1qW1YWtw3q9Q28QThrIY-rDU9Gl-SLIKO/view?usp=sharing) · [百度网盘](https://pan.baidu.com/share/init?surl=y_O586GBmZZ7g4d2nOF0Vg) | Value Simplex | [GitHub](https://github.com/valuesimplex/FinBERT) | 金融科技领域 |
| EduBERT | base | [好未来AI](https://ai.100tal.com/download/TAL-EduBERT-TF.zip) | [好未来AI](https://ai.100tal.com/download/TAL-EduBERT.zip) | tal-tech | [GitHub](https://github.com/tal-tech/edu-bert) | 教育领域 |
| guwenbert-base | base | - | [百度网盘](https://pan.baidu.com/s/1dw_08p7CVsz0jVj4jd58lQ) · [🤗HF](https://huggingface.co/ethanyt/guwenbert-base) | Ethan | [GitHub](https://github.com/Ethan-yt/guwenbert) | 古文领域 |
| guwenbert-large | large | - | [百度网盘](https://pan.baidu.com/s/1TL9mBIlIv2rSvp61xCkeJQ) · [🤗HF](https://huggingface.co/ethanyt/guwenbert-large) | Ethan | [GitHub](https://github.com/Ethan-yt/guwenbert) | 古文领域 |
| BERT-CCPoem | small | - | [thunlp](https://thunlp.oss-cn-qingdao.aliyuncs.com/BERT_CCPoem_v1.zip) | THUNLP-AIPoet | [GitHub](https://github.com/THUNLP-AIPoet/BERT-CCPoem) | 古典诗歌 |

备注: 

> wwm全称为**Whole Word Masking **,一个完整的词的部分WordPiece子词被mask，则同属该词的其他部分也会被mask

> ext表示在更多数据集下训练

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ChineseBERT

+ 2021 | ChineseBERT: Chinese Pretraining Enhanced by Glyph and Pinyin Information | Zijun Sun, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2106.16038.pdf)

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| ChineseBERT | base | - | [🤗HF](https://huggingface.co/ShannonAI/ChineseBERT-base) | ShannonAI | [GitHub](https://github.com/ShannonAI/ChineseBert) | 通用 |
| ChineseBERT | large | - | [🤗HF](https://huggingface.co/ShannonAI/ChineseBERT-large) | ShannonAI | [GitHub](https://github.com/ShannonAI/ChineseBert) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RoBERTa

+ 2019 | RoBERTa: A Robustly Optimized BERT Pretraining Approach | Yinhan Liu, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1907.11692.pdf)

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| RoBERTa-tiny-clue | tiny | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny-clue.zip) | [百度网盘](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | CLUE | [GitHub](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用 |
| RoBERTa-tiny-pair | tiny | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny-pair.zip) | [百度网盘](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | CLUE | [GitHub](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用 |
| RoBERTa-tiny3L768-clue | tiny | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny3L768-clue.zip) | - | CLUE | [GitHub](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用 |
| RoBERTa-tiny3L312-clue | tiny | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-tiny3L312-clue.zip) | [百度网盘](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | CLUE | [GitHub](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用 |
| RoBERTa-large-pair | large | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-large-pair.zip) | [百度网盘](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | CLUE | [GitHub](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用 |
| RoBERTa-large-clue | large | [Google Drive](https://storage.googleapis.com/cluebenchmark/pretrained_models/RoBERTa-large-clue.zip) | [百度网盘](https://pan.baidu.com/share/init?surl=hoR01GbhcmnDhZxVodeO4w) | CLUE | [GitHub](https://github.com/CLUEbenchmark/CLUEPretrainedModels) | 通用 |
| RBT3 | 3层base | [Google Drive](https://drive.google.com/file/d/1-rvV0nBDvRCASbRz8M9Decc3_8Aw-2yi/view?usp=drive_open) · [讯飞云](https://pan.iflytek.com/link/275E5B46185C982D4AF5AC295E1651B6) | [Google Drive](https://drive.google.com/file/d/1_LqmIxm8Nz1Abvlqb8QFZaxYo-TInOed/view) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| RBTL3 | 3层large | [Google Drive](https://drive.google.com/open?id=1Jzn1hYwmv0kXkfTeIvNT61Rn1IbRc-o8) · [讯飞云](https://pan.iflytek.com/link/0DD18FAC080BAF75DBA28FB5C0047760) | [Google Drive](https://drive.google.com/open?id=1eHM3l4fMo6DsQYGmey7UZGiTmQquHw25) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| RBTL4 | 4层large | [讯飞云](http://pan.iflytek.com/link/7B04C5BF09812DB241BBA973D649824C) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| RBTL6 | 6层large | [讯飞云](http://pan.iflytek.com/link/B935B1F701A8FD352CAA74614126C4A2) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| RoBERTa-wwm-ext | base | [Google Drive](https://drive.google.com/open?id=1jMAKIJmPn7kADgD3yQZhpsqM-IRM1qZt) · [讯飞云](http://pan.iflytek.com/#/link/98D11FAAF0F0DBCB094EE19CCDBC98BF) | [Google Drive](https://drive.google.com/open?id=1eHM3l4fMo6DsQYGmey7UZGiTmQquHw25) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| RoBERTa-wwm-ext-large | large | [Google Drive](https://drive.google.com/open?id=1dtad0FFzG11CBsawu8hvwwzU2R0FDI94) · [讯飞云](http://pan.iflytek.com/#/link/AC056611607108F33A744A0F56D0F6BE) | [Google Drive](https://drive.google.com/open?id=1-2vEZfIFCdM1-vJ3GD6DlSyKT4eVXMKq) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-BERT-wwm) | 通用 |
| RoBERTa-base | base | [Google Drive](https://drive.google.com/open?id=1ykENKV7dIFAqRRQbZIh0mSb7Vjc2MeFA) · [百度网盘](https://pan.baidu.com/s/1hAs7-VSn5HZWxBHQMHKkrg) | [Google Drive](https://drive.google.com/open?id=1H6f4tYlGXgug1DdhYzQVBuwIGAkAflwB) · [百度网盘](https://pan.baidu.com/s/1AGC76N7pZOzWuo8ua1AZfw) | brightmart | [GitHub](https://github.com/brightmart/roberta_zh) | 通用 |
| RoBERTa-Large | large | [Google Drive](https://drive.google.com/open?id=1W3WgPJWGVKlU9wpUYsdZuurAIFKvrl_Y) · [百度网盘](https://pan.baidu.com/s/1Rk_QWqd7-wBTwycr91bmug) | [Google Drive](https://drive.google.com/open?id=1yK_P8VhWZtdgzaG0gJ3zUGOKWODitKXZ) | brightmart | [GitHub](https://github.com/brightmart/roberta_zh) | 通用 |
| RoBERTa-tiny | tiny | [🤗HF](https://huggingface.co/uer) | [🤗HF](https://huggingface.co/uer) | DBIIR @ RUC | [GitHub](https://github.com/dbiir/UER-py) | 通用 |
| RoBERTa-mini | mini | [🤗HF](https://huggingface.co/uer) | [🤗HF](https://huggingface.co/uer) | DBIIR @ RUC | [GitHub](https://github.com/dbiir/UER-py) | 通用 |
| RoBERTa-small | small | [🤗HF](https://huggingface.co/uer) | [🤗HF](https://huggingface.co/uer) | DBIIR @ RUC | [GitHub](https://github.com/dbiir/UER-py) | 通用 |
| RoBERTa-medium | medium | [🤗HF](https://huggingface.co/uer) | [🤗HF](https://huggingface.co/uer) | DBIIR @ RUC | [GitHub](https://github.com/dbiir/UER-py) | 通用 |
| RoBERTa-base | base | [🤗HF](https://huggingface.co/uer) | [🤗HF](https://huggingface.co/uer) | DBIIR @ RUC | [GitHub](https://github.com/dbiir/UER-py) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ALBERT

+ 2019 | ALBERT: A Lite BERT For Self-Supervised Learning Of Language Representations | Zhenzhong Lan, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1909.11942.pdf)

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| Albert-tiny | tiny | [Google Drive](https://storage.googleapis.com/albert_zh/albert_tiny_489k.zip) | [Google Drive](https://drive.google.com/open?id=1VBsUJ7R5eWF1VcUBQY6BEn1a9miEvlBr) | brightmart | [GitHub](https://github.com/brightmart/albert_zh) | 通用 |
| Albert-base | base | [Google Drive](https://storage.googleapis.com/albert_zh/albert_base_zh_additional_36k_steps.zip) | [Google Drive](https://drive.google.com/open?id=1HeijHGubWR-ElFnfxUf8IrRx7Ghm1S_Q) | brightmart | [GitHub](https://github.com/brightmart/albert_zh) | 通用 |
| Albert-large | large | [Google Drive](https://storage.googleapis.com/albert_zh/albert_large_zh.zip) | [Google Drive](https://drive.google.com/open?id=1TAuv7OiFN8qbkT6S_VbfVbhkhg2GUF3q) | brightmart | [GitHub](https://github.com/brightmart/albert_zh) | 通用 |
| Albert-xlarge | xlarge | [Google Drive](https://storage.googleapis.com/albert_zh/albert_xlarge_zh_183k.zip) | [Google Drive](https://drive.google.com/open?id=1kMhogQRX0uGWIGdNhm7-3hsmHlrzY_gp) | brightmart | [GitHub](https://github.com/brightmart/albert_zh) | 通用 |
| Albert-base | base | [Google Drive](https://storage.googleapis.com/albert_models/albert_base_zh.tar.gz) | - | Google Research | [GitHub](https://github.com/google-research/ALBERT) | 通用 |
| Albert-large | large | [Google Drive](https://storage.googleapis.com/albert_models/albert_large_zh.tar.gz) | - | Google Research | [GitHub](https://github.com/google-research/ALBERT) | 通用 |
| Albert-xlarge | xlarge | [Google Drive](https://storage.googleapis.com/albert_models/albert_xlarge_zh.tar.gz) | - | Google Research | [GitHub](https://github.com/google-research/ALBERT) | 通用 |
| Albert-xxlarge | xxlarge | [Google Drive](https://storage.googleapis.com/albert_models/albert_xxlarge_zh.tar.gz) | - | Google Research | [GitHub](https://github.com/google-research/ALBERT) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### NEZHA

+ 2019 | NEZHA: Neural Contextualized Representation for Chinese Language Understanding | Junqiu Wei, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1909.00204)

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| NEZHA-base | base | [Google Drive](https://drive.google.com/drive/folders/1tFs-wMoXIY8zganI2hQgDBoDPqA8pSmh?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1UVQjy9v_Sv4cQd1ELdjqww) | [GitHub](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | HUAWEI | [GitHub](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用 |
| NEZHA-base-wwm | base | [Google Drive](https://drive.google.com/drive/folders/1bK6WbqAG-B6BX2d9RPprnh2MPK6zL0t_?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1-YG8e5V2zKCnR3azsGZT1w) | [GitHub](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | HUAWEI | [GitHub](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用 |
| NEZHA-large | large | [Google Drive](https://drive.google.com/drive/folders/1ZPPM5XtTTOrS_CDRak1t2nCBU-LFZ_zs?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1R1Ew-Lu8oIP6QhWO6nqp5Q) | [GitHub](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | HUAWEI | [GitHub](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用 |
| NEZHA-large-wwm | large | [Google Drive](https://drive.google.com/drive/folders/1LOAUc9LXyogC2gmP_q1ojqj41Ez01aga?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1JK1RLIJd2wpuypku3stt8w) | [GitHub](https://github.com/lonePatient/NeZha_Chinese_PyTorch) | HUAWEI | [GitHub](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用 |
| WoNEZHA (word-base) | base | [百度网盘](https://pan.baidu.com/s/1ABKwUuIiMEEsRXxxlbyKmw) | - | ZhuiyiTechnology | [GitHub](https://github.com/ZhuiyiTechnology/WoBERT) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### MacBERT

+ 2020 | Revisiting Pre-Trained Models for Chinese Natural Language Processing | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2004.13922.pdf)

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| MacBERT-base | base | [Google Drive](https://drive.google.com/file/d/1aV69OhYzIwj_hn-kO1RiBa-m8QAusQ5b/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/CF2A1F9AEBF859650E8956854A994C1B) | - | Yiming Cui | [GitHub](https://github.com/ymcui/MacBERT) | 通用 |
| MacBERT-large | large | [Google Drive](https://drive.google.com/file/d/1lWYxnk1EqTA2Q20_IShxBrCPc5VSDCkT/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/805D743F3826EC4F4EB5C774D34432AE) | - | Yiming Cui | [GitHub](https://github.com/ymcui/MacBERT) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### WoBERT

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| WoBERT | base | [百度网盘](https://pan.baidu.com/s/1BrdFSx9_n1q2uWBiQrpalw) | - | ZhuiyiTechnology | [GitHub](https://github.com/ZhuiyiTechnology/WoBERT) | 通用 |
| WoBERT-plus | base | [百度网盘](https://pan.baidu.com/s/1Ltq3ltQsyBCj56zoOOvI9A) | - | ZhuiyiTechnology | [GitHub](https://github.com/ZhuiyiTechnology/WoBERT) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### XLNET

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| XLNet-base | base | [Google Drive](https://drive.google.com/open?id=1m9t-a4gKimbkP5rqGXXsEAEPhJSZ8tvx) · [讯飞云](http://pan.iflytek.com/#/link/32619C31BDEFAF2D82CB8C7F66F01D5C) | [Google Drive](https://drive.google.com/open?id=1mPDgcMfpqAf2wk9Nl8OaMj654pYrWXaR) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-XLNet) | 通用 |
| XLNet-mid | middle | [Google Drive](https://drive.google.com/open?id=1342uBc7ZmQwV6Hm6eUIN_OnBSz1LcvfA) · [讯飞云](http://pan.iflytek.com/#/link/ED7DF7ED04B871AFE8E4D97704B9134D) | [Google Drive](https://drive.google.com/open?id=1u-UmsJGy5wkXgbNK4w9uRnC0RxHLXhxy) | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-XLNet) | 通用 |
| XLNet-zh-Large | large | [百度网盘](https://pan.baidu.com/s/1dy0Z27DoZdMpSmoz1Q4G5A) | - | brightmart | [GitHub](https://github.com/brightmart/xlnet_zh) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ELECTRA

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| ELECTRA-180g-large | large | [Google Drive](https://drive.google.com/file/d/1P9yAuW0-HR7WvZ2r2weTnx3slo6f5u9q/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/7605874F5A11CD693C60EAB79005CCF3) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 通用 |
| ELECTRA-180g-small-ex | small | [Google Drive](https://drive.google.com/file/d/1NYJTKH1dWzrIBi86VSUK-Ml9Dsso_kuf/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/3EFCF909FC5CFEA6F0EA7AA774C64CF0) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 通用 |
| ELECTRA-180g-base | base | [Google Drive](https://drive.google.com/file/d/1RlmfBgyEwKVBFagafYvJgyCGuj7cTHfh/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/38E14C9BDBE8E93F09DFE2198E308489) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 通用 |
| ELECTRA-180g-small | small | [Google Drive](https://drive.google.com/file/d/177EVNTQpH2BRW-35-0LNLjV86MuDnEmu/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/D1B8FE678FA5BC31AA43BD99AD09913E) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 通用 |
| legal-ELECTRA-large | large | [Google Drive](https://drive.google.com/file/d/1jPyVi_t4QmTkFy7PD-m-hG-lQ8cIETzD/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |
| legal-ELECTRA-base | base | [Google Drive](https://drive.google.com/file/d/12ZLaoFgpqGJxSi_9KiQV-jdVN4XRGMiD/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |
| legal-ELECTRA-small | small | [Google Drive](https://drive.google.com/file/d/1arQ5qNTNoc1OyMH8wBUKdTMy2QponIFY/view?usp=sharing) · [讯飞云](http://pan.iflytek.com/#/link/CC111ED9B1D4AE7E26C69A520A6D8759) | - | Yiming Cui | [GitHub](https://github.com/ymcui/Chinese-ELECTRA) | 司法领域 |
| ELECTRA-tiny | tiny | [Google Drive](https://drive.google.com/file/d/1UP4byt4-kgenwST0KvyMYNbln6FfaSLp/view?usp=sharing) · [百度网盘](https://pan.baidu.com/share/init?surl=4b-IiCkjRg-6XIYPXnezZA) | - | CLUE | [GitHub](https://github.com/CLUEbenchmark/ELECTRA) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ZEN

+ 2019 | ZEN: Pre-training Chinese Text Encoder Enhanced by N-gram Representations | Shizhe Diao, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/1911.00720.pdf)
+ 2021 | ZEN 2.0: Continue Training and Adaption for N-gram Enhanced Text Encoders | Yan Song, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2105.01279.pdf)

| 模型            | 版本  | TensorFlow | PyTorch                                                      | 作者                                                         | 源地址                                                 | 应用领域 |
| --------------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------ | -------- |
| ZEN-Base        | base  |            | <p>[Google Drive](https://drive.google.com/open?id=1oxNdYMQOpFe3QlttH98bAqg_FQiiVeMr)<br>[百度网盘](https://pan.baidu.com/s/1E2ylFnzGSkwBc8tY_OqZYg)</p> | [Sinovation Ventures AI Institute](https://github.com/sinovation) | [github](https://github.com/sinovation/ZEN)            | 通用     |
| Erlangshen-ZEN2 | large |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Erlangshen-ZEN2-668M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL)                    | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |

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
| ernie-3.0-base   | 12-layer, 768-hidden, 12-heads | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_base_zh.pdparams) | [[🤗HF\]](https://huggingface.co/nghuyong/ernie-3.0-base-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-medium | 6-layer, 768-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_medium_zh.pdparams) | [[🤗HF\]](https://huggingface.co/nghuyong/ernie-3.0-medium-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-mini   | 6-layer, 384-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_mini_zh.pdparams) | [[🤗HF\]](https://huggingface.co/nghuyong/ernie-3.0-mini-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-micro  | 4-layer, 384-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_micro_zh.pdparams) | [[🤗HF\]](https://huggingface.co/nghuyong/ernie-3.0-micro-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |
| ernie-3.0-nano   | 4-layer, 312-hidden, 12-heads  | [link](https://bj.bcebos.com/paddlenlp/models/transformers/ernie_3.0/ernie_3.0_nano_zh.pdparams) | [[🤗HF\]](https://huggingface.co/nghuyong/ernie-3.0-nano-zh) | [PaddlePaddle](https://github.com/PaddlePaddle) | [github](https://github.com/PaddlePaddle/PaddleNLP/tree/develop/model_zoo/ernie-3.0) | 通用     |

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
| Mengzi-BERT     | base(L12) |            | [[🤗HF\]](https://huggingface.co/Langboat/mengzi-bert-base) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 通用     |
| Mengzi-BERT-fin | base(L12) |            | [[🤗HF\]](https://huggingface.co/Langboat/mengzi-bert-base-fin) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 金融财经 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Bloom

+ 2022 | Bloom: BigScience Large Open-science Open-access Multilingual Language Model | huggingface bigscience | - | [`BLOG`](https://bigscience.huggingface.co/blog/bloom)

| 模型         | 版本    | TensorFlow | PyTorch                                                     | 作者                                        | 源地址                                                | 应用领域 |
| ------------ | ------- | ---------- | ----------------------------------------------------------- | ------------------------------------------- | ----------------------------------------------------- | -------- |
| bloom-6b4-zh | 6B(L30) |            | [[🤗HF\]](https://huggingface.co/Langboat/bloom-6b4-zh) | [Langboat](https://huggingface.co/Langboat) | [github](https://github.com/huggingface/transformers) | 通用     |

> 注：作者另有bloom-389m-zh到bloom-2b5-zh等多个中文模型

<p align="right">[<a href="#top">Back to Top</a>]</p>

### TaCL

+ 2021 | TaCL: Improving BERT Pre-training with Token-aware Contrastive Learning | Yixuan Su, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2111.04198.pdf)

| 模型 | 版本      | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                    | 应用领域 |
| ---- | --------- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ----------------------------------------- | -------- |
| TaCL | base(L12) |            | [[🤗HF\]](https://huggingface.co/cambridgeltl/tacl-bert-base-chinese) | [yxuansu](https://github.com/yxuansu) | [github](https://github.com/yxuansu/TaCL) | 通用     |

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
| Erlangshen | large(L24) | bert |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Erlangshen-1.3B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### PERT

+ 2022 | PERT: Pre-Training BERT with Permuted Language Model | Yiming Cui, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2203.06906)

| 模型       | 版本       | TensorFlow                                                   | PyTorch                                                      | 作者                                   | 源地址                                  | 应用领域 |
| ---------- | ---------- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | --------------------------------------- | -------- |
| PERT-base  | base(12L)  | [百度网盘-rcsw](https://pan.baidu.com/s/1yDHkYKmdaJkliTGHWQtdFA?pwd=rcsw) | [[🤗HF\]](https://huggingface.co/hfl/chinese-pert-base)  | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/PERT) | 通用     |
| PERT-large | large(24L) | [百度网盘-e9hs](https://pan.baidu.com/s/1MG44TRIgqV6m_StfB_yBqQ?pwd=e9hs) | [[🤗HF\]](https://huggingface.co/hfl/chinese-pert-large) | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/PERT) | 通用     |

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
| DeBERTa-v2-Large  | large  |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Erlangshen-DeBERTa-v2-320M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |
| DeBERTa-v2-xLarge | xlarge |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Erlangshen-DeBERTa-v2-710M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |
| DeBERTa-v2        | base   |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Erlangshen-DeBERTa-v2-186M-Chinese-SentencePiece) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GlyphBERT

+ 2021 | GlyphCRM: Bidirectional Encoder Representation for Chinese Character with its Glyph | Yuxin li, et al. | arXiv | [`PDF`](https://arxiv.org/pdf/2107.00395.pdf) |

| 模型          | 版本 | TensorFlow | PyTorch                                                 | 作者                                      | 源地址                                           | 应用领域 |
| ------------- | ---- | ---------- | ------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------ | -------- |
| GlyphCRM-base | base |            | [[🤗HF\]](https://huggingface.co/HIT-TMG/GlyphBERT) | [HITsz-TMG](https://github.com/HITsz-TMG) | [github](https://github.com/HITsz-TMG/GlyphBERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CKBERT

+ 2022 | Revisiting and Advancing Chinese Natural Language Understanding with Accelerated Heterogeneous Knowledge Pre-training | Zhang, Taolin, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2210.05287)

| 模型                | 版本  | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                       | 应用领域 |
| ------------------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------- | -------------------------------------------- | -------- |
| pai-ckbert-base-zh  | base  |            | [[🤗HF\]](https://huggingface.co/alibaba-pai/pai-ckbert-base-zh) | [Alibaba](https://github.com/alibaba) | [github](https://huggingface.co/alibaba-pai) | 通用     |
| pai-ckbert-large-zh | large |            | [[🤗HF\]](https://huggingface.co/alibaba-pai/pai-ckbert-large-zh) | [Alibaba](https://github.com/alibaba) | [github](https://huggingface.co/alibaba-pai) | 通用     |
| pai-ckbert-huge-zh  | huge  |            | [[🤗HF\]](https://huggingface.co/alibaba-pai/pai-ckbert-huge-zh) | [Alibaba](https://github.com/alibaba) | [github](https://huggingface.co/alibaba-pai) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### LERT

+ 2022 | LERT: A Linguistically-motivated Pre-trained Language Model | Yiming Cui et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.05344)

| 模型               | 版本 | TensorFlow                                                   | PyTorch                                                      | 作者                                   | 源地址                                  | 应用领域 |
| ------------------ | ---- | ------------------------------------------------------------ | ------------------------------------------------------------ | -------------------------------------- | --------------------------------------- | -------- |
| Chinese-LERT-small | 15m  | [百度网盘-4vuy](https://pan.baidu.com/s/1fBk3em8a5iCMwPLJEBq2pQ?pwd=4vuy) | [[🤗HF\]](https://huggingface.co/hfl/chinese-lert-small) | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/LERT) | 通用     |
| Chinese-LERT-base  | 400m | [百度网盘-9jgi](https://pan.baidu.com/s/1_yb1jCDJ4s2P8OrF_5E_Tg?pwd=9jgi) | [[🤗HF\]](https://huggingface.co/hfl/chinese-lert-base)  | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/LERT) | 通用     |
| Chinese-LERT-large | 1.2G | [百度网盘-s82t](https://pan.baidu.com/s/1pxsS3almc90DPvMXH6BMYQ?pwd=s82t) | [[🤗HF\]](https://huggingface.co/hfl/chinese-lert-large) | [Yiming Cui](https://github.com/ymcui) | [github](https://github.com/ymcui/LERT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RoCBert

+ 2022 | RoCBert: Robust Chinese Bert with Multimodal Contrastive Pretraining | Hui Su et al. | ACL | [`PDF`](https://aclanthology.org/2022.acl-long.65.pdf)

| 模型    | 版本 | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                       | 应用领域 |
| ------- | ---- | ---------- | ------------------------------------------------------------ | --------------------------------------- | -------------------------------------------- | -------- |
| rocbert | base |            | [[🤗HF\]](https://huggingface.co/weiweishi/roc-bert-base-zh) | [Weiwe Shi](https://github.com/sww9370) | [github](https://github.com/sww9370/RoCBert) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### M3E

| 模型      | 版本  | PyTorch                                               | 作者                                      | 源地址                                                       | 备注         |
| --------- | ----- | ----------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------ | ------------ |
| m3e-base  | base  | [m3e-base](https://huggingface.co/moka-ai/m3e-base)   | [Moka-AI](https://huggingface.co/moka-ai) | [uniem](https://github.com/wangyuxinwhy/uniem) | 文本嵌入模型 |
| M3e-small | Small | [m3e-small](https://huggingface.co/moka-ai/m3e-small) | [Moka-AI](https://huggingface.co/moka-ai) | [uniem](https://github.com/wangyuxinwhy/uniem) | 文本嵌入模型 |

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

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| GPT2 | 30亿语料 | - | [Google Drive](https://drive.google.com/file/d/1mT_qCQg4AWnAXTwKfsyyRWCRpgPrBJS3) · [百度网盘](https://pan.baidu.com/s/1yiuTHXUr2DpyBqmFYLJH6A) | Caspar ZHANG | [GitHub](https://github.com/imcaspar/gpt2-ml) | 通用 |
| GPT2 | 15亿语料 | - | [Google Drive](https://drive.google.com/file/d/1IzWpQ6I2IgfV7CldZvFJnZ9byNDZdO4n) · [百度网盘](https://pan.baidu.com/s/1TA_3e-u2bXg_hcx_NwVbGw) | Caspar ZHANG | [GitHub](https://github.com/imcaspar/gpt2-ml) | 通用 |
| CDial-GPT-LCCC-base | base | - | [🤗HF](https://huggingface.co/thu-coai/CDial-GPT_LCCC-base) | thu-coai | [GitHub](https://github.com/thu-coai/CDial-GPT) | 中文对话 |
| CDial-GPT2-LCCC-base | base | - | [🤗HF](https://huggingface.co/thu-coai/CDial-GPT2_LCCC-base) | thu-coai | [GitHub](https://github.com/thu-coai/CDial-GPT) | 中文对话 |
| CDial-GPT-LCCC-large | large | - | [🤗HF](https://huggingface.co/thu-coai/CDial-GPT_LCCC-large) | thu-coai | [GitHub](https://github.com/thu-coai/CDial-GPT) | 中文对话 |
| GPT2-dialogue | base | - | [Google Drive](https://drive.google.com/drive/folders/1Ogz3eapvtvdY4VUcY9AEwMbNRivLKhri?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1qDZ24VKLBU9GKARX9Ev65g) | yangjianxin1 | [GitHub](https://github.com/yangjianxin1/GPT2-chitchat) | 闲聊对话 |
| GPT2-mmi | base | - | [Google Drive](https://drive.google.com/drive/folders/1oWgKXP6VG_sT_2VMrm0xL4uOqfYwzgUP?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1ubXGuEvY8KmwEjIVTJVLww) | yangjianxin1 | [GitHub](https://github.com/yangjianxin1/GPT2-chitchat) | 闲聊对话 |
| GPT2-散文模型 | base | - | [Google Drive](https://drive.google.com/drive/folders/1rJC4niJKMVwixUQkuL9k5teLRnEYTmUf?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1nbrW5iw34GRhoTin8uU2tQ) | Zeyao Du | [GitHub](https://github.com/Morizeyao/GPT2-Chinese) | 散文 |
| GPT2-诗词模型 | base | - | [Google Drive](https://drive.google.com/drive/folders/1Z6nF1nrgTkrZcRLHedQHXb4_M9I7yQPN?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1Hy0OQ5xZcTLer9MQZW8o3g) | Zeyao Du | [GitHub](https://github.com/Morizeyao/GPT2-Chinese) | 诗词 |
| GPT2-对联模型 | base | - | [Google Drive](https://drive.google.com/drive/folders/1ZnsvS7oHRVueNKj_SeEhiQt86aze3ojj?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1j9yVQwjlXZq58wOyXK4lcg) | Zeyao Du | [GitHub](https://github.com/Morizeyao/GPT2-Chinese) | 对联 |
| RoFormer-GPT | base(L12) | [百度网盘](https://pan.baidu.com/s/11YTnWLX0ThQr2P2yW0P7GA) | - | ZhuiyiTechnology | [GitHub](https://github.com/ZhuiyiTechnology/roformer) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GPT-3

+ 2019 | Transformer-XL: Attentive Language Models Beyond a Fixed-Length Context | Zihang Dai, et al. | arXiv | [`PDF`](https://arxiv.org/abs/1901.02860)

+ 2020 | Language Models are Few-Shot Learners | Tom B. Brown, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2005.14165)

| 模型 | 版本 | 介绍 | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | ---- | ------- | ---- | ------ | -------- |
| Chinese-Transformer-XL | 29亿参数(GPT-3) | [项目首页](https://gpt-3.aminer.cn/) | [模型下载](http://dorc-model-team.ks3-cn-beijing.ksyun.com/ren-zhi/my-model/mp_rank_00_model_states.pt) | THUDM | [GitHub](https://github.com/THUDM/Chinese-Transformer-XL) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### NEZHA-Gen

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| NEZHA-Gen | base | [Google Drive](https://drive.google.com/drive/folders/1i4f_8LhaVDNjnGlLXNJ0rNgBP0E4L6V0?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1Bgle8TpcxHyuUz_jAXOBWw) | - | HUAWEI | [GitHub](https://github.com/huawei-noah/Pretrained-Language-Model) | 通用 |
| NEZHA-Gen | base | [Google Drive](https://drive.google.com/drive/folders/1B5-jxUlzhoKwFVMQ-nkqqbmJQgr1lRAp?usp=sharing) · [百度网盘](https://pan.baidu.com/s/1me6_BGYHbWFdTi80vRQ2Lg) | - | HUAWEI | [GitHub](https://github.com/huawei-noah/Pretrained-Language-Model) | 诗歌 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### CPM-Generate

| 模型 | 版本 | 资源 | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | ---- | ------- | ---- | ------ | -------- |
| CPM | 26亿参数 | [项目首页](https://cpm.baai.ac.cn/) | [模型下载](https://cpm.baai.ac.cn/download.html) | Tsinghua AI | [GitHub](https://github.com/TsinghuaAI/CPM-Generate) | 通用 |

备注:

> PyTorch转TensorFlow可参考: [CPM-LM-TF2](https://github.com/qhduan/CPM-LM-TF2)
> PyTorch转PaddlePaddle可参考: [CPM-Generate-Paddle](https://github.com/jm12138/CPM-Generate-Paddle)

<p align="right">[<a href="#top">Back to Top</a>]</p>

### T5

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| T5 | small | [🤗HF](https://huggingface.co/uer/t5-small-chinese-cluecorpussmall) | [🤗HF](https://huggingface.co/uer/t5-small-chinese-cluecorpussmall) | DBIIR @ RUC | [GitHub](https://github.com/dbiir/UER-py) | 通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### T5-PEGASUS

| 模型 | 版本 | Keras | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | ----- | ------- | ---- | ------ | -------- |
| T5-PEGASUS | base | [百度网盘](https://pan.baidu.com/s/1lQ9Dt9wZDO3IgiCL9tP-Ug) | - | ZhuiyiTechnology | [GitHub](https://github.com/ZhuiyiTechnology/t5-pegasus) | 通用 |
| T5-PEGASUS | small | [百度网盘](https://pan.baidu.com/s/1bXRVWnDyAck9VfSO9_1oJQ) | - | ZhuiyiTechnology | [GitHub](https://github.com/ZhuiyiTechnology/t5-pegasus) | 通用 |

> Keras转PyTorch可参考: [t5-pegasus-pytorch](https://github.com/renmada/t5-pegasus-pytorch)

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Mengzi-T5

| 模型 | 版本 | TensorFlow | PyTorch | 作者 | 源地址 | 应用领域 |
| ---- | ---- | --------- | ------- | ---- | ------ | -------- |
| Mengzi-T5 | base(L12) | - | [🤗HF](https://huggingface.co/Langboat/mengzi-t5-base) | Langboat | [GitHub](https://github.com/Langboat/Mengzi) | 通用 |

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
| EVA2.0-xLarge | xlarge   | [项目首页](https://wudaoai.cn/model/detail/EVA) | [[🤗HF\]](https://huggingface.co/thu-coai/EVA2.0-xlarge) | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 |                  |
| EVA2.0-large  | large    | [项目首页](https://wudaoai.cn/model/detail/EVA) | [[🤗HF\]](https://huggingface.co/thu-coai/EVA2.0-large)  | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 |                  |
| EVA2.0-base   | base     | [项目首页](https://wudaoai.cn/model/detail/EVA) | [[🤗HF\]](https://huggingface.co/thu-coai/EVA2.0-base)   | [thu-coai](https://github.com/thu-coai) | [github](https://github.com/thu-coai/EVA) | 中文开放域对话 |                  |

<p align="right">[<a href="#top">Back to Top</a>]</p>-

### BART

+ 2019 | BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension | Mike Lewis, et al. | arxiv | [`PDF`](https://arxiv.org/abs/1910.13461)

| 模型       | 版本  | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                   | 应用领域 |
| ---------- | ----- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ---------------------------------------- | -------- |
| BART-base  | base  |            | [[🤗HF\]](https://huggingface.co/fnlp/bart-base-chinese) | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 中文通用 |
| BART-large | large |            | [[🤗HF\]](https://huggingface.co/fnlp/bart-large-chinese) | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 闻仲

| 模型     | 版本       | 类型 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域 |
| -------- | ---------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | -------- |
| Wenzhong | large(L24) | GPT2 |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Wenzhong-3.5B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### 余元

| 模型   | 版本       | 类型 | TensorFlow | PyTorch                                                     | 作者                                      | 源地址                                                 | 应用领域 |
| ------ | ---------- | ---- | ---------- | ----------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------ | -------- |
| Yuyuan | large(L24) | GPT2 |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Yuyuan-3.5B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 医学领域 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### RWKV

+ 2021 | An Attention Free Transformer | Shuangfei Zhai, et al. | arxiv | [`PDF`](https://arxiv.org/abs/2105.14103)
+ 2022 | The RWKV Language Model . | [github](https://github.com/BlinkDL/RWKV-LM)

| 模型 | 版本      | 类型 | TensorFlow | PyTorch                                                      | 作者                                  | 源地址                                         | 应用领域 |
| ---- | --------- | ---- | ---------- | ------------------------------------------------------------ | ------------------------------------- | ---------------------------------------------- | -------- |
| RWKV | base(L12) |      |            | [github](https://github.com/BlinkDL/AI-Writer/releases)      | [PENG Bo](https://github.com/BlinkDL) | [github](https://github.com/BlinkDL/AI-Writer) | 小说     |
| RWKV | 7B        |      |            | [[🤗HF\]](https://huggingface.co/BlinkDL/rwkv-4-pile-7b) | [PENG Bo](https://github.com/BlinkDL) | [github](https://github.com/BlinkDL/ChatRWKV)  | 小说     |
| RWKV | 14B       |      |            | [[🤗HF\]](https://huggingface.co/BlinkDL/rwkv-4-pile-7b/tree/main) | [PENG Bo](https://github.com/BlinkDL) | [github](https://github.com/BlinkDL/ChatRWKV)  | 小说     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### PromptCLUE

| 模型             | 版本      | TensorFlow | PyTorch                                                      | 作者                                    | 源地址                                          | 应用领域 |
| ---------------- | --------- | ---------- | ------------------------------------------------------------ | --------------------------------------- | ----------------------------------------------- | -------- |
| PromptCLUE       | base(L12) |            | [[🤗HF\]](https://huggingface.co/ClueAI/PromptCLUE-base) | [ClueAI](https://huggingface.co/ClueAI) | [github](https://github.com/clue-ai/PromptCLUE) | 通用     |
| PromptCLUE-v1-5  | base(L12) |            | [[🤗HF\]](https://huggingface.co/ClueAI/PromptCLUE-base-v1-5) | [ClueAI](https://huggingface.co/ClueAI) | [github](https://github.com/clue-ai/PromptCLUE) | 通用     |
| PromptCLUE-large | large     |            | [API在线调用](https://www.clueai.cn/)                        | [ClueAI](https://huggingface.co/ClueAI) | [github](https://github.com/clue-ai/PromptCLUE) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### ChatYuan

| 模型              | 版本  | 类型 | TensorFlow | PyTorch                                                      | 作者                                 | 源地址                                        | 应用领域   |
| ----------------- | ----- | ---- | ---------- | ------------------------------------------------------------ | ------------------------------------ | --------------------------------------------- | ---------- |
| ChatYuan          | large | T5   |            | [[🤗HF\]](https://huggingface.co/ClueAI/ChatYuan-large-v1) | [ClueAI](https://github.com/clue-ai) | [github](https://github.com/clue-ai/ChatYuan) | 功能型对话 |
| ChatYuan-large-v2 | large | T5   |            | [[🤗HF\]](https://huggingface.co/ClueAI/ChatYuan-large-v2) | [ClueAI](https://github.com/clue-ai) | [github](https://github.com/clue-ai/ChatYuan) | 功能型对话 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### SkyText

| 模型    | 版本  | 类型 | TensorFlow | PyTorch                                               | 作者                                          | 源地址                                                   | 应用领域 |
| ------- | ----- | ---- | ---------- | ----------------------------------------------------- | --------------------------------------------- | -------------------------------------------------------- | -------- |
| SkyText | large | GPT3 |            | [[🤗HF\]](https://huggingface.co/SkyWork/SkyText) | [SkyWorkAIGC](https://github.com/SkyWorkAIGC) | [github](https://github.com/SkyWorkAIGC/SkyText-CN-GPT3) | 通用     |

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
| Zhouwenwang | base(L12)  | roformer |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Zhouwenwang-110M) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |
| Zhouwenwang | large(L24) | roformer |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Zhouwenwang-1.3B) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文通用 |

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
| CPT-base  | base(L12)  |            | [[🤗HF\]](https://huggingface.co/fnlp/cpt-base)  | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 通用     |
| CPT-large | large(L24) |            | [[🤗HF\]](https://huggingface.co/fnlp/cpt-large) | [fastNLP](https://github.com/fastnlp) | [github](https://github.com/fastnlp/CPT) | 通用     |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### GLM

+ 2022 | GLM: General Language Model Pretraining with Autoregressive Blank Infilling | Zhengxiao Du, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2103.10360)
+ 2022 | GLM-130B: An Open Bilingual Pre-trained Model | Aohan Zeng, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2210.02414)

| 模型     | 版本    | TensorFlow | PyTorch                                                      | 作者                                        | 源地址                                      | 应用领域 |
| -------- | ------- | ---------- | ------------------------------------------------------------ | ------------------------------------------- | ------------------------------------------- | -------- |
| GLM      | large   |            | [[🤗HF\]](https://huggingface.co/BAAI/glm-large-chinese) | [THUDM](https://github.com/THUDM)           | [github](https://github.com/THUDM/glm)      | 通用     |
| GLM      | xxlarge |            | [[🤗HF\]](https://huggingface.co/BAAI/glm-10b-chinese)   | [THUDM](https://github.com/THUDM)           | [github](https://github.com/THUDM/glm)      | 通用     |
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
| Mengzi-oscar | base(L12) |            | [[🤗HF\]](https://huggingface.co/Langboat/mengzi-oscar-base) | [Langboat](https://github.com/Langboat) | [github](https://github.com/Langboat/Mengzi) | 中文多模态-图文 |

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
| Taiyi-CLIP-Roberta-large-326M-Chinese | base |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Taiyi-CLIP-Roberta-large-326M-Chinese) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### AltCLIP

+ 2022 | AltCLIP: Altering the Language Encoder in CLIP for Extended Language Capabilities | Chen, Zhongzhi, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.06679)

| 模型    | 版本  | TensorFlow | PyTorch                                            | 作者                                     | 源地址                                                       | 应用领域        |
| ------- | ----- | ---------- | -------------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| AltCLIP | 3.22G |            | [[🤗HF\]](https://huggingface.co/BAAI/AltCLIP) | [FlagAI](https://github.com/FlagAI-Open) | [github](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/AltCLIP) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### AltDiffusion

+ 2022 | AltCLIP: Altering the Language Encoder in CLIP for Extended Language Capabilities | Chen, Zhongzhi, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2211.06679)
+ 2022 | High-Resolution Image Synthesis With Latent Diffusion Models | Rombach, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2112.10752)

| 模型         | 版本 | TensorFlow | PyTorch                                                 | 作者                                     | 源地址                                                       | 应用领域        |
| ------------ | ---- | ---------- | ------------------------------------------------------- | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| AltDiffusion | 8.0G |            | [[🤗HF\]](https://huggingface.co/BAAI/AltDiffusion) | [FlagAI](https://github.com/FlagAI-Open) | [github](https://github.com/FlagAI-Open/FlagAI/tree/master/examples/AltDiffusion) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### Taiyi-Stable-Diffusion

+ 2022 | Fengshenbang 1.0: Being the Foundation of Chinese Cognitive Intelligence | Junjie Wang, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2209.02970)
+ 2022 | High-Resolution Image Synthesis With Latent Diffusion Models | Rombach, et al. | arXiv | [`PDF`](https://arxiv.org/abs/2112.10752)

| 模型                   | 版本 | TensorFlow | PyTorch                                                      | 作者                                      | 源地址                                                 | 应用领域        |
| ---------------------- | ---- | ---------- | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------ | --------------- |
| Taiyi-Stable-Diffusion | 1B   |            | [[🤗HF\]](https://huggingface.co/IDEA-CCNL/Taiyi-Stable-Diffusion-1B-Chinese-v0.1) | [IDEA-CCNL](https://github.com/IDEA-CCNL) | [github](https://github.com/IDEA-CCNL/Fengshenbang-LM) | 中文多模态-图文 |

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
| OFA-Chinese |      |            | [[🤗HF\]](https://huggingface.co/YeungNLP/ofa-cn-base-muge-v2) | [Yang JianXin](https://github.com/yangjianxin1) | [github](https://github.com/yangjianxin1/OFA-Chinese) | 中文多模态-图文 |

<p align="right">[<a href="#top">Back to Top</a>]</p>

### QA-CLIP

| 模型            | 版本 | 视觉架构 | PyTorch                                                      | 作者                                     | 源地址                                                       | 应用领域        |
| --------------- | ---- | -------- | ------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------ | --------------- |
| QA-CLIPRN50     | 77M  | ResNet50 | [[🤗HF\]](https://huggingface.co/TencentARC/QA-CLIP/resolve/main/QA-CLIP-RN50.pt) | [腾讯](https://github.com/TencentARC-QQ) | [QA-CLIP](https://github.com/TencentARC-QQ/QA-CLIP) | 中文多模态-图文 |
| QA-CLIPViT-B/16 | 188M | ViT-B/16 | [[🤗HF\]](https://huggingface.co/TencentARC/QA-CLIP/resolve/main/QA-CLIP-base.pt) | [腾讯](https://github.com/TencentARC-QQ) | [QA-CLIP](https://github.com/TencentARC-QQ/QA-CLIP) | 中文多模态-图文 |
| QA-CLIPViT-L/14 | 406M | ViT-L/14 | [[🤗HF\]](https://huggingface.co/TencentARC/QA-CLIP/resolve/main/QA-CLIP-large.pt) | [腾讯](https://github.com/TencentARC-QQ) | [QA-CLIP](https://github.com/TencentARC-QQ/QA-CLIP) | 中文多模态-图文 |

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

* 2026.04.12 增加[MiniMax-M2.7](#ReasoningLLM)，MiniMax 开源的推理大模型，230B 总参数 MoE 架构，激活 10B 参数，支持 Agent Teams、复杂 Skills 和动态工具搜索
* 2026.04.06 增加[Gemma-4](#MultiModal-ChatLLM)，Google DeepMind 开源的多模态大模型，包含 E2B/E4B/26B A4B(MoE)/31B(Dense) 四种尺寸，支持文本/图像/音频多模态输入，256K 上下文，原生 Thinking 推理模式和 Function Calling 能力
* 2026.02.16 增加[Step-3.5-Flash, GLM-5, MiniMax-M2.5, Kimi-K2.5, Ring-2.5-1T](#ReasoningLLM)、[GLM-OCR, Ace-Step1.5, HunyuanImage-3.0-Instruct](#MultiModal-ChatLLM)、[Qwen3-Coder-Next](#Domain-ChatLLM)
* 2025.12.12 增加[deepseek-3.2]
* 2025.10.12 增加[Ling-1T,KAT-Dev-72B-Exp, GLM-4.6 ]
* 2025.09.20 增加[Tongyi DeepResearch,Qwen3-Next,Magistral Small,VoxCPM,VibeVoice,HunyuanImage]
* 2025.08.19 增加[gpt-oss-20B,gpt-oss-120B,Baichuan-M2,Ovis2.5,GLM-4.5V]
* 2025.08.05 增加[GLM-4.5,Hunyuan,Qwen3-Thinking-2507,Step3,Kimi-k2,Qwen3-Coder]
* 2025.07.07 增加[Kimi-VL-Thinking,GLM-4.1V-Thinking,Dhanishtha-2.0,ERNIE-4.5]
* 2025.06.29 增加[Qwen3-Embedding,Skywork-SWE，Hunyuan-A13B]
* 2025.06.17 增加[MiniMax-M1,Kimi-Dev]
* 2025.05.29 增加[DeepSeek-R1-0528,QwenLong-L1,Dolphin]
* 2025.05.07 增加[Qwen3,MiMo]
* 2025.04.15 增加[GLM-Z1-0414. DeepCoder, Kimi-VL-Thinking, Skywork-OR1]
* 2025.03.22 增加[Skywork-R1V,FIN-R1]
* 2025.03.09 增加[QwQ-32B, Aya Vision,CogView4]
* 2025.02.26 增加[Moonlight、Wan2.1、Step-Audio-Chat]
* 2025.02.15 增加[Ovis2]
* 2025.01.19 增加[MiniMax-01, miniCPM-O， OuteTTS]
* 2025.01.12 增加[Sky-T1,search-o1](#ReasoningLLM)
* 2025.01.02 增加[Huatuo-o1](#ReasoningLLM)
* 2024.12.25 增加[QVQ-72B]
* 2024.12.16 增加[Megrez-3B-Omni, DeepSeek-VL2]
* 2024.11.29 增加[QwQ-32B-Preview,Marco-o1 ,Skywork-01-Open,HK-01aw](#ReasoningLLM)
* 2024.11.15 增加[Qwen-2.5-coder, OpenCoder](#Domain-ChatLLM)
* 2024.11.05 增加[Hunyuan-Large](#Chat-LLM)
* 2024.10.26 增加[GLM-4-Voice,Pangea,Aya-Expanse]()
* 2024.10.22 增加[Granite 3.0](#Chat-LLM),一套全新的轻量级、多语种支持的语言模型，专为推理、编程和工具使用设计，可在计算资源受限的环境中运行，适合企业使用和定制
* 2024.09.19 增加[Qwen2.5](#Chat-LLM)
* 2024.09.08 增加[DeepSeekV2.5, MiniCPM3, Yi-Coder](#Chat-LLM)
* 2024.08.30 增加[C4AI Command R+ 08-2024,Qwen2-VL](#Chat-LLM)
* 2024.07.26 增加[JIUTIAN-Chat,Tele-FLM]()
* 2024.07.24 增加[Meta-llama3.1](#Chat-LLM)
* 2024.07.05 增加[CodeGeeX4](#Domain-ChatLLM)
* 2024.07.04 增加[internlm2.5](#Chat-LLM)
* 2024.06.19 增加[MAP-NEO-Chat](#Chat-LLM)，MAP-NEO is a fully open-sourced Large Language Model that includes the pretraining data, a data processing pipeline (Matrix), pretraining scripts, and alignment code.
* 2024.06.18 增加[DeepSeek-Coder-V2、Nemotron-4](#Chat-LLM)
* 2024.06.14 增加[Index-Chat](#Chat-LLM)
* 2024.06.08 增加[Qwen2,ChatTTS](#Chat-LLM)
* 2024.06.03 增加[GLM-4、Skywork-MoE](#Chat-LLM)
* 2024.05.30 增加[Yuan2.0-M32: Mixture of Experts with Attention Router](#ChatLLM)
* 2024.05.20 增加[CogVLM2,360VL,HunyuanDiT,星辰-Chat]
* 2024.05.13 增加[Yi-1.5]
* 2024.05.07 增加[XVERSE-V,DeepSeek-V2,XVERSE-MoE]
* 2024.04.27 增加[Qwen1.5-110B, Llama3-zh](#Chat-LLM)
* 2024.04.14 增加[MiniCPM-V2、WaveCoder、codegemma、Sailor、Nanbeige2-Chat、MiniCPM-MoE、Zhinao-Chat]()
* 2024.04.12 增加[XVERSE-MoE](#LLM)
* 2024.04.08 增加[SoftTiger、HammerLLM](#LLM)
* 2024.04.06 增加[Qwen1.5-32B](#ChatLLM)
* 2024.04.04 增加[Mengzi3](#ChatLLM)
* 2024.03.29 增加[Qwen-Audio、Qwen-MoE](#ChatLLM)
* 2024.03.13 增加[Command-R](#ChatLLM)
* 2024.03.01 增加[Breeze-Instruct, starcoder2](#ChatLLM)
* 2024.02.18 增加[aya-101、chemLLM](#ChatLLM)
* 2024.02.06 增加[Qwen1.5](#ChatLLM)
* 2024.02.02 增加[MiniCPM, TuringMM-Chat](#ChatLLM)
* 2024.02.01 增加[LongAlign-Chat，Chinese-Mixtral-Chat](#ChatLLM)
* 2024.01.31 增加[iFlytekSpark-Chat，rwkv-5-world](#ChatLLM)
* 2024.01.23 增加[Yi-VL-6/34B](#MultiModal-ChatLLM)
* 2024.01.22 增加[orion-4B](#ChatLLM)
* 2024.01.19 增加[internlm2-chat，Chinese-Mixtral](#ChatLLM)
* 2024.01.10 增加[Telechat，Code Millenials](#ChatLLM)
* 2024.01.09 增加[kagentlms](#ChatLLM),具有Agents的规划、反思、工具使用等能力的系列大模型
* 2024.01.05 增加[WizardCoder-33B-V1.1](#Domain-ChatLLM)
* 2023.12.27 增加[YaYi-30B-Chat](#ChatLLM)
* 2023.12.05 增加[SUS-Chat-34B、Aquila2-Chat-70B、Alaya-Chat-7B](#ChatLLM)
* 2023.12.01 增加[Qwen-Base-1.8/72B](#Base-LLM),[Qwen-Chat-1.8/72B](#ChatLLM),[Qwen-Audio](#MultiModal-ChatLLM)
* 2023.11.30 增加[Yuan-2.0、DeepSeek-Base](#Base-LLM),[DeepSeek-Chat](#ChatLLM)
* 2023.11.20 增加[Alaya-Chat-7B、OrionStar-Yi-Chat-34B](#ChatLLM)
* 2023.11.11 增加[XVERSE-65B、Nanbeige-Chat-16B、OpenChat 3.5](#ChatLLM)
* 2023.11.03 增加[SPHINX、Tongyi-Finance、Phind、DeepSeek-Coder](#ChatLLM)
* 2023.11.02 增加[AndesGPT-7B、SeaLLM、BlueLM](#ChatLLM)
* 2023.10.31 增加[Zephyr-7B、Mistral-7b](#ChatLLM)
* 2023.10.25 增加[zhiyin、zhilu]()
* 2023.10.20 增加[cross、taiyi、fuyu、Ziya-visual、CodeShell、CogVLM]()
* 2023.10.17 增加[Ziya2-13B-Base、Ziya2-13B-Chat](#ChatLLM)
* 2023.10.12 增加[AquilaChat2-7/13B、AquilaChat2-16K、Vulture-180B](#ChatLLM)
* 2023.10.04 增加[DISC-LawLLM、WiNGPT、ziya-coding、Vulture、AgriGPT](#ChatLLM)
* 2023.09.25 增加[Colossal-LLaMA-2-7B](#ChatLLM),相较于原始LLaMA-2，在成功提升中文能力的基础上，进一步提升其英文能力，性能可与开源社区同规模预训练SOTA模型媲美。
* 2023.09.20 增加[InternLM-20B、OpenBA](#ChatLLM),InternLM-20B已发布，包括基础版和对话版。OpenBA是一个从头开始预训练的开源15B双语非对称端到端模型。
* 2023.09.08 增加[FLM-101B、falcon-180B、Openbuddy-70B、TigerBot-70B](#ChatLLM)
* 2023.09.06 增加[Baichuan2](#ChatLLM),Baichuan 2 是百川智能推出的新一代开源大语言模型，采用 2.6 万亿 Tokens 的高质量语料训练。
* 2023.09.01 增加[DISC-MedLLM、YuLan-Chat-2、Chinese-Alpaca-2-16K](#ChatLLM),[Vally](#MultiModal-ChatLLM)
* 2023.08.29 增加[CodeLLAma、Atom](#ChatLLM),[IDEFICS](#MultiModal-ChatLLM)
* 2023.08.25 增加[sqlcoder](#ChatLLM),一个 SOTA 大型语言模型， SQLCoder 将自然语言问题转换为 SQL 查询。在开发者的开源评估框架 SQLEval 中，SQLCoder 的性能明显优于所有主要的开源模型，并且优于 OpenAI 的 GPT-3.5。
* 2023.08.23 增加[Qwen-VL](#MultiModal-ChatLLM),Qwen-VL 是阿里云研发的大规模视觉语言模型（Large Vision Language Model, LVLM）。Qwen-VL 可以以图像、文本、检测框作为输入，并以文本和检测框作为输出。
* 2023.08.21 增加[智海-录问](#ChatLLM),智海-录问(wisdomInterrogatory)是由浙江大学、阿里巴巴达摩院以及华院计算三家单位共同设计研发的法律大模型。
* 2023.08.15 增加[WizardMath](#ChatLLM),
* 2023.08.09 增加[TigerBot-13B](#ChatLLM),在Llama-2的基础上以虎博积累的技术和数据继续训练，不但保持了Llama-2出色的英文能力，更是在中文能力上填补了Llama-2的不足，各项主流中文任务中超过Llama-2的49%，在开源同类模型中具有竞争力。
* 2023.08.07 增加[XVERSE-13B](#ChatLLM),XVERSE-13B,它支持40多种语言、8192上下文长度。在多项中英文测评中，性能超过了同尺寸（130亿参数）的LLama2、Baichuan等。
* 2023.08.03 增加[通义千问](#ChatLLM),通义千问-7B（Qwen-7B）是阿里云研发的通义千问大模型系列的70亿参数规模的模型。
* 2023.07.31 增加[LLasM、Chinese-LLaVA](#MultiModal-ChatLLM)多模态大模型
* 2023.07.31 增加[Chinese-Llama-2](#ChatLLM).原版Llama-2的基础上扩充并优化了中文词表，使用了120G大规模中文数据进行增量预训练，相关模型支持4K上下文并可通过NTK方法最高扩展至18K+
* 2023.07.29 增加[BatGPT，Mozi，StarGLM](#ChatLLM).
* 2023.07.27 增加[WizardLM-v1.2](#ChatLLM).
* 2023.07.25 增加相关[Awesome列表](#other-awesome)
* 2023.07.24 增加[Llama2-chinese-chat、Jiang-chat](#ChatLLM)等对话语言模型。
* 2023.07.19 增加[LLaMA2](#LLM),Meta 发布了大家期待已久的免费可商用版本 Llama 2。
* 2023.07.16 增加[PolyLM](#LLM),PolyLM是一个通晓多语言语言的大规模语言模型，该模型可以应用于对话问答、文本生成、机器翻译和情感分析等领域，能够自动生成高质量的多语言文本。
* 2023.07.11 增加[Baichuan-13B](#LLM),baichuan-13B是由百川智能开发的一个开源可商用的大规模预训练语言模型。
* 2023.07.10 增加WizardLM-13B-V1.1
* 2023.07.09 增加VisualCLA多模态大模型
* 2023.07.04 增加[书生·浦语](#ChatLLM),书生·浦语大模型，包含面向实用场景的70亿参数基础模型与对话模型.
* 2023.07.04 增加[yuren](#MultiModal-ChatLLM),[vicuna,CuteGPT,ailawyer](#ChatLLM)
* 2023.06.30 增加[VisCPM](#MultiModal-ChatLLM),VisCPM 是一个开源的多模态大模型系列，支持中英双语的多模态对话能力（VisCPM-Chat模型）和文到图生成能力（VisCPM-Paint模型），在中文多模态开源模型中达到最佳水平。
* 2023.06.28 增加[PULSE](#ChatLLM),PULSE-中文医疗大语言模型。
* 2023.06.26 增加[CoLLaMA](#ChatLLM),CoLLaMA是基于代码的多语言大模型。
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

### Contributors

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
