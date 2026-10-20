# 社区启动方案

状态：筹备方案。当前实际运行载体是 [Alpha-Orionis/infinite-monkey-lab](https://github.com/Alpha-Orionis/infinite-monkey-lab)，尚未建立独立 GitHub Organization，应用尚未实现。

第一阶段目标：让不同背景的参与者从不会参与开源，到能够共同完成一个高质量 AI 应用，并让科研型与就业型成员都获得可验证成果。

## 名称与品牌定位

| 项目 | 当前约定 |
| --- | --- |
| 对外名称 | 无限猴子实验室 · Infinite Monkey Lab |
| 一句话定位 | 面向所有人、以 GitHub 为核心的 AI 开源共创社区 |
| 标语 | 不断尝试，共同创造。 · Keep Trying. Create Together. |
| 学习载体 | 真实的 AI 应用项目与开源贡献 |
| 成长方向 | AI Learning → AI Building → Research / Career 双轨实践 |
| 核心证据 | Issue、PR、Review、可运行应用、实验记录与公开演示 |
| 协作方式 | 中文为主，主要项目提供英文简介，开展跨背景、跨地区协作 |

正式名称为「无限猴子实验室」，英文名 Infinite Monkey Lab，仓库名为 infinite-monkey-lab。名字借用无限猴子的思想实验，表达普通人借助 AI 不断尝试、验证与改进，也能共同创造有价值成果的信念。我们是独立社区项目；不宣称高校官方身份、已有导师网络或已实现的成员规模。

## 现阶段与未来四仓库架构

现阶段继续维护一个已有仓库，先验证入门、协作、评审与交付流程。未来有明确维护者和实质内容后，再按以下职责拆分：

```text
<未来组织，名称待定>/
├── .github/                 组织主页与默认协作文件
│   ├── profile/README.md
│   ├── CONTRIBUTING.md
│   └── CODE_OF_CONDUCT.md
├── handbook/                学习路线与成员手册
├── project-hub/             项目提案、项目标准与任务导航
└── campus-ai-assistant/     首个应用的实现、测试、评测与部署
```

| 未来仓库 | 目前内容位置 | 拆分条件 |
| --- | --- | --- |
| `.github` | [组织主页草稿](../templates/organization-profile-README.md)、根目录贡献与行为规范 | 正式组织名称、Owner 和公开主页内容确认 |
| `handbook` | `docs/` 的入门、成长、科研、就业与招募指南 | 有持续维护手册的负责人，导航迁移方案明确 |
| `project-hub` | `projects/`、`templates/`、[项目成果标准](project-standards.md) 与现有 Issues | 有多个需要统一跟踪的实际项目，避免重复维护任务 |
| `campus-ai-assistant` | [校园知识助手提案](../projects/campus-knowledge-assistant/README.md) | 维护者、技术范围、数据许可和资源方案明确，首批实现可落地 |

拆分时保留作者与历史记录，更新旧入口和交叉链接，明确原有 Issues 的去向。独立仓库各自放置许可文件，不把默认社区文件视作许可证继承。

GitHub 的公开 `.github` 仓库可以为同一账号下未自行定义相应文件的仓库提供默认社区文件；组织主页使用其中的 `profile/README.md`。当前仓库中的 `.github/` 目录只服务本仓库，不等同于已经建立了组织级 `.github` 仓库。参见 [默认社区文件](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file) 与 [组织主页说明](https://docs.github.com/en/account-and-profile/concepts/organization-profile)。

## GitHub 工具分工

| 工具 | 使用方式 | 本仓库状态 |
| --- | --- | --- |
| Organization | 正式成员、仓库与权限的统一归属 | 后续筹建，当前为个人账号下的公开仓库 |
| Discussions | 技术问答、经验分享与开放讨论 | 已启用，用于问答和开放交流；可交付任务仍通过 Issues 跟踪 |
| Issues | 学习、研究与开发任务，记录范围、依赖和验收 | 已有公开启动任务，后续任务由提案拆分 |
| Pull Requests | 交付代码、文档和实验，完成评审与反馈 | 贡献流程与 PR 模板已提供 |
| Projects | 汇总任务状态、负责人、方向与迭代 | 建议后续启用；尚未创建看板 |
| Actions | 在新增代码时执行对应测试与质量检查 | 尚未配置；当前为文档仓库 |
| Pages | 在内容稳定后展示组织介绍、教程与成果 | 尚未部署，当前入口为 README |

未来看板建议字段：Status（待讨论 / 可认领 / 进行中 / 待评审 / 已完成 / 暂停）、Track、负责人、迭代、成果链接。Issue 和 PR 保持为原始任务与交付记录；不在多处复制互相冲突的状态。

## 首期只启动一个项目

首发选择 Campus Knowledge Assistant（校园知识助手），先交付文本/Markdown 资料问答、检索、来源引用和资料不足时的拒答。多模态作为未来扩展。

- 学习成员：验证入门流程、准备有授权的样例资料与问题。
- 科研成员：提出检索基线、引用质量和拒答评测方案，保留配置与误差分析。
- 工程成员：实现导入、检索、问答接口与界面，提供测试和本地运行说明。
- 项目负责人和维护者：统一问题定义、拆分任务、安排评审并控制范围。

技术方案可评估 Python、FastAPI、RAG、前端与 Docker；这些是待比较的选择，尚未确定依赖栈。优先小模型、自写示例资料和低成本本地方案，不默认让贡献者承担模型费用。

Paper Reproduction Lab 和 Open Agent Workshop 暂为后续候选，见 [项目目录](../projects/README.md)。

## 四周一次共创周期

以下是建议节奏，实际开始日期、例会时间和负责人尚待确认，本文件不创建日历活动或定时任务。

| 周次 | 工作 | 必须留下的记录 |
| --- | --- | --- |
| 第 1 周 | 确认场景、维护人力、资料范围与最小验收，认领任务 | 项目提案、任务列表、已确认的资源边界 |
| 第 2 周 | 完成基线或最小流程，尽早提交 Draft PR | 可检查的中间成果、运行记录、困难与依赖 |
| 第 3 周 | 共同评审、补充测试与实验，修复失败案例 | Review 反馈、修改记录、评测配置与结果 |
| 第 4 周 | 演示、复现检查、复盘与下一轮范围选择 | 成果链接、贡献说明、已知限制与下轮任务 |

建议每周一次约 30 分钟的线上短会，每月一次成果展示；允许异步参与，并公开文字纪要。考试或课程繁忙时可缩减范围或暂停，不以出勤和打卡次数排名。

## 启动顺序与现有任务

1. 按 [招募与参与规则](recruitment.md) 确认首批核心成员意向，优先补足项目负责人和评审支持。
2. [#1 验证新成员入门流程](https://github.com/Alpha-Orionis/infinite-monkey-lab/issues/1)。
3. [#2 确认资料授权并整理示例数据](https://github.com/Alpha-Orionis/infinite-monkey-lab/issues/2)。
4. [#3 提交技术方案与最小版本任务拆解](https://github.com/Alpha-Orionis/infinite-monkey-lab/issues/3)。
5. 方案通过讨论后再拆分实现、评测与部署任务，按 [成果标准](project-standards.md) 验收。

前三个月建议目标见 [路线图](../ROADMAP.md)，具体角色、决策和退出机制见 [治理章程](../GOVERNANCE.md)。

## 平台使用说明

本方案使用普通仓库、模板和 Issues 组织学习任务，不依赖 GitHub Classroom。GitHub 官方公告给出的 Classroom 退出日期为 2026 年 8 月 28 日，见 [官方公告](https://github.blog/changelog/2026-05-26-github-classroom-sign-ups-are-no-longer-available/)。后续创建 Organization 时按 [官方组织创建指南](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch) 办理。
