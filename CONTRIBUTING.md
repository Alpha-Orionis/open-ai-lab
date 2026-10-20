# 贡献指南

任何人都可以参与，无需学生身份、报名或加入组织，参与免费。欢迎文档、翻译、代码、测试、评测、问题分析、设计和代码评审等贡献。小修正可以直接提交 PR，无需等待任务分配；较大改动先在 Issue 协调。

## 选择一个任务

- 从 `good first issue` 开始；`help wanted` 表示欢迎协作。
- 新想法先通过“任务或项目提案”Issue 模板讨论目标、边界和验收标准。
- 开始前在 Issue 下说明计划，避免重复劳动。任务分配由维护者确认；无需公开姓名、学校、电话或简历。
- 较大任务拆成能独立验证的小任务；遇到困难及时记录卡点。

## 提交第一个 PR

1. Fork 仓库，并克隆你自己的副本。
2. 从最新的 `main` 创建分支，例如 `docs/first-pr-guide` 或 `feat/retrieval-baseline`。
3. 完成一个明确改进；不要混入无关格式修改。
4. 本地验证：文档检查链接和示例，代码运行对应测试，实验保留配置与结果。
5. 提交并推送分支，向本仓库 `main` 发起 PR。未完成时可先提交 Draft PR。
6. 填写 PR 模板并使用 `Closes #编号` 关联任务；根据评审意见继续修改。

```bash
# 将 YOUR_USERNAME 替换为你自己的 GitHub 用户名
git clone https://github.com/YOUR_USERNAME/infinite-monkey-lab.git
cd infinite-monkey-lab
git switch -c docs/first-contribution
# 编辑并检查文件后，明确选择要提交的文件
git add path/to/changed-file
git commit -m "docs: improve getting started guide"
git push -u origin docs/first-contribution
```

## 什么样的 PR 可以合并

- 解决了关联问题，交付与验收标准一致。
- 说明改了什么、为什么改、如何验证；评测结果有来源和限制。
- 文档链接有效；代码或实验按对应项目说明可以运行。
- 没有密钥、私人资料、未经授权的课程材料或无法确认来源的内容。
- 引用外部内容并保留许可；AI 辅助生成的关键内容经过人工理解和检查。
- 通常至少一名维护者评审通过后合并；重大方向调整先在 Issue 中讨论。

本仓库目前以文档为主，没有应用测试套件。新增应用时需同时提供运行、测试与依赖说明。

## AI 辅助贡献

可以使用 AI 解释代码、生成草稿或协助调试。在 PR 中说明重要的 AI 辅助部分、自己做了哪些验证。不要提交无法解释的代码、虚构引用、编造实验结果，或将他人非公开数据输入外部服务。

## 研究贡献与署名

研究开始前讨论任务分工、数据使用和预期成果；持续保留实验记录。论文署名依据实际贡献与目标期刊或会议规则共同讨论，维护者身份、付费或 PR 数量均不能自动换取署名。

## 提问与反馈

使用问题反馈模板，附复现步骤、预期和实际结果。对社区协作问题可依照 [协作规范](CODE_OF_CONDUCT.md) 处理。提交贡献即表示你有权以本仓库许可提供该内容；第三方内容需另行标注授权。

## 开放成果与许可

原创贡献按 [MIT 许可](LICENSE) 发布，保留已有作者署名。代码、文档、实验、评测与可公开的结果应随 PR 一起提供；第三方材料逐项注明来源和许可，授权不明时提供获取说明或原创替代，不直接上传。详见 [开放成果规则](docs/openness.md)。

## 不写代码也能参与

可在 [Discussions](https://github.com/Alpha-Orionis/infinite-monkey-lab/discussions) 提问和分享学习记录，或在 [Issues](https://github.com/Alpha-Orionis/infinite-monkey-lab/issues) 反馈文档问题、提出需求和报告复现结果。也欢迎翻译、界面草图、体验反馈与评审。没有本地开发环境时，可通过 GitHub 网页编辑文档并提交 PR。
