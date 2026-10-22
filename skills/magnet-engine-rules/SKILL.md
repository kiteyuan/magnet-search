---
name: magnet-engine-rules
description: >-
  Writes and validates 纸鸢磁力 (Kiteyuan Magnet) crawler engine rules in regulars.json
  (stepConfig, sortList, listPointer, nextStep). Use when the user adds or edits search
  engines, imports rules, or provides a search URL or curl to reverse-engineer a site.
---

# 纸鸢磁力 · 引擎规则

通用 Agent 说明文档（Markdown + JSON 样例），供任意 AI 编程助手阅读，不依赖特定 IDE。

## 何时使用

- 用户要**新增/修改**磁力搜索引擎规则
- 用户给出**搜索页 URL** 或 **curl**，需要生成可导入的 JSON
- 用户问 `stepConfig`、`listPointer`、`regulars.json` 怎么写

## 工作流

1. 读 [reference.md](./reference.md) 中的 **最小可用模板** 与 **stepConfig** 字段说明。
2. 对照 [examples/](./examples/) 里完整样例的字段组织方式（样例仅作结构参考，站点可能已失效）。
3. 用 URL/curl 请求页面 → 定 `listPointer` / `itemFields` → 必要时加 `nextStep` → 对齐 `sortList` 与 `navigation.sorts`。
4. **验证**：JSON 可解析；至少 2 个关键词、`page=1/2` 能稳定解析出 `title` 与 `magnet`（或经二跳得到磁链）。输出 `items/title/magnet/date/size` 统计。

## 输出约定

- 交付**可导入**的 JSON：`configName`、`configVersion`、`regulars[]` 中**一条或多条**引擎对象。
- `engineName` 不与用户已有引擎重名。
- 能列表直出磁链则**不要**滥用 `nextStep`。

## 运行时行为（摘要）

占位符 `%SearchKey%` / `%Page%` / `%Offset%` 会在请求前替换；相对 URL 拼到 `engineUrl`；HTML 的 `attr:href` 会转为绝对链接。
