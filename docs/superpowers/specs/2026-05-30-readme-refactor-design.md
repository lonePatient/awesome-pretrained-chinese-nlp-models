# README 模块化改造设计文档

## 日期
2026-05-30

## 背景
当前 README.md 文件过大，多个模块的完整表格直接展示在首页，导致：
1. 页面过长，用户难以快速浏览
2. 信息噪音大，重点不突出
3. 与已有模块（ChatLLM、ReasoningLLM 等）的"摘要+跳转"模式不一致

## 目标
1. **统一风格**：所有大模型模块采用"README 摘要（最新5个）+ docs 完整列表"模式
2. **时间排序**：每个模块按时间倒序排列（最新在第一行）
3. **降低噪音**：README 首页只展示各模块最新 5 个条目

## 改造范围

### 涉及模块
| 模块 | 当前状态 | 改造方式 |
|------|---------|---------|
| Base-LLM | 完整表格在 README | 提取到 docs/base-llm.md，README 保留摘要 |
| Domain-Base-LLM | 完整表格在 README | 提取到 docs/domain-base-llm.md，README 保留摘要 |
| Embedding | 完整表格在 README | 提取到 docs/embedding.md，README 保留摘要 |

### 不涉及模块（保持原样）
- ChatLLM（已有 docs/chat-llm.md，已是摘要模式）
- Domain-ChatLLM（已有 docs/domain-chat-llm.md，已是摘要模式）
- MultiModal-ChatLLM（已有 docs/multimodal-chat-llm.md，已是摘要模式）
- ReasoningLLM（已有 docs/reasoning-llm.md，已是摘要模式）
- 预训练模型系列（已是摘要模式）
- Other-Awesome（已是摘要模式）
- 大模型评估基准（非表格模块，保持原样）
- 开源模型库平台（非表格模块，保持原样）
- 开源数据集库（非表格模块，保持原样）

## 详细设计

### 1. Base-LLM 模块

#### README.md 展示方式
```markdown
## Base-LLM

> 大规模基础模型：表格中只罗列出参数量`大于7B`以上模型。[查看完整列表 →](docs/base-llm.md)

| 模型 | 大小 | 时间 | 语言 | 架构 | 下载 | 项目 | 机构 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| XVERSE-MoE | 255B / A36B | 2024-09 | 中英 | MoE | [🤗HF](...) | [GitHub](...) | xverse-ai | - |
| Qwen-2.5 | 0.5~72B (7档) | 2024-09 | 中英 | CD | [🤗HF](...) | [GitHub](...) | QwenLM | [Blog](...) |
| Tele-FLM | 52B / 102B / 1TB | 2024-07 | 多语 | CD | [🤗HF](...) | - | CofeAI | [Paper](...) |
| meta-llama-3.1 | 8B / 70B / 405B | 2024-07 | 多语 | CD | [🤗HF](...) | [GitHub](...) | meta-llama | - |
| internlm2.5-Base | 7B | 2024-07 | 中英 | CD | [🤗HF](...) | [GitHub](...) | InternLM | [Technical Report](...) |

> 📋 查看全部 40+ 个模型请访问 [Base-LLM 完整列表 →](docs/base-llm.md)
```

#### docs/base-llm.md 结构
- 标题：Base-LLM - 大规模基础模型
- 返回主页链接
- 完整表格（所有条目，按时间倒序）
- 表格列：模型、大小、时间、语言、架构、下载、项目、机构、备注

### 2. Domain-Base-LLM 模块

