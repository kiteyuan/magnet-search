纸鸢磁力是一款致力于用户极致搜索体验的磁力聚合工具，工具引擎通过自定义规则的磁力引擎搜索（均来自国内公网服务）清洗出最佳结果列表，同时提供磁力解析和文件预览图功能，为用户搜索时大大减少垃圾文件的转存风险。用户可自定义编写规则导入自用的引擎站点，纸鸢磁力从而负责并发搜索和返回，快速搜索全网海量资源。

> 纸鸢磁力只负责读取用户自定义的引擎站点并执行请求返回，不提供任何资源存储和查询服务，查询到的结果内容只取决于用户编写的自定义规则和站点数据，任何数据均不经过服务器。（工具内的任何服务均为公网已有服务二次封装而成）

工具地址：[纸鸢发布页](https://kiteyuan.info/) · [网页版 1](https://magnet.kiteyuan.info/) · [网页版 2](https://search.kiteyuan.info/) · [纸鸢下载内测](https://mybt.kiteyuan.info/) · APP：微信公众号【纸鸢花的小屋】回复【纸鸢磁力】【纸鸢下载】【纸鸢下载内测码】

## 仓库说明

本仓库是 **产品说明 + Agent Skill（写引擎规则）**，不再包含桌面客户端源码与 GitHub Actions 打包。

| 内容 | 路径 |
|------|------|
| Cursor / Agent Skill（推荐） | [`skills/magnet-engine-rules/`](./skills/magnet-engine-rules/) |
| 规则字段详解 | [`skills/magnet-engine-rules/reference.md`](./skills/magnet-engine-rules/reference.md) |
| 完整规则样例 | [`skills/magnet-engine-rules/examples/`](./skills/magnet-engine-rules/examples/) |

### 安装 Skill（Cursor）

将 `skills/magnet-engine-rules` 复制到：

- **个人**：`~/.cursor/skills/magnet-engine-rules/`
- **项目**：`<你的仓库>/.cursor/skills/magnet-engine-rules/`

或在对话中 `@skills/magnet-engine-rules/SKILL.md`（若已放在当前工作区）。

桌面 / Android 客户端在 [kiteyuan-search](https://github.com/kiteyuan/kiteyuan-search) 的 `desktop/` 目录本地构建，不在此仓库发版。

---

#### 一、磁力规则

首次使用工具需要配置规则，可手动导入和云导入，导入成功后即可开始搜索（移动端入口：【个人】-【我的规则】）。可借助 Claude Code、Codex、Cursor 等 AI 工具，配合上方 Skill 编写自定义规则。

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/6a5b0d78-2bca-4ca6-8e7e-e935561b17b6" />

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/9d5e0231-66ca-40e2-96fc-2a79e16e3f5e" />

#### 二、磁力搜索

引擎规则配置完成后，即可进行资源搜索，除了搜索结果列表，工具还提供额外的预览和查看文件结构等附加功能。

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/f933f4f7-3809-431c-842a-21cafb5a6d66" />

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/98f75cbf-c405-4211-8d22-411d656c397c" />

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/97c825e7-20cb-4b85-9ea9-3aff7efc3850" />

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/321ff841-7309-438e-a9c8-8a481f7f85a1" />

#### 三、磁力解析

用户可键入任意磁力链接，自动解析出相关预览图和文件结构信息。（移动端入口：底部菜单第三个功能页面）

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/776154a7-c83f-4890-af03-4ede97553a28" />

#### 四、我的收藏

账号登录状态下，用户可以将收藏合集进行外部分享链接/RSS订阅。

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/afc77bc1-e483-4441-9d03-9b2a1ba053d6" />

#### 五、帖子广场

账号登录状态下，用户可以发布文章帖子。

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/d37c9f7d-7465-445b-84ab-8ca8cbae2253" />

#### 六、磁力转存

磁力转存的相关功能均在内测中，并且工具地址在【纸鸢下载】项目中（非纸鸢磁力），内测期间需要内测码。

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/092f803d-b309-4caa-b88b-393f6f922b3f" />

<img width="2880" height="1462" alt="image" src="https://github.com/user-attachments/assets/f7122c23-ae98-472d-a7e8-2e8909664b0d" />
