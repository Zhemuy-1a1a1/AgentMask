# One-File Agent Packs / 单文件 Agent 包

> One file, one agent, ready to import and use.  
> 一个文件，一个 Agent，拿去就能直接用。

[English Guide](./README.en.md) · [中文说明](./README.zh-CN.md) · [Quick Start EN](./QUICKSTART.en.md) · [快速开始 CN](./QUICKSTART.zh-CN.md) · [Upgrade / 升级路径](./UPGRADE.md) · [Agent Index / Agent 列表](./agents/INDEX.md)

---

## TL;DR / 一句话说明

This repo gives you lightweight **one-file agent packs** for real work.
You open a markdown file, copy it into your AI agent's instructions, and start using it.

这个仓库提供一批适合真实场景的 **单文件 Agent 包**。
你只需要打开一个 markdown 文件，复制到自己的 AI Agent 指令区，就可以开始使用。

---

## Start Here / 第一次来先看这里

### If you are new / 如果你是第一次接触
1. Read [Quick Start EN](./QUICKSTART.en.md) or [快速开始 CN](./QUICKSTART.zh-CN.md)
2. Open [agents/INDEX.md](./agents/INDEX.md)
3. Pick one pack that matches your scenario
4. Copy that `.md` file into your agent instructions
5. Try the example inputs in [examples/sample-inputs.md](./examples/sample-inputs.md)

### What each pack usually contains / 每个 Agent 包通常包含
- role definition / 角色定义
- core capabilities / 核心能力
- input template / 输入模板
- output structure / 输出结构
- basic rules / 基础规则
- usage notes / 使用说明

---

## Open-source Packs / 当前开源包

| Pack | What it helps with | Link |
|------|--------------------|------|
| Xiaohongshu Operator / 小红书运营助手 | Titles, post drafts, tags, cover ideas | [open](./agents/小红书运营助手.md) |
| Xiaohongshu Leads Agent / 小红书获客Agent | Comments, DMs, conversion paths | [open](./agents/小红书获客Agent.md) |
| Short Video Writer / 短视频创作Agent | Hooks, scripts, CTA | [open](./agents/短视频创作Agent.md) |
| Customer Support Assistant / 客服回复助手 | Customer replies and support flow | [open](./agents/客服回复助手.md) |
| Sales Follow-up Agent / 客服跟单Agent | Follow-up timing and conversion | [open](./agents/客服跟单Agent.md) |
| Quote Generator / 报价单Agent | Professional quotations | [open](./agents/报价单Agent.md) |
| Coding Assistant / 代码编程助手Agent | Code writing and debugging | [open](./agents/代码编程助手Agent.md) |
| Data Analyst / 数据分析Agent | Metrics, insights, next steps | [open](./agents/数据分析Agent.md) |
| Meeting Notes Agent / 会议纪要Agent | Meeting summaries and action items | [open](./agents/会议纪要Agent.md) |
| Project Manager Agent / 项目管理Agent | Task breakdown, risks, next actions | [open](./agents/项目管理Agent.md) |

---

## Example Files / 示例文件
- [Sample Inputs / 示例输入](./examples/sample-inputs.md)
- [Sample Outputs / 示例输出](./examples/sample-outputs.md)

If you're not sure how to start, copy one example input first and replace the content with your own situation.
如果你不知道怎么开始，先复制一条示例输入，再把里面的内容改成自己的情况。

---

## Why this repo exists / 为什么做这个仓库

Most people do **not** need more prompt theory.
They need something they can:
- import quickly
- understand quickly
- adapt quickly
- use for actual work

大多数人并不缺更多 prompt 理论，
他们缺的是一个：
- 能快速导入
- 能快速看懂
- 能快速改造
- 能真正拿去干活

So the structure here is intentionally simple:
**one scenario → one pack → one markdown file**

所以这里故意把结构压得很简单：
**一个场景 → 一个包 → 一个 markdown 文件**

---

## Upgrade Path / 升级路径

This repo is the lightweight public layer.
The full commercial version can include:
- richer templates
- SOPs
- FAQ
- examples
- combo packs
- industry custom versions

这个仓库放的是轻量公开层。
完整版商业包可包含：
- 更完整模板
- SOP
- FAQ
- 案例库
- 组合包
- 行业定制版

See: [UPGRADE.md](./UPGRADE.md)

---

## License / 许可证

[CC BY-NC 4.0](./LICENSE)

You can learn from it, adapt it, and share it with attribution.
You may **not** directly resell the open-source version for commercial use.

你可以学习、改写、传播（需署名），
但**不能**直接把开源版拿去商用倒卖。
