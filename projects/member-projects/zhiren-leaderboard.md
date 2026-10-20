# 智人排行榜 · AstrBot 群聊插件

一个把群聊记分、查询、周榜播报与网页排行串起来的 AstrBot 插件。除带理由的人工加扣分外，还提供由管理员开启的 AI 裁判，适合交流机器人事件处理、LLM 接入与插件工程。

**English:** An AstrBot group-chat plugin with reason-based scoring, weekly rankings, a web dashboard and an optional LLM judge.

**作者：[云烟错 · yunyancuo](https://github.com/yunyancuo)** · [源码与使用说明](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard)

## 可以做什么

- 群聊记分：通过 `@某成员 加一分 理由` 或扣分指令记录变化，处理理由缺失、自我记分和短时间重复消息。
- 查询与历史：支持总分、周榜、个人详情与近期记录，各群数据分别保存。
- 自动播报：每周汇总上一周排行榜，相关时间逻辑独立在纯 Python 模块中。
- Web 展示：提供周榜 / 总榜、搜索、领奖台与个人详情，页面定时刷新。
- 可选 AI 裁判：管理员开启后接入配置好的 LLM Provider，结合群聊上下文生成评分。启用前应让群成员了解其用途与发言处理方式。

## 使用与源码入口

该项目依赖 AstrBot 宿主。在匹配的 AstrBot 环境中安装与配置插件；启用 AI 功能还需要可用的 LLM Provider。Web 端口可通过 `ZHIREN_WEB_PORT` 配置。

| 入口 | 内容 |
| --- | --- |
| [README](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/blob/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc/README.md) | 指令、AI 开关与 Web 配置 |
| [main.py](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/blob/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc/main.py) | AstrBot 事件、SQLite、AI 调用、网页服务与播报任务 |
| [zhiren_logic.py](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/blob/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc/zhiren_logic.py) | 指令解析、周键、时间计算与 AI 输出解析，独立于 AstrBot |
| [web/index.html](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/blob/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc/web/index.html) | 排行榜与详情界面 |
| [metadata.yaml](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/blob/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc/metadata.yaml) | 插件名称、作者、仓库与版本 |

技术栈：Python、AstrBot、SQLite、aiohttp、HTML / JavaScript，以及可选的 LLM Provider。

## 适合一起完善的方向

指令与重复消息边界、跨周时间逻辑、数据隔离、AI 输出解析，以及网页详情展示，可以分别形成小任务。集成验证使用测试群与合成消息，避免将真实群聊记录提交到公开仓库。

## 版本与核对

- 2026-10-19 核对版本 [`6ac86c4`](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/tree/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc)，`metadata.yaml` 与插件注册均为 1.2.3。
- 已核对 README、配置、源码入口与独立逻辑模块；本次未连接 AstrBot、调用 LLM、发送群消息或启动 Web 服务。
- 原仓库提供 [MIT LICENSE](https://github.com/yunyancuo/astrbot_plugin_zhiren_leaderboard/blob/6ac86c4b0f7e8d52fb7d2e63ed79358b5dcbeecc/LICENSE)。本页保留源码与作者入口。

[返回成员项目展示](README.md)
