# TodoTree · Markdown 桌面待办墙

把待办放在桌面上，数据留在一个 Markdown 文件里。TodoTree 是一款基于 Electron 的 Windows 桌面工具，以暗金半透明窗口展示任务，提供目标、待完成、已完成、放弃四个分区。

**English:** A Windows desktop task wall built with Electron, using a local Markdown file for task storage.

**作者：[云烟错 · yunyancuo](https://github.com/yunyancuo)** · [源码](https://github.com/yunyancuo/todotree) · [下载 v1.6.1](https://github.com/yunyancuo/todotree/releases/tag/v1.6.1)

![TodoTree 原仓库运行截图](https://raw.githubusercontent.com/yunyancuo/todotree/e95b65235f70ebb618c99ea77ed65dd742856ff0/docs/demo.png)

## 可以做什么

- 桌面层锚定：通过 WorkerW / Progman 挂入桌面窗口层，方便在桌面查看任务。
- 任务组织：支持多层子任务、状态切换、分区与任务拖拽、截止日期和撤销操作。
- 本地数据：默认读取桌面的 `TODOTREE.md`，可用其他编辑器修改；提供外部修改检测与备份流程。
- 日常使用：提供 Windows 安装包、开机自启与快捷方式入口。

## 试用与源码入口

可从 [v1.6.1 发布页](https://github.com/yunyancuo/todotree/releases/tag/v1.6.1) 获取 `TodoTree-Setup-1.6.1.exe`。源码运行步骤见 [原 README](https://github.com/yunyancuo/todotree/blob/07c165118ec70afee0a308361383cc62cb882a47/README.md)：克隆仓库，在目录内执行 `npm install` 和 `npm start`。

| 入口 | 内容 |
| --- | --- |
| [desktop-layer.js](https://github.com/yunyancuo/todotree/blob/e95b65235f70ebb618c99ea77ed65dd742856ff0/desktop-layer.js) | Windows 桌面窗口层处理 |
| [main.js](https://github.com/yunyancuo/todotree/blob/e95b65235f70ebb618c99ea77ed65dd742856ff0/main.js) · [preload.js](https://github.com/yunyancuo/todotree/blob/e95b65235f70ebb618c99ea77ed65dd742856ff0/preload.js) | Electron 主进程、文件与界面通信 |
| [renderer/](https://github.com/yunyancuo/todotree/tree/e95b65235f70ebb618c99ea77ed65dd742856ff0/renderer) | 任务界面、交互和样式 |
| [任务文件模板](https://github.com/yunyancuo/todotree/blob/e95b65235f70ebb618c99ea77ed65dd742856ff0/TODOTREE-template.md) | Markdown 数据格式示例 |

技术栈：Electron、JavaScript、Node.js 文件系统、Markdown、Windows 桌面窗口接口。

## 适合一起完善的方向

Windows 版本与显示缩放兼容性、桌面层焦点切换、任务交互和 Markdown 同步边界，都可以从一个可复现的小问题开始。协作建议在原仓库或 [社区收录任务 #5](https://github.com/Alpha-Orionis/student-ai-open-lab/issues/5) 讨论。

## 版本与核对

- 2026-10-19 核对源码版本 [`e95b652`](https://github.com/yunyancuo/todotree/tree/e95b65235f70ebb618c99ea77ed65dd742856ff0)，`package.json` 为 1.6.1；发布页存在对应安装包，已查看原运行截图。
- 本次完成源码入口与发布信息核对，尚未安装、启动或复测功能。
- 2026-10-20 许可补充：源仓库已加入独立 [MIT LICENSE](https://github.com/yunyancuo/todotree/blob/07c165118ec70afee0a308361383cc62cb882a47/LICENSE)，并在构建配置中包含该文件。此项适用于后续构建；已有 v1.6.1 安装包未重新发布。本页使用来源链接与原图地址展示。

[返回成员项目展示](README.md)
