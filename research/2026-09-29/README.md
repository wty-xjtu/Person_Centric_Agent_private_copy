# Personal Agent 完整调研 CSV

调研截止日期：2026-09-29。文献和产品分表保留其完整字段，没有裁剪摘要或证据链接。

| 文件 | 条目数 | 内容 |
| --- | ---: | --- |
| [literature_catalog.csv](literature_catalog.csv) | 1,814 | 文献候选、摘要、作者、原始链接、相关性说明及检索信息 |
| [product_catalog.csv](product_catalog.csv) | 79 | 产品/产品族的记忆、个性化、主动机制、动作、用户控制、状态与官方来源 |

## 文献字段与范围

`id` 为候选标识；`grade` 为相关性档位；`year` / `date` 为检索元数据中的年份与日期；`title`、`url`、`abstract`、`venue`、`authors` 为文献信息；`relevance_note` 说明为何与 Personal Agent 相关；`search_term` 和 `metadata` 保留检索信息。

T1 为近 12 个月核心相关，T2 为更早的核心/奠基材料，T3 为直接关联的方法与应用，T4–T5 为邻近背景。它们不是论文质量评分。分布：T1 412、T2 196、T3 186、T4 641、T5 379。

本表为检索与初筛候选，**不表示 1,814 篇均已全文精读或核验所有实验结果**。同题名版本已做部分合并，改题名版本仍可能重复；正式引用前应核验论文元数据与摘要。

## 产品字段与范围

`id`、`name`、`category` 标识产品族与主类别；`status` 记录核查时状态；`evidence_level` 为材料类型；`user_evidence_memory`、`personalization`、`proactivity`、`actions`、`user_controls`、`availability_business_model` 等字段分别记录公开材料中的记忆、个性化、主动机制和控制方式。

D＝官方使用/支持/开发文档，P＝官方产品/发布页（含开发者应用商店条目），U＝线索或证据不足。32 项 D、40 项 P、7 项 U，共引用 143 个不同官方 URLs。所有产品均为公开资料研究，`hands_on_tested=False`。

## 文件使用

CSV 按标准 CSV 引号规则保存，摘要可含逗号和换行，行数应以 CSV 解析器统计，不能按文本换行数统计。产品列表字段以 ` | ` 分隔；文献列表字段保留为标准 CSV 字段。
