# 深度学习基础笔记

围绕深度学习入门整理的六份 Jupyter Notebook，包含数学基础、数据处理、自动求导与线性回归实践，适合边读代码边回顾概念。

**English:** Six introductory notebooks covering mathematical foundations, data processing, automatic differentiation and linear regression.

- 原仓库：[yunyancuo/notes-for-deep-learniung](https://github.com/yunyancuo/notes-for-deep-learniung)（保留源仓库拼写）
- 作者主页：[云烟错 · yunyancuo](https://github.com/yunyancuo)
- 方向：Learning
- 当前状态：已有学习笔记与代码单元；依赖版本、完整运行记录与引用说明待完善。按基础学习材料展示，尚不作为论文复现成果。

## 阅读路线

以下文件均位于核对版本的 [源仓库根目录](https://github.com/yunyancuo/notes-for-deep-learniung/tree/27b642b549366589753b64017c048e48b695acd2)：

| 顺序建议 | Notebook | 主题 |
| --- | --- | --- |
| 1 | `线代笔记.ipynb` | 张量与线性代数基础 |
| 2 | `积分导数笔记.ipynb` | 微积分与导数 |
| 3 | `数据处理笔记.ipynb` | 数据读写与处理 |
| 4 | `自动求导笔记.ipynb` | 自动求导与梯度 |
| 5 | `线性回归的实现.ipynb` | 线性回归实现 |
| 6 | `线性神经网络.ipynb` | 线性神经网络相关笔记 |

该顺序是本介绍页的阅读建议，可按已有基础选择。

## 使用入口

先在源仓库预览 Notebook，再决定是否下载并逐单元运行。源码单元中可见 `torch`、`pandas`、`numpy`、`matplotlib`、`matplotlib_inline`、`d2l` 等导入，核对版本尚未提供依赖锁定与统一环境说明。

Notebook 中保留的输出不能替代新环境运行记录。复现时应记录 Python 与依赖版本、执行顺序、实际输出和报错；如果做教学改编，先补齐内容来源与授权说明。

## 可讨论的协作方向

- 补齐依赖清单与适合新成员的运行步骤，逐本记录能否从空内核执行。
- 为容易混淆的张量形状、梯度与回归实现补充解释或小练习。
- 核对学习资料与示例代码出处；在原仓库完善许可与来源后，再讨论教材式改编。

## 来源、许可与核对记录

- 核对日期：2026-10-19。
- 核对版本：[`27b642b`](https://github.com/yunyancuo/notes-for-deep-learniung/tree/27b642b549366589753b64017c048e48b695acd2)。
- 已核对六份 Notebook 的存在与部分代码单元的依赖导入；尚未安装依赖或执行 Notebook。
- 源仓库核对版本未提供 LICENSE 文件。本目录只提供介绍和链接，未复制 Notebook 或其输出。

[返回成员项目展示](README.md)
