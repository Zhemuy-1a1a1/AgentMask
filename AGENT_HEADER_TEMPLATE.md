# Agent 文件统一头部模板

## 标准 YAML Front Matter 模板

```yaml
---
name: agent-name
description: Agent 功能简述，一句话说明这个 Agent 是做什么的
use_case: 具体使用场景（何时应该调用这个 Agent）
target_user: 精确到角色层级（不是"所有人"，而是具体角色）
version: "1.0.0"
updated: "2026-03-22"
tokens_estimate: "3k-8k（弱模型友好）"
---
```

## 字段说明

| 字段 | 必填 | 说明 | 示例 |
|---|---|---|---|
| name | ✅ | kebab-case，与文件名一致 | `xiaohongshu-operator` |
| description | ✅ | 一句话功能描述 | `小红书种草文专家，擅长爆款标题+正文章节结构` |
| use_case | ✅ | 何时用，用在哪里 | `发布前润色、选题枯竭时、竞品分析时` |
| target_user | ✅ | 角色层级 | `运营新手 / 独立博主 / MCN机构运营` |
| version | ✅ | 语义化版本 | `1.0.0` |
| updated | ✅ | 更新日期 | `2026-03-22` |
| tokens_estimate | 建议 | 输入+输出估算 | `5k-15k（弱模型友好）` |

## 使用方式

每个 `agents/zh-CN/` 下的 `.md` 文件，开头插入以上 YAML 块，保留原有内容不变。

## 统一头部优势

- **可机读**：工具/脚本可自动解析元数据，生成索引
- **可搜索**：快速知道每个 Agent 适用场景
- **弱模型友好**：`tokens_estimate` 提示成本，方便用户选型
- **版本追踪**：`updated` 字段让维护者知道哪些 Agent 需要更新

## 最小化备选方案（Comment Block 格式）

如果目标平台不支持 YAML，可用 Markdown comment：

```markdown
<!--
name: agent-name
description: 一句话描述
use_case: 使用场景
target_user: 目标用户
version: 1.0.0
updated: 2026-03-22
-->
```
