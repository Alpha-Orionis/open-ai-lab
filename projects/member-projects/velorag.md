# VeloRAG · RAG 应用框架

面向知识库检索与问答的 Python 项目，包含文档处理、混合检索、知识图谱、Agent 组件与 Web 应用相关代码，适合用于学习 RAG 的模块划分和讨论应用实现。

**English:** A Python RAG project with document processing, hybrid retrieval, knowledge-graph and agent components, plus API and web interface code.

- 原仓库：[yunyancuo/velorag](https://github.com/yunyancuo/velorag)
- 作者主页：[云烟错 · yunyancuo](https://github.com/yunyancuo)
- 方向：Building / Research
- 当前状态：已有应用源码、示例、测试文件和容器配置；本次仅做源码与文档入口核对，尚未完成独立运行验证。

## 已有内容

| 模块 | 源码入口 | 可以关注的问题 |
| --- | --- | --- |
| 文档处理与主流程 | [document/](https://github.com/yunyancuo/velorag/tree/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/document)、[pipeline.py](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/pipeline.py) | 文档如何解析、分块、进入索引与检索 |
| 混合检索 | [retrieval/hybrid.py](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/retrieval/hybrid.py) | dense、sparse、hybrid 与 graph_enhanced 模式如何组合结果 |
| 知识图谱与 Agent | [graph/](https://github.com/yunyancuo/velorag/tree/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/graph)、[agent/](https://github.com/yunyancuo/velorag/tree/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/agent) | 图谱与组件编排如何接入主流程 |
| 应用接口与界面 | [server/app.py](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/server/app.py)、[frontend/](https://github.com/yunyancuo/velorag/tree/84a20a550ec805745517ce9176abb6620bffb4f2/frontend) | API、知识库管理与前端如何配合 |
| 示例与测试 | [example.py](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/example.py)、[tests/test_core.py](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/tests/test_core.py) | 示例输入、核心测试与失败路径是否完整 |

## 使用与运行入口

源仓库的 [pyproject.toml](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/pyproject.toml) 声明 Python 3.10+，并提供 server、embeddings、graph、vector 等可选依赖。

[命令行入口](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/src/velorag/__main__.py) 定义了 `serve`、`ingest`、`search`、`ask`、`status` 子命令；[容器配置](https://github.com/yunyancuo/velorag/blob/84a20a550ec805745517ce9176abb6620bffb4f2/docker-compose.yml) 列有 API、worker、Redis 和 PostgreSQL 服务。

核对版本中缺少根目录 README，但打包配置引用了 `README.md`。因此应先在源仓库补齐安装、配置和最小示例，再验证启动与检索；本页暂不把这些入口写成已跑通的安装教程。模型下载、外部服务与 API 的资源需求也需随运行记录明确。

## 可讨论的协作方向

- 工程：补齐 README、依赖与配置示例，记录从空环境到最小检索流程的步骤。
- 科研：使用有明确来源的小数据集，比较检索模式，记录检索质量、引用质量、延迟与失败案例；指标与基线先讨论。
- 社区关联：可为校园知识助手的方案讨论提供源码参考；是否采用其中组件，由 [技术方案任务 #3](https://github.com/Alpha-Orionis/student-ai-open-lab/issues/3) 单独决定。

以上为协作建议，尚未分配任务或约定维护投入。

## 来源、许可与核对记录

- 核对日期：2026-10-19。
- 核对版本：[`84a20a5`](https://github.com/yunyancuo/velorag/tree/84a20a550ec805745517ce9176abb6620bffb4f2)。
- 已检查文件路径、配置与命令行定义；尚未安装依赖、运行测试或复现性能。
- `pyproject.toml` 声明 Apache-2.0，核对版本中尚未发现独立 LICENSE 文件；授权信息需由源仓库进一步补齐。本目录仅提供介绍与链接，未复制源代码。

[返回成员项目展示](README.md)
