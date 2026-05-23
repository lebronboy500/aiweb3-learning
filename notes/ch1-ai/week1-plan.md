# Week 1 学习计划 — AI 基础

> Phase: P1-AI基础 | Week 1 of 4
> 对应 Handbook: https://aiweb3.school/zh/handbook/ai/

**本周目标**: 理解 AI / ML / DL / LLM 核心原理，掌握 Prompt Engineering 基础，完成 LLM API 调用 Demo。

---

## 每日任务

### Day 1 (Mon) — 环境 + 全局认知

**阅读**
- [ ] Handbook: [AI Introduction](https://aiweb3.school/zh/handbook/ai/introduction/)
- [ ] 仓库: `notes/ch1-ai/overview.md`（已有内容，补充自己的理解）

**动手**
- [ ] 配置 Python 3.11 venv，安装 `openai httpx python-dotenv`
- [ ] 创建 `projects/week1/` 目录，初始化 `README.md`

**产出**
- [ ] `daily-logs/` 当日打卡
- [ ] `notes/ch1-ai/overview.md` 补写「个人笔记 & 疑问」部分

---

### Day 2 (Tue) — LLM 原理深挖

**阅读**
- [ ] Handbook: [Large Language Models](https://aiweb3.school/zh/handbook/ai/llm/)
- [ ] 补充阅读: [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/)（选读，重点看图）

**理解要点**
- Tokenization 的工作方式
- Transformer 的 Attention 机制直觉理解
- 预训练 vs 微调 vs RLHF 的区别

**产出**
- [ ] `notes/ch1-ai/llm-notes.md`：用自己的话解释 Token、Context Window、Temperature 三个概念
- [ ] `daily-logs/` 当日打卡

---

### Day 3 (Wed) — Prompt Engineering

**阅读**
- [ ] Handbook: [Prompts](https://aiweb3.school/zh/handbook/ai/prompt/)
- [ ] OpenAI Prompt Engineering Guide（官方文档，浏览即可）

**动手实验**（在 ChatGPT 或 Playground 里做）
- [ ] 实验 1: Zero-shot — 直接问一个技术问题，记录输出质量
- [ ] 实验 2: Few-shot — 给 2-3 个例子后再问同一问题，对比差异
- [ ] 实验 3: Chain-of-thought — 加上 "Think step by step"，对比前两次

**产出**
- [ ] `notes/ch1-ai/prompt-notes.md`：记录三次实验的 prompt + 输出 + 分析
- [ ] `daily-logs/` 当日打卡

---

### Day 4 (Thu) — AI Agent 架构

**阅读**
- [ ] Handbook: [Agents](https://aiweb3.school/zh/handbook/ai/agent/)
- [ ] 浏览: [Agentic Commerce Track](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/)（感受 AI Agent 在 Web3 的方向）

**理解要点**
- Agent = LLM + Memory + Tools + Planning 的组合
- Tool calling 的工作机制（Function Calling API）
- ReAct 模式：Reason → Act → Observe 循环

**产出**
- [ ] `notes/ch1-ai/agent-notes.md`：画一个简单的 Agent 工作流程图（ASCII 或文字描述）
- [ ] `daily-logs/` 当日打卡

---

### Day 5 (Fri) — LLM API 编码

**目标**: 跑通第一个 Python LLM 调用

**代码任务**
```
projects/week1/
├── 01_hello_llm.py       # 基础调用：单次 Q&A
├── 02_chat_loop.py       # 多轮对话：维护 messages history
└── README.md             # 记录运行方式和结果截图路径
```

`01_hello_llm.py` 最低要求：
- 用 openai 库调用 chat completions
- 接收命令行参数作为 prompt
- 打印 token 使用量

`02_chat_loop.py` 最低要求：
- while 循环读取用户输入
- 维护完整 messages 列表
- 输入 "exit" 退出并打印总 token 消耗

**产出**
- [ ] 代码提交到 `projects/week1/`
- [ ] `daily-logs/` 当日打卡

---

### Day 6 (Sat) — Prompt 工程化 Demo

**目标**: 在 Day 5 代码基础上加入结构化 Prompt，让 LLM 扮演一个角色

**代码任务**
```
projects/week1/03_role_agent.py
```

要求：
- System prompt 定义角色：一个 Web3 技术讲师
- 输入任意 Web3 概念，输出结构化解释（概念定义 / 类比 / 应用场景）
- 用 JSON mode 或 response_format 规范输出格式

**产出**
- [ ] 代码提交，在 `projects/week1/README.md` 中附上一次完整运行示例
- [ ] `daily-logs/` 当日打卡

---

### Day 7 (Sun) — 周复盘

**整理任务**
- [ ] 补全本周所有未完成的 notes
- [ ] 更新根目录 `README.md`：勾选 `- [x] Week 1: AI 基础`，加上本周亮点一句话

**复盘文档**: 新建 `notes/ch1-ai/week1-review.md`，回答三个问题：
1. LLM 和传统 if-else 程序最本质的区别是什么？
2. Temperature 设为 0 和 1 分别适合什么场景？
3. AI Agent 和普通 LLM chatbot 的区别在哪里？

**提交**
- [ ] 一次整体 commit，message 格式：`week1: AI基础学习完成 — notes + demos`
- [ ] Push 到 GitHub

---

## 本周产出清单

| 文件 | 类型 | 说明 |
|------|------|------|
| `notes/ch1-ai/llm-notes.md` | 笔记 | LLM 原理 |
| `notes/ch1-ai/prompt-notes.md` | 笔记 | Prompt 实验记录 |
| `notes/ch1-ai/agent-notes.md` | 笔记 | Agent 架构理解 |
| `notes/ch1-ai/week1-review.md` | 复盘 | 周复盘问答 |
| `projects/week1/01_hello_llm.py` | 代码 | LLM Hello World |
| `projects/week1/02_chat_loop.py` | 代码 | 多轮对话 |
| `projects/week1/03_role_agent.py` | 代码 | 结构化角色 Demo |
| `daily-logs/YYYY-MM-DD.md` × 7 | 打卡 | 每日记录 |

---

## 参考链接

- Handbook AI 板块: https://aiweb3.school/zh/handbook/ai/introduction/
- OpenAI API Docs: https://platform.openai.com/docs/guides/chat
- The Illustrated Transformer: https://jalammar.github.io/illustrated-transformer/
- Prompt Engineering Guide: https://www.promptingguide.ai/zh

---

*by lebron | aiweb3-learning | Week 1*
