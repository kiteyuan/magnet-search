<div align="center">

<img src="./favicon.ico" width="72" height="72" alt="纸鸢磁力" />

# 纸鸢磁力

**聚合搜索 · 规则自定义 · Agent / MCP 可接入**

[![Website](https://img.shields.io/badge/Website-kiteyuan.info-0ea5e9?style=flat-square)](https://kiteyuan.info/)
[![Web](https://img.shields.io/badge/Web-magnet.kiteyuan.info-22c55e?style=flat-square)](https://magnet.kiteyuan.info/)
[![Client](https://img.shields.io/badge/Client-cilisou.kiteyuan.info-f59e0b?style=flat-square)](https://cilisou.kiteyuan.info/)
[![MCP](https://img.shields.io/badge/MCP-接入文档页-a855f7?style=flat-square)](https://magnet.kiteyuan.info/mcp)
[![Stars](https://img.shields.io/github/stars/kiteyuan/magnet-search?style=flat-square)](https://github.com/kiteyuan/magnet-search)

</div>

纸鸢磁力是一款致力于用户极致搜索体验的磁力聚合工具：通过自定义规则对接公网搜索引擎，清洗结果列表，并提供磁力解析与文件预览，降低转存垃圾文件的风险。用户可自行编写并导入引擎站点，由纸鸢并发搜索并返回结果。

> 纸鸢磁力只负责读取用户自定义的引擎站点并执行请求返回，不提供任何资源存储和查询服务。结果取决于你配置的规则与站点数据；工具内能力均为公网已有服务的二次封装。

## 自定义引擎规则 Skill

路径：[`skills/magnet-engine-rules`](./skills/magnet-engine-rules)

给需要自己写 / 改磁力搜索引擎规则的用户。

**使用方法：**

1. 将 `skills/magnet-engine-rules` 目录下载到本地，交给你的 Agent（Claude Code、Codex、Cursor 等）。
2. 把平时常用的磁力搜索站点地址（或搜索页 URL / curl）发给 Agent，它会按 Skill 分析页面并编写规则。
3. 将生成的规则文件导入纸鸢磁力的【磁力规则配置】。
4. 导入成功后，纸鸢磁力即可支持你自定义站点的磁力搜索。

## MCP 搜索与操作 Skill

路径：[`skills/magnet-mcp`](./skills/magnet-mcp)

给希望用 Agent（Claude Code、Codex、Cursor 等）直接搜索、预览、管理纸鸢磁力收藏的用户。能力通过官网 MCP 提供，不经过本仓库。

**使用方法：**

1. 打开 [纸鸢磁力 MCP 页](https://magnet.kiteyuan.info/mcp) 并登录，生成 MCP Token。
2. 将 `skills/magnet-mcp` 交给 Agent，并按 Skill 说明把 Token 配进 MCP 客户端（入口 `https://magnet.kiteyuan.info/api/v1/mcp`）。
3. 即可让 Agent 调用搜索、预览、文件结构、收藏合集与分享等工具。

---

#### 一、磁力规则

首次使用需配置规则（手动导入 / 云导入）。移动端入口：**【个人】→【磁力规则配置】**。一般不需要自定义的用户可直接使用【云导入】，默认规则通常够用。
<img width="1280" height="648" alt="image" src="https://github.com/user-attachments/assets/32951dfa-9399-4b9c-8635-5f154dab7336" />
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/adf5bdb6-98df-49a0-834a-65134a68438b" />

#### 二、磁力搜索
引擎规则配置完成后，即可进行资源搜索，除了搜索结果列表，工具还提供额外的预览和查看文件结构等附加功能。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/88a16e72-3183-4de3-a4ed-72931dc3b069" />
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/653ea0d1-92aa-481c-b407-564bb7142016" />
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/64b8f2ee-db26-4aa7-8a24-25c07aa9468d" />

#### 三、磁力解析
用户可键入任意磁力链接，自动解析出相关预览图和文件结构信息。（移动端入口：底部菜单第三个功能页面）
<img width="1280" height="648" alt="image" src="https://github.com/user-attachments/assets/c314b14f-1819-4c6d-b36d-5b45b4ee075d" />
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/654c324c-0fe8-4269-af73-c5b9716b4478" />

#### 四、我的收藏
账号登录状态下，用户可以将收藏合集进行外部分享链接/RSS订阅。
<img width="1280" height="649" alt="image" src="https://github.com/user-attachments/assets/ba7acb1c-4a4d-4e47-b945-0ea19fc8c646" />

#### 五、帖子广场
账号登录状态下，用户可以发布文章帖子。
<img width="1280" height="648" alt="image" src="https://github.com/user-attachments/assets/b322832e-fb08-4fd2-ab9f-83b3e26a083a" />
