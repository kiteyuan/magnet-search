纸鸢磁力是一款致力于用户极致搜索体验的磁力聚合工具，工具引擎通过自定义规则的磁力引擎搜索（均来自国内公网服务）清洗出最佳结果列表，同时提供磁力解析和文件预览图功能，为用户搜索时大大减少垃圾文件的转存风险。用户可自定义编写规则导入自用的引擎站点，纸鸢磁力从而负责并发搜索和返回，快速搜索全网海量资源。

> 纸鸢磁力只负责读取用户自定义的引擎站点并执行请求返回，不提供任何资源存储和查询服务，查询到的结果内容只取决于用户编写的自定义规则和站点数据，任何数据均不经过服务器。（工具内的任何服务均为公网已有服务二次封装而成）

## 仓库说明

本仓库是 **产品介绍** 与 **磁力引擎规则编写指南**（Agent Skill 格式，不绑定某一 IDE）。

| 内容 | 路径 |
|------|------|
| 规则 Skill 入口 | [`skills/magnet-engine-rules/SKILL.md`](./skills/magnet-engine-rules/SKILL.md) |
| 字段详解 | [`skills/magnet-engine-rules/reference.md`](./skills/magnet-engine-rules/reference.md) |
| JSON 样例 | [`skills/magnet-engine-rules/examples/`](./skills/magnet-engine-rules/examples/) |

### 给 AI 助手用（通用）

`SKILL.md` + `reference.md` + `examples/` 是任意编程向 AI（Claude Code、Codex、Cursor、Copilot Chat 等）都能直接读的 Markdown / JSON，**不要求**专用插件。

1. 把本仓库 clone 或只下载 `skills/magnet-engine-rules/` 目录。
2. 在对话里让 AI **先读** `SKILL.md`，写规则时对照 `reference.md`，结构不确定时看 `examples/`。
3. 若你的工具支持「项目知识 / 规则文件」，把上述目录加入上下文或 `@` 引用即可。

部分工具的可选快捷方式（非必须）：Cursor 可复制到 `~/.cursor/skills/magnet-engine-rules/`；其他产品按各自「自定义指令 / AGENTS.md / skills」目录放置同一文件夹即可。

---

#### 一、磁力规则

首次使用需配置规则（手动导入 / 云导入）。移动端入口：**【个人】→【磁力规则配置】**。编写规则时可让 AI 阅读本仓库 [Skill 入口](./skills/magnet-engine-rules/SKILL.md) 与 [字段说明](./skills/magnet-engine-rules/reference.md)。
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
