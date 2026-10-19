# FeiyuCursor · 大肥鱼动态鼠标指针

围绕大肥鱼角色主题制作的 Windows 鼠标方案，覆盖正常选择、文本输入、链接选择、等待、后台运行与窗口缩放等 17 项指针状态。项目同时公开指针文件、动画生成脚本、预览图和安装包。

**English:** A character-themed Windows cursor pack with 17 cursor roles, animated busy states and Python build scripts.

**作者：[云烟错 · yunyancuo](https://github.com/yunyancuo)** · [原仓库与下载入口](https://github.com/yunyancuo/FeiyuCursor)

![FeiyuCursor 原仓库效果预览](https://raw.githubusercontent.com/yunyancuo/FeiyuCursor/e2861c2f808ec81ef0a6bfac8fa7cb706c7127bf/%E6%95%88%E6%9E%9C%E9%A2%84%E8%A7%88.png)

## 作品特点

- 完整鼠标方案：覆盖 17 项 Windows 指针角色，包含静态 `.cur` 与动态 `.ani` 文件。
- 动态反馈：忙与后台运行状态采用 16 帧动画，展示角色呼吸、星轨等变化。
- 操作细节：在造型之外处理点击热点、文本选择对比度与多尺寸输出。
- 制作流程公开：可阅读 Python 图像处理与指针生成脚本，了解从素材到可安装方案的过程。

## 使用与制作入口

在原仓库下载 ZIP 包后，按 [使用说明](https://github.com/yunyancuo/FeiyuCursor/blob/e2861c2f808ec81ef0a6bfac8fa7cb706c7127bf/%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.txt) 选择安装脚本或 INF 安装方式，再在 Windows 鼠标属性中应用方案。当前说明面向 Windows 10 / 11。

| 入口 | 内容 |
| --- | --- |
| [FeiyuCursor_大肥鱼指针.zip](https://github.com/yunyancuo/FeiyuCursor/blob/e2861c2f808ec81ef0a6bfac8fa7cb706c7127bf/FeiyuCursor_%E5%A4%A7%E8%82%A5%E9%B1%BC%E6%8C%87%E9%92%88.zip) | 已生成的指针与安装材料 |
| [build_feiyu.py](https://github.com/yunyancuo/FeiyuCursor/blob/e2861c2f808ec81ef0a6bfac8fa7cb706c7127bf/build_feiyu.py) | Python 图像处理、指针与动画生成 |
| [安装鼠标指针.inf](https://github.com/yunyancuo/FeiyuCursor/blob/e2861c2f808ec81ef0a6bfac8fa7cb706c7127bf/%E5%AE%89%E8%A3%85%E9%BC%A0%E6%A0%87%E6%8C%87%E9%92%88.inf) | Windows 鼠标方案注册与角色映射 |

技术栈：Python、Pillow、NumPy、Windows CUR / ANI 指针格式与 INF 安装配置。该作品是桌面美化与素材工程项目，运行时不依赖大模型服务。

## 适合一起完善的方向

不同 DPI 与深浅背景下的可读性、指针热点、动态节奏、安装恢复说明，以及素材到多尺寸成品的构建流程，都可以形成具体的体验反馈或工程任务。

## 版本与核对

- 2026-10-19 核对版本 [`e2861c2`](https://github.com/yunyancuo/FeiyuCursor/tree/e2861c2f808ec81ef0a6bfac8fa7cb706c7127bf)，已查看原预览图、使用说明、生成脚本与成品文件。
- 本次未运行生成脚本或应用鼠标方案，兼容性仍需实际使用验证。
- 核对版本未提供独立 LICENSE。角色、素材、代码的权利归属与使用范围以原仓库及相关权利人的说明为准；本页仅使用来源链接与原图地址展示。

[返回成员项目展示](README.md)