#### README.md 展示方式
```markdown
## Domain-Base-LLM

> 各个垂直领域开源基础模型。[查看完整列表 →](docs/domain-base-llm.md)

| 模型 | 大小 | 时间 | 语言 | 领域 | 下载 | 项目 | 机构 | 架构 | 文献 | 备注 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Qwen-2.5 | 1.5/7B | 2024-09 | 中英 | 代码 | [🤗HF](...) | [Qwen2.5](...) | QwenLM | CD | [Blog](...) | |
| Qwen-2.5 | 1.5/7/72B | 2024-09 | 中英 | 数学 | [🤗HF](...) | [Qwen2.5](...) | QwenLM | CD | [Blog](...) | |
| Tongyi-Finance-Base | 14B | 2023-11 | 中文 | 金融 | [ModelScope](...) | [通义金融-14B](...) | 通义金融大模型 | CD | | |
| ChiMed-GPT | 13B | 2023-10 | 中文 | 医疗 | [🤗HF](...) | [ChiMed-GPT](...) | 中国科学技术大学 | CD | [Paper](...) | |
| CodeShell-base | 7B | 2023-10 | 中英 | 代码 | [🤗HF](...) | [codeshell](...) | WisdomShell | CD | | |

> 📋 查看全部 15+ 个模型请访问 [Domain-Base-LLM 完整列表 →](docs/domain-base-llm.md)
```

#### docs/domain-base-llm.md 结构
- 标题：Domain-Base-LLM - 垂直领域基础模型
- 返回主页链接
- 完整表格（所有条目，按时间倒序）
- 表格列：模型、大小、时间、语言、领域、下载、项目、机构、架构、文献、备注

### 3. Embedding 模块

#### README.md 展示方式
```markdown
### Embedding

> MTEB排行榜: <https://huggingface.co/spaces/mteb/leaderboard> [镜像](https://hf-mirror.com/spaces/mteb/leaderboard)
> [查看完整列表 →](docs/embedding.md)

| 模型 | 大小 | 时间 | 语言 | 领域 | 下载 | 项目 | 机构 | 文 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| Qwen3-Embedding | 0.6/4/8B | 2025-06 | 多语 | 通用 | [🤗HF](...) | [Qwen3-Embedding](...) | QwenLM | [Arxiv](...) |
| JinaColBERT V2 | large | 2024-08 | 多语 | 通用 | [🤗HF](...) | / | Jina AI | [Paper](...) |
| Conan-embedding-v1 | large | 2024-08 | 中文 | 通用 | [🤗HF](...) | / | TencentABC | [Paper](...) |
| xiaobu-v2 | large | 2024-07 | 中文 | 通用 | [🤗HF](...) | / | lier007 | |
| zpoint_large | Large | 2024-06 | 中文 | 通用 | [🤗HF](...) | / | yang | |

> 📋 查看全部 15+ 个模型请访问 [Embedding 完整列表 →](docs/embedding.md)
```

#### docs/embedding.md 结构
- 标题：Embedding 模型
- 返回主页链接
- MTEB 排行榜链接
- 完整表格（所有条目，按时间倒序）
- 表格列：模型、大小、时间、语言、领域、下载、项目、机构、文

## 实施步骤

1. 创建 `docs/base-llm.md`，复制 Base-LLM 完整表格
2. 修改 README.md 中 Base-LLM 模块为摘要模式
3. 创建 `docs/domain-base-llm.md`，复制 Domain-Base-LLM 完整表格
4. 修改 README.md 中 Domain-Base-LLM 模块为摘要模式
5. 创建 `docs/embedding.md`，复制 Embedding 完整表格
6. 修改 README.md 中 Embedding 模块为摘要模式
7. 验证所有链接和格式

## 风险评估

| 风险 | 影响 | 缓解措施 |
|------|------|---------|
| 链接失效 | 中 | 创建文件后立即验证相对路径 |
| 格式不一致 | 低 | 严格遵循现有 docs 文件格式 |
| 内容遗漏 | 中 | 复制完整表格后再删减 |

## 验收标准

- [ ] README.md 中 Base-LLM 只显示最新 5 个条目
- [ ] README.md 中 Domain-Base-LLM 只显示最新 5 个条目
- [ ] README.md 中 Embedding 只显示最新 5 个条目
- [ ] docs/base-llm.md 包含完整表格
- [ ] docs/domain-base-llm.md 包含完整表格
- [ ] docs/embedding.md 包含完整表格
- [ ] 所有跳转链接可正常点击
- [ ] 时间排序正确（最新在第一行）
