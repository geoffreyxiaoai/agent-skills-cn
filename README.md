# agent-skills-cn

> 跨平台 AI Agent Skills 中文精选 · Curated cross-platform AI Agent Skills, with Chinese reviews

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**中文**：本仓库精选**跨平台通用**的 AI Agent Skills（适用于 Claude Code、Muse、Cursor、Codex、Gemini CLI、OpenCode 等），每条附**中文说明**与**实测点评**，并标注适用平台与安装方式。

**English**: A curated collection of **cross-platform** AI Agent Skills (Claude Code, Muse, Cursor, Codex, Gemini CLI, OpenCode, …), each with a Chinese review, supported platforms, and install instructions.

## 🎯 定位 / Positioning

Skills 生态正在爆发（Anthropic 官方插件市场、obra/superpowers 等），但**中文精选 + 实测点评**缺位。本项目：

- ✅ 只收**跨平台通用** skills（不绑定单一平台）
- ✅ 每条带**中文一句话说明** + **中文实测点评**
- ✅ 标注**适用平台**与**安装方式**，按用途分类
- ✅ 与 [awesome-muse-cn](https://github.com/) 互补：那边只收 Muse 生态，这里是跨平台通用

## 📌 收录标准 / Curation criteria

1. 仓库/技能真实存在，来源可查（链接有效、文档齐全）
2. 优先收录有明确安装方式、可跨平台使用的 skills
3. 优先收录有第三方评测、社区口碑（star 数、评测文章）的条目
4. **未实际安装运行验证的条目标注 🧪 待实测**

状态图例 / Status legend：

| 标记 | 含义 |
|------|------|
| ✅ 已验证 | 仓库存在、文档齐全，安装方式来自官方文档或可信来源 |
| 🧪 待实测 | 来源可信但尚未实际安装运行，点评基于公开资料 |

---

## 🏛️ 官方精选 / Official

### anthropics/skills（官方技能标准库）

- **简介**：Anthropic 官方技能仓库，定义 Skills 开放标准的生产级实现，涵盖文档处理、开发工具、工作流自动化。Anthropic's official skills repo: production-ready implementations of the Skills standard.（~99k ⭐，截至 2026-10）
- **适用平台**：Claude Code、Claude.ai、API
- **安装**：`/plugin marketplace add anthropics/skills`
- **中文点评**：官方出品的「黄金标准」，既是生产工具也是学习范本。文档处理四件套（docx/pdf/pptx/xlsx）在各自场景下几乎是必装；frontend-design 生成的前端界面质量明显高于裸提示词。✅ 已验证

包含的子技能：

| 技能 | 一句话中文说明 |
|------|---------------|
| `docx` | 创建、编辑、分析 Word 文档，支持修订追踪与批注 |
| `pdf` | PDF 提取文本/表格、合并拆分、处理表单 |
| `pptx` | 创建编辑 PPT，支持布局、模板、图表与自动生成幻灯片 |
| `xlsx` | 创建编辑 Excel，支持公式、格式化、数据分析与可视化 |
| `doc-coauthoring` | 结构化协作写文档的工作流 |
| `frontend-design` | 生产级前端/UI 组件设计与开发 |
| `artifacts-builder` | 用 React + Tailwind + shadcn 构建复杂 HTML artifacts |
| `mcp-server`（mcp-builder）| 高质量 MCP 服务器构建指南 |
| `webapp-testing` | 用 Playwright 测试本地 Web 应用 |
| `skill-creator` | 教你写出高质量 skills 的官方指南 |
| `internal-comms` | 内部沟通写作（状态报告、Newsletter、FAQ） |
| `algorithmic-art` | 用 p5.js 做生成艺术（种子随机、流场、粒子系统） |
| `canvas-design` | 设计 PNG/PDF 视觉艺术 |
| `slack-gif-creator` | 生成符合 Slack 尺寸限制的动画 GIF |
| `brand-guidelines` / `theme-factory` | Anthropic 品牌规范配色与 artifacts 主题 |

### claude-plugins-official（官方插件市场）

- **简介**：随 Claude Code 自动注册的官方市场，291 个插件（截至 2026-09），含 GitHub / Figma / Slack / Sentry 集成、安全审查与多语言 LSP 服务器。Anthropic's curated plugin marketplace, auto-registered in Claude Code.
- **适用平台**：Claude Code
- **安装**：首次启动自动注册；`/plugin install github@claude-plugins-official`
- **中文点评**：官方策展，质量与安全性最高的一批插件。装机先看这里，再去社区市场淘。✅ 已验证

---

## 💻 编程开发 / Coding

### obra/superpowers

- **简介**：Jesse Vincent（@obra）打造的完整软件开发方法论技能包：强制先头脑风暴出 spec、测试驱动（RED→GREEN→REFACTOR）、子 agent 分工实现、完整分支生命周期。A complete software-dev methodology as composable skills: brainstorm-first, mandatory TDD, subagent-driven development.（~62k ⭐，Claude Code 市场第 4 大安装量插件）
- **适用平台**：Claude Code、Cursor、Codex、OpenCode
- **安装**：
  ```
  /plugin marketplace add obra/superpowers-marketplace
  /plugin install superpowers@superpowers-marketplace
  ```
- **中文点评**：第三方评测给了 5/5（Essential）。最大特点是技能**按上下文自动触发**，不用手动调用。适合「想让 AI 按固定流程干活」的团队；但对喜欢随手写代码的人来说仪式感偏重，建议先试 `/brainstorm`。✅ 已验证

### VersoXBT/claude-recommended-skills

- **简介**：基于 Anthropic 团队《Lessons from Building Claude Code》提炼的 9 个生产级技能：4 轮代码评审、CI/CD、OODA 故障排查、基础设施运维、安全查库分析、业务流程自动化、代码脚手架等。9 production-ready skills distilled from Anthropic's own engineering lessons.
- **适用平台**：Claude Code（SKILL.md 标准，兼容其他 Agent）
- **安装**：`npx skills add https://github.com/VersoXBT/claude-recommended-skills`
- **中文点评**：每个技能都带 "Gotchas"（真实生产踩坑记录）和可执行脚本，不是纸上谈兵。`runbook-investigator` 的 OODA 排查流程和 `code-quality-review` 的严重程度分级很实用。✅ 已验证

包含：`code-quality-review`（结构化 4 轮评审）、`cicd-deployment`（CI/CD 与发布）、`runbook-investigator`（OODA 故障调查）、`infra-operations`（基础设施日常运维）、`data-fetch-analysis`（安全查库/监控/API 分析）、`business-process-automation`（带回滚的流程自动化）、`code-scaffolding`（贴合现有代码风格的脚手架）、`library-api-reference`（内部库文档查询）、`product-verification`（验证改动产生正确的产品行为）。

### Jeffallan/claude-skills 🧪

- **简介**：66 个面向全栈开发者的专用技能，把 Claude Code 变成专家结对程序员。66 specialized skills for full-stack developers.（8.1k ⭐）
- **适用平台**：Claude Code
- **安装**：见仓库 README
- **中文点评**：数量最多的一批开发者技能合集之一，覆盖全栈场景。🧪 待实测

### samber/cc-skills-golang 🧪

- **简介**：Golang 专用 Agent 技能合集（文档、测试、代码规范等）。Agentic skills collection for Golang projects.（1.2k ⭐）
- **适用平台**：Claude Code
- **安装**：见仓库 README
- **中文点评**：Go 生态少见的技能合集，Gopher 值得一看。🧪 待实测

### levy-n/claude-useful-skills 🧪

- **简介**：5 个自用生产级技能：spec 驱动开发（gsd-orchestration）、AI Agent 系统设计（agent-architect）、17 个 ML/DL 子技能、提示词工程（prompt-master）、SVG logo 设计。5 production-ready skills: spec-driven dev, agent design, ML/DL, prompt engineering, logo design.
- **适用平台**：Claude Code
- **安装**：`npx claude-useful-skills`
- **中文点评**：作者自用后开源的组合，一键安装很省事；ML/DL 子技能对做模型的人有吸引力。🧪 待实测

### epicgames/unreal-engine-skills-for-claude-code 🧪

- **简介**：Epic Games 官方出品的 Unreal Engine 开发技能，已上架官方插件市场。Official Unreal Engine skills, published in the official marketplace.（290 ⭐）
- **适用平台**：Claude Code
- **安装**：`/plugin install unreal-engine-skills-for-claude-code@claude-plugins-official`
- **中文点评**：大厂官方背书的垂直领域技能，UE 开发者必备。🧪 待实测

---

## ✍️ 写作与文档 / Writing & Docs

### obra/the-elements-of-style（Elements of Style）

- **简介**：基于 Strunk《风格的要素》（1918）的写作指导技能，含 18 条清晰简洁写作规则全文。Writing guidance based on Strunk's classic, all 18 rules included.
- **适用平台**：Claude Code、Cursor（经 superpowers 市场）
- **安装**：`/plugin install elements-of-style@superpowers-marketplace`（需先添加 obra/superpowers-marketplace）
- **中文点评**：英文写作的「内功心法」型技能，对技术文档、英文邮件提升明显；中文写作不直接适用。✅ 已验证

### hardikpandya/stopslop 🧪

- **简介**：在输出前自动屏蔽 100+ 种 AI 写作套话（空洞开场、强调滥用、商业黑话）。Bans 100+ AI writing clichés before output.
- **适用平台**：Claude.ai、Claude Code（文件夹上传即用）
- **安装**：下载仓库后按 SKILL.md 方式加载
- **中文点评**：和中文语境下的「去 AI 味」需求高度契合，值得一试。🧪 待实测

---

## 🎨 设计与创意 / Design

官方 `anthropics/skills` 中的 `frontend-design`、`algorithmic-art`、`canvas-design`、`slack-gif-creator` 已覆盖本类主流需求（见上文官方精选），社区补充如下：

### levyn（svg-logo-designer，见 claude-useful-skills）🧪

- **简介**：专业 SVG logo 生成技能，输出多版生产级标志。Generate multiple production-grade logo variants.
- **适用平台**：Claude Code
- **安装**：随 `npx claude-useful-skills` 安装
- **中文点评**：独立开发者做品牌视觉的低成本方案。🧪 待实测

---

## 📊 数据分析 / Data Analysis

### anthropics/skills → xlsx

- **简介**：见官方精选。Excel 创建/编辑/分析，支持公式、格式化与可视化。
- **适用平台**：Claude Code、Claude.ai、API
- **中文点评**：做报表、数据清洗时调用，效果稳定，是文档四件套里复用率最高的一个。✅ 已验证

### VersoXBT/data-fetch-analysis

- **简介**：安全地查询数据库、监控系统与 API，并分析产出报告。Safely query DBs, monitoring and APIs, then analyze and report.
- **适用平台**：Claude Code
- **安装**：随 claude-recommended-skills 安装
- **中文点评**：强调「安全查询」而非直接给写权限，运维/数据同学的生产友好设计。✅ 已验证

---

## ⚙️ 自动化运维 / DevOps & Automation

### VersoXBT/cicd-deployment + infra-operations + business-process-automation

- **简介**：CI/CD 流水线管理与发布、基础设施日常运维（健康检查/证书/依赖/容量）、带可观测性与回滚的重复工作流自动化。
- **适用平台**：Claude Code
- **安装**：随 claude-recommended-skills 安装
- **中文点评**：把「自动化」和「回滚/可观测」绑在一起是正确姿势，适合 SRE 团队。✅ 已验证

### obra/private-journal-mcp 🧪

- **简介**：带语义搜索的私人日记 MCP 服务器，项目级与全局双存储。Private journaling MCP with semantic search, project-local + global storage.
- **适用平台**：Claude Code（经 superpowers 市场）
- **安装**：`/plugin install private-journal-mcp@superpowers-marketplace`
- **中文点评**：给 Agent 加「长期记忆」的轻量方案，隐私敏感数据注意本地存储配置。🧪 待实测

---

## 🔍 研究与营销 / Research & Marketing

### mvanhorn/last30daysskill 🧪

- **简介**：强制 Claude 先检索近 30 天的最新信息再写作，解决训练数据过时问题。Makes Claude research the last 30 days before writing.
- **适用平台**：Claude.ai、Claude Code（文件夹上传即用）
- **安装**：下载 `github.com/mvanhorn/last30daysskill` 后加载
- **中文点评**：写行业分析、新闻稿之前挂上，能显著减少「过时知识」幻觉。🧪 待实测

### coreyhaines31/marketingskills 🧪

- **简介**：加载文案框架、钩子公式与 campaign 结构，让营销输出真正带转化。Copywriting frameworks, hook formulas, campaign structures.
- **适用平台**：Claude.ai、Claude Code（文件夹上传即用）
- **安装**：下载仓库后加载
- **中文点评**：英文营销文案场景口碑不错，中文营销需自行调教框架。🧪 待实测

---

## 🛠️ 技能开发与安装工具 / Meta & Tooling

### anthropics/skills → skill-creator

- **简介**：Anthropic 官方的技能开发互动指南，问答式帮你生成技能的目录结构与文档。Interactive guide to building effective skills.
- **适用平台**：Claude Code、Claude.ai、API
- **中文点评**：想自己写技能的人先装这个，少走弯路。✅ 已验证

### vercel-labs/skills

- **简介**：`npx skills` CLI，一条命令跨平台安装技能。One-command cross-platform skill installer.
- **适用平台**：Claude Code、Cursor、VS Code 等
- **安装**：`npx skills i vercel-labs/agent-skills`
- **中文点评**：跨平台技能分发的事实标准工具之一，本仓库多数社区条目都可用它安装。✅ 已验证

### ai-ecoverse/gh-upskill

- **简介**：按 [agentskills.io](https://agentskills.io) 规范从 GitHub 批量安装/管理技能的 CLI（含 gh 插件形态）。Install Agent Skills from GitHub repos in batch, per the agentskills.io spec.
- **适用平台**：Claude Code、Cursor、VS Code 等
- **安装**：`curl -fsSL https://raw.githubusercontent.com/ai-ecoverse/gh-upskill/main/install.sh | bash` 或 `gh extension install ai-ecoverse/gh-upskill`
- **中文点评**：适合一次装多个技能、跨项目管理技能的人；支持私有仓库是加分项。✅ 已验证（仓库与文档存在，安装方式来自官方 README）

---

## 📚 精选目录与市场 / Directories & Marketplaces

找更多技能时，先看这些目录（它们本身也是技能生态的重要入口）：

| 目录 | 规模 | 说明 |
|------|------|------|
| [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | 53.3k ⭐ | 最大的 Claude Skills 精选目录之一 |
| [sickn33/antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | 32.5k ⭐ | 1400+ 可安装技能，覆盖 Claude Code / Cursor / Codex CLI / Gemini CLI |
| [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) | 15.4k ⭐ | 1000+ 官方与社区技能，跨平台 |
| [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills) | 11.1k ⭐ | 持续更新的精选目录，含技能原理与安全指南 |
| [alaatt/awesome-claude-skills-1](https://github.com/alaatt/awesome-claude-skills-1) | — | 另一个活跃的精选目录 |
| [skillsmp.com](https://skillsmp.com) | 50 万+ skills | Web 市场，支持分类搜索 |
| [skillhub.club](https://skillhub.club) | 7000+ | 经 AI 评审的技能市场，覆盖 Claude / Codex / Gemini |
| [skillpicker.xyz](https://skillpicker.xyz) | — | 按用途（"skills for X"）检索技能 |

---

## 🤝 贡献 / Contributing

欢迎 PR 补充新技能！请按以下格式提交，并注明是否已实测：

```markdown
### 技能名

- **简介**：一句话英文 + 中文说明
- **适用平台**：Claude Code / Cursor / ...
- **安装**：安装命令或步骤
- **中文点评**：你的使用体验 / 或标注 🧪 待实测
```

要求：仓库真实存在、链接有效；与 awesome-muse-cn（只收 Muse 生态）不重复——这里只收**跨平台通用** skills。

## 📄 License

MIT
