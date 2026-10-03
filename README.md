# AI 工作流 · 递进阅读

一个本地阅读器，收录 **Anthropic (Claude)、OpenAI、Pi、Nous Research (Hermes)** 四个平台关于 AI 工作流 / 智能体的文章与报告、第一篇的官方引用网络，以及 **agent/harness 领域 20 篇最有方法论增量的论文与技术报告**。所有链接已于 **2026-09-29** 用 Chromium 逐条打开核对；**每篇附 1000–3000 字中文深度解读**（工程类完成于 2026-10-02，论文类完成于 2026-10-03，基于全文撰写）。

## 怎么打开

任选其一：

- **直接双击 `index.html`**（纯单文件，无外部依赖，离线可用）
- 或用本地服务（推荐，方便浏览器书签）：

  ```bash
  cd ai-workflow-reading
  python3 -m http.server 8642 --bind 127.0.0.1
  # 打开 http://127.0.0.1:8642
  ```

## 递进结构（9 个阶段 · 56 篇）

| 阶段 | 主题 | 篇数 |
|---|---|---|
| 1 | 地基：理解 AI 工作流与智能体（工作流 vs 智能体的判断框架） | 4 |
| 2 | 核心机制：上下文、工具与执行环境（含 Anthropic 与 Pi 在 MCP 上的交锋） | 8 |
| 3 | 实战：四大平台的编程智能体（Claude Code / Codex / Pi / Hermes） | 9 |
| 4 | 长时运行与可靠性：harness、安全与评估 | 7 |
| 5 | 走出文章：延伸阅读与动手环节 | 2 |
| 6 | 延伸 · 第一篇的引用网络（Building effective agents 的官方外链解析） | 6 |
| 7 | 论文 · 评测：把智能体变成可测量的对象（SWE-bench / τ-bench / METR / AI Agents That Matter / HAL / Agent-as-a-Judge / 评测噪声） | 7 |
| 8 | 论文 · 可靠性与控制面：从提示词防御到系统级治理（间接注入 / CaMeL / AI Control / MAST / Progent / A2A / AGENTS.md） | 7 |
| 9 | 论文 · 长时程与多智能体协作推理（Generative Agents / Voyager / MemGPT / Reflexion / ToT / 别建多智能体） | 6 |
| 7-9 | 论文层只收有**方法论增量**的工作：每个工作改变什么、为什么重要、值得深读哪些章节，都有专文论证 | |

阶段 6 收录第一篇文章亲自指向的下一跳：五模式 cookbook 代码页、MCP 发布文、Tool Use GA、SWE-bench Sonnet 研究、Agent SDK 总览，以及文中点名的三个外部框架（Strands / Rivet / Vellum）对比。

## 每篇两层内容

- **速览层**：来源徽章、难度、日期、预计时长、3 条中文要点、一句「为什么读」
- **深度层（📖 展开）**：约 1000–3000 字中文深度解读，固定六节——它在回应什么问题 / 核心内容拆解 / 关键细节与数据 / 与清单其他文章的呼应 / 实践启示 / 局限与时效。所有数字与日期取自原文，旧文附时效评估（如第 1 篇的官方过时横幅、第 14 篇的自声明）

另有 **[ste.html](ste.html)**：ASD-STE100（简化技术英语）风格的「简明观点版」——36 个条目的核心观点各压缩成几句零歧义英文（一句一事、≤20 词、主动语态、一词一义、无习语），附中文对照，适合快速回忆与复习。

## 递进阅读模式（功能）

- **专注模式**：点任意文章标题或右上角「▶ 开始专注阅读」，一次只显示一篇，从第一篇未读的接续；解读区默认展开
- **进度持久化**：已读状态存在浏览器 `localStorage`，重开页面不丢
- **键盘导航**（专注模式内）：`←` `→` 切换，`Enter` 标记已读并继续，`Esc` 退出
- **筛选**：按来源（Anthropic / OpenAI / Pi / Nous / 生态框架）筛选，「只看未读」开关
- **重置进度**：右上角按钮

## 想加文章或改解读？

- 加文章：编辑 `index.html` 中的 `ARTICLES` 数组，把 `id` 加进 `STAGES` 对应阶段的 `arts`，序号和进度自动重算
- 改深度解读：在 `index.html` 里搜 `/*DEPTH-INJECT-START*/`，其中 `window.__DEPTH` 以文章 id 为键存放各篇解读 HTML，直接改对应字段即可

## 来源说明

- **Pi** 指 Mario Zechner（badlogic）开发的极简编程智能体（`earendil-works/pi`），文章来自其博客 mariozechner.at
- **Hermes** 指 Nous Research 的开源自托管智能体 Hermes Agent（hermes-agent.nousresearch.com）
- 深度解读为中文原创分析（要点提炼 + 论证拆解 + 时效评估），便于消化；完整内容请点「阅读原文」看原站
