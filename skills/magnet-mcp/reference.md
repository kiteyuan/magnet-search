# 纸鸢磁力 MCP 工具参考

入口：`https://magnet.kiteyuan.info/api/v1/mcp`  
Token 管理：`https://magnet.kiteyuan.info/mcp`（需登录）

鉴权：`Authorization: Bearer <mcp_token>`

## 磁力

### magnet_search

从本地库按匹配度检索磁力。

| 参数 | 类型 | 说明 |
|------|------|------|
| `query` | string | 必填，搜索关键词 |
| `limit` | number | 可选，条数，默认约 7，最大 20 |

### magnet_preview

获取磁力预览信息（截图、类型等）。

| 参数 | 类型 | 说明 |
|------|------|------|
| `magnet_link` | string | 必填 |

### magnet_files

解析磁力文件结构树。

| 参数 | 类型 | 说明 |
|------|------|------|
| `magnet_link` | string | 必填 |

## 收藏合集

### favorite_collections_list

列出当前用户合集。无参数。

### favorite_collection_detail

| 参数 | 类型 | 说明 |
|------|------|------|
| `collection_key` | string | 必填，如 `default` |

### favorite_collection_create

| 参数 | 类型 | 说明 |
|------|------|------|
| `label` | string | 必填，合集名称 |

### favorite_collection_rename

| 参数 | 类型 | 说明 |
|------|------|------|
| `collection_key` | string | 必填 |
| `label` | string | 必填，新名称 |

### favorite_collection_delete

| 参数 | 类型 | 说明 |
|------|------|------|
| `collection_key` | string | 必填；不可删除 `default` |

## 合集分享

### favorite_share_detail

| 参数 | 类型 | 说明 |
|------|------|------|
| `code` | string | 必填，合集码 |

### favorite_share_enable

| 参数 | 类型 | 说明 |
|------|------|------|
| `collection_key` | string | 必填 |

返回合集码、分享链接、RSS 等（以实际响应为准）。

### favorite_share_disable

| 参数 | 类型 | 说明 |
|------|------|------|
| `collection_key` | string | 必填 |

### favorite_share_import

| 参数 | 类型 | 说明 |
|------|------|------|
| `code` | string | 必填 |
| `label` | string | 可选，导入后合集名称 |
