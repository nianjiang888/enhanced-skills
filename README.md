# 中文增强版技能集（Enhanced CN）

7 个自包含 Agent 技能，走的是同一条路子：抓海外热门技能的核心方法论，独立重写，补上中文场景和中文团队习惯。不照搬原文，不冒充原创。

共 **7** 个技能包，全部自包含（包内即可跑通，无需额外依赖）。

## 技能一览

| # | 技能包 | 名称 | 做什么 |
|---|---|---|---|
| 1 | `cn-code-review` | 中文代码审查 | 对代码改动做四阶段中文审查（上下文—高层—逐行—总结），用严重度标记区分阻塞项与建议项，补中文技术栈检查项。 |
| 2 | `cn-competitor-analysis` | 中文竞品情报分析 | 用天眼查、36氪、微信指数、小红书、七麦等中文信源做竞品识别与维度跟踪，输出带出处的 SWOT、定位图与战斗卡。 |
| 3 | `cn-content-topic` | 中文内容选题与标题工程 | 用六路信源批量挖选题并逐条评分排序，为优先选题生成多版本候选标题、首屏钩子与平台合规标注。 |
| 4 | `cn-doc-summary` | 中文长文与报告摘要 | 把公众号、知乎、飞书、研报等中文长文或报告，按受众与目的做成结论先行、可引用、去 AI 味的结构化摘要。 |
| 5 | `cn-meeting-notes` | 中文会议纪要整理 | 把会议录音转写稿或零散笔记，整理成结论先行、行动项带责任人和截止时间的中文结构化纪要，并清理口语赘词。 |
| 6 | `cn-policy-decoder` | 中文政策解读与申报拆解 | 对红头文件先定效力层级与文号，再拆支持方向与申报硬条件，匹配申报主体，输出时间倒排与待核实清单。 |
| 7 | `cn-translation-proofread` | 中文翻译校对与本地化质检 | 做翻译准确性评分与句级质检，识别中文翻译腔、中英混排标点问题，按技术、产品、营销、通知四场景切换标准。 |

## 目录结构

```
enhanced/
├── cn-code-review/
├── cn-competitor-analysis/
├── cn-content-topic/
├── cn-doc-summary/
├── cn-meeting-notes/
├── cn-policy-decoder/
├── cn-translation-proofread/
```

每个技能包结构：`SKILL.md`（技能定义）+ `references/`（配套依据库：检查项、清单、模板）。纯指令型技能，无脚本依赖，Agent 读取 SKILL.md 即按工作流执行。

## 本地使用

```
git clone <仓库地址>
```

把需要的技能目录整体复制到你的 Agent skills 目录即可。技能由 Agent 读取 `SKILL.md` 后按工作流执行，无需单独运行脚本。

## 从 GitHub 导入到 SkillHub

每个技能独立目录，目录根即 `SKILL.md`，不含二进制文件。在 SkillHub 发布页选「从 GitHub 导入」，绑定账号后会自动扫出候选技能。

**注意：平台单次最多导入 5 个技能，7 个需要分 2 批。**

| 批次 | 技能 |
|---|---|
| 第 1 批 | `cn-code-review`、`cn-competitor-analysis`、`cn-content-topic`、`cn-doc-summary`、`cn-meeting-notes` |
| 第 2 批 | `cn-policy-decoder`、`cn-translation-proofread` |

## 许可

MIT

## 出品方与更多工具

本技能系列由墨金格团队出品。主产品[墨金格](https://www.mojinge.cloud/?utm_source=github_skills&utm_medium=readme&utm_campaign=skills_matrix)（mojinge.cloud）——把故事变成短剧：一句想法进来，一部能拍的剧本出去，分集剧情、人物 / 场景 / 道具资产、每集分镜提示词一次给齐；导入小说可走全流程改编（导入 → 故事中枢 → 分集大纲 → 改编剧本 → 分镜脚本）。按次付费，生成失败不扣费，邮箱即账号。

Made by the team behind [Mojinge](https://www.mojinge.cloud/?utm_source=github_skills&utm_medium=readme&utm_campaign=skills_matrix) — turn a story into a shootable screenplay: episode breakdowns, character/scene/prop assets, and per-shot prompts in one pass.

配套开源件 [ShotLock](https://github.com/nianjiang888/shotlock)：分镜脚本一致性校验引擎，十五条规则专抓角色漂移、越轴、语速超载，可作生成流程的卡口。
