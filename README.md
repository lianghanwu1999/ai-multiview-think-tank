# 🏛️ 智囊议会 (AI Multiview Think Tank)

**5 位独立顾问 + 1 位主席的多维度 AI 分析决策框架**

---

## 这是什么？

智囊议会是一个**跨平台的 AI 分析技能**，让 LLM 从 5 个固定维度独立审视任意问题或文档，最后由主席汇总给出综合结论 + 可执行方案。

不需要任何 API 调用、外部工具或多 Agent 框架——**纯 prompt 即可运行**。

## 五位顾问

| # | 角色 | 核心职责 |
|---|------|---------|
| 1 | 🔴 **唱反调者** | 质疑漏洞、找风险、反向论证 |
| 2 | 🟡 **第一性原理思考者** | 抛开表象，回归本质拆解核心逻辑 |
| 3 | 🟢 **发散拓展者** | 补充关联信息、延伸视角、替代方案 |
| 4 | 🔵 **外部旁观者** | 中立第三方客观评价 |
| 5 | 🟣 **落地执行者** | 实操、流程、成本、可行性 |

## 🏛️ 主席

综合 5 方观点，输出：

- **核心共识** — 各方一致认同的关键点
- **核心分歧** — 存在张力的观点及权衡
- **最终结论** — 不模棱两可的明确判断
- **可执行方案** — 含优先级、时间线和风险提示

---

## 支持的平台

| 平台 | 目录 | 使用方式 |
|------|------|---------|
| **Codex** | [`codex/`](./codex/) | 安装为 Codex Skill，输入 `$ai-multiview-think-tank` 触发 |
| **Claude** | [`claude/`](./claude/) | 粘贴到 Claude Projects 的 Project Instructions |
| **ChatGPT** | [`chatgpt/`](./chatgpt/) | 粘贴到 GPTs 的 Instructions 或 Custom Instructions |
| **OpenCode** | [`opencode/`](./opencode/) | 配置为 OpenCode 的 instructions / rules |
| **通用** | [`universal/`](./universal/) | 通用 System Prompt，适用于 Hermes / Llama / Qwen / DeepSeek / Ollama / Open WebUI / LobeChat 等 |

---

## 快速开始

### Codex

```bash
# 将 codex/ 目录复制到 Codex 的 skills 路径
cp -r codex/ ~/.agents/skills/ai-multiview-think-tank/

# 然后在 Codex 中输入：
$ai-multiview-think-tank 帮我分析一下这个方案
```

### Claude

1. 打开 [Claude Projects](https://claude.ai/projects)
2. 创建新项目 → 将 `claude/project-instructions.md` 的全部内容粘贴到 Project Instructions
3. 对话中说「启动智囊议会」即可触发

### ChatGPT

1. 创建自定义 GPT 或使用 Custom Instructions
2. 将 `chatgpt/custom-instructions.md` 的内容粘贴到 Instructions 字段
3. 对话中说「启动智囊议会」

### 开源模型 (Hermes / Llama / DeepSeek 等)

将 `universal/system-prompt.md` 配置为 System Prompt，支持：
- Ollama (Modelfile 的 SYSTEM 指令)
- Open WebUI (模型设置 → System Prompt)
- LobeChat (角色设定 → 系统提示词)
- 任意 OpenAI 兼容 API (messages 中的 system role)

### OpenCode

将 `opencode/instructions.md` 配置为 OpenCode 的 instructions / rules 文件。

---

## 示例输出

对于问题「Skills 对 AI 发展的影响」，议会的输出结构如下：

```
## 🏛️ 智囊议会 — Skills 对 AI 发展的影响

### 1. 🔴 唱反调者
[质疑：Skills 固化思维、制造能力幻觉、安全边界模糊...]

### 2. 🟡 第一性原理思考者
[本质：降低 AI 在特定领域的认知负载，如同人类的 SOP...]

### 3. 🟢 发散拓展者
[延伸：类比 App Store 生态、倒逼模型进化、催生新职业...]

### 4. 🔵 外部旁观者
[中立：务实有效的方案，但治理和信任问题被忽视...]

### 5. 🟣 落地执行者
[实操：先找高频场景、小版本迭代、季度复审维护...]

## 🏛️ 议会主席汇总
[共识 + 分歧 + 最终结论 + 可执行方案]
```

---

## 目录结构

```
ai-multiview-think-tank/
├── README.md                        # 本文件
├── codex/                           # Codex Skill
│   ├── SKILL.md
│   └── agents/openai.yaml
├── claude/                          # Claude Projects
│   └── project-instructions.md
├── chatgpt/                         # ChatGPT GPTs / Custom Instructions
│   └── custom-instructions.md
├── opencode/                        # OpenCode
│   └── instructions.md
└── universal/                       # 通用 System Prompt
    └── system-prompt.md
```

## 为什么选择这个框架？

市面上有「多智能体辩论」的框架（如 AutoGen、CrewAI），但它们需要多轮 API 调用、外部编排、代码集成。智囊议会的优势在于：

- **零依赖** — 纯 prompt，不需要任何代码或外部工具
- **跨平台** — 一份核心逻辑，适配所有主流 LLM 平台
- **轻量** — 单次 LLM 调用即可完成完整分析
- **结构化** — 5+1 的固定角色框架，输出稳定可预期
- **可复用** — 一次配置，永久使用

---

## License

MIT
