# Obsidian LLM Wiki

把资料整理为模型可以按需读取、能追溯来源的知识节点，减少长对话中的上下文腐烂与反复读取原文。

## 设计

- 保留原始资料，将摘要、概念、主题和来源分开；模型的理解与跨文档关联保存在 Markdown 节点中。
- 先读索引与摘要，再读相关节点，必要时回查原文；复用已有理解，减少无关资料进入上下文。具体 Token 收益取决于资料与查询，不承诺固定比例。
- 使用 Ingest / Query / Lint 三种流程处理入库、查询、知识冲突与断链检查；围绕实际案例与用户共同迭代 Schema。

## 安装与使用

把本目录放到支持 Skill 的 Agent 的技能目录中，目录名使用 `obsidian-llm-wiki`，请 Agent 读取 [SKILL.md](SKILL.md)。首次使用提供自己的 vault 路径。此 Skill 不包含私人知识库，不是 Obsidian 常驻插件；是否可渲染特定图表或生成 PDF 取决于 Agent 环境。

| 模式 | 参考 |
|---|---|
| 配置目标知识库 | [vault-profile.md](references/vault-profile.md) |
| 增量入库 | [ingest.md](references/ingest.md) |
| 查询与成果生成 | [query-output.md](references/query-output.md) |
| 维护与检查 | [lint.md](references/lint.md) |
| 用户反馈与规则迭代 | [collaborative-iteration.md](references/collaborative-iteration.md) |

## 方法与归属

参考 Andrej Karpathy 的 [LLM Wiki 方法](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f)，由 Xingyun 结合 Obsidian、来源溯源、Schema 共同迭代与项目实践整理为 Agent Skill。此仓库不复制该方法原文，不声称原方法由本项目提出。项目自身代码与说明使用 [MIT License](LICENSE)，外部链接内容按各自授权使用。
