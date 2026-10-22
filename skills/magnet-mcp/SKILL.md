---
name: magnet-mcp
description: >-
  Connects an AI agent to 纸鸢磁力 (Kiteyuan Magnet) via MCP to search magnets,
  preview files, and manage favorite collections/shares. Use when the user wants
  agent-driven magnet search or collection ops through magnet.kiteyuan.info MCP.
---

# 纸鸢磁力 · MCP 搜索与操作

通过纸鸢磁力官方 **MCP（Model Context Protocol）** 接口，让 Agent 代为搜索磁力、预览资源、管理收藏合集与分享。

## 前置条件（必须先做）

1. 打开 [纸鸢磁力 MCP 页](https://magnet.kiteyuan.info/mcp) 并**登录账号**。
2. 在页面上**生成 / 重置 MCP Token**（明文仅当次可见，请自行保存；丢失需重新生成）。
3. 将 Token 配置进 Agent 的 MCP 客户端（见下方配置）。未登录或未配置有效 Token 时，鉴权会失败（401）。

## MCP 连接

- 说明与 Token 管理页：`https://magnet.kiteyuan.info/mcp`
- Streamable HTTP 入口：`https://magnet.kiteyuan.info/api/v1/mcp`
- 鉴权头：`Authorization: Bearer <mcp_token>`（不要把 Token 写进 URL query）

客户端配置示例（字段名必须是 `mcpServers`）：

```json
{
  "mcpServers": {
    "kite-search": {
      "url": "https://magnet.kiteyuan.info/api/v1/mcp",
      "headers": {
        "Authorization": "Bearer <mcp_token>"
      }
    }
  }
}
```

配置保存后，确认 Agent 已加载 `kite-search`（或你起的同名服务）下的工具，再开始调用。

## 何时使用

- 用户要用 Agent **搜索**纸鸢磁力本地库结果
- 用户要对磁力链接做 **预览 / 文件结构** 解析
- 用户要管理 **收藏合集**（列表、创建、改名、删除）或 **分享 / 导入合集**

工具名与参数细节见 [reference.md](./reference.md)。

## Agent 工作流

1. 确认 MCP 已连上且可用；若工具调用返回 401，提示用户回 MCP 页检查登录与 Token。
2. 搜索：调用 `magnet_search`（`query` 必填；`limit` 可选，默认约 7、上限 20）。
3. 需要预览图/类型等信息：对结果里的磁力链接调用 `magnet_preview`。
4. 需要文件树：调用 `magnet_files`。
5. 收藏：先 `favorite_collections_list`，再按需 `favorite_collection_detail` / `create` / `rename` / `delete`（不可删 `default`）。
6. 分享：`favorite_share_enable` / `disable` / `detail` / `import`。

## 注意

- Token 等同账号凭证，勿提交到公开仓库或发给不可信方。
- 搜索结果来自纸鸢磁力服务侧能力；向用户展示时保留标题、大小、日期、磁力链接等关键字段即可。
- 不要编造未通过 MCP 返回的磁链或合集数据。
