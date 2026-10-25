# 热门行业研究与数据分析工具：搬迁及改造报告

核查日期：2026-10-25（北京时间）。目标账号：3416461284a-debug。

已通过GitHub网页创建10个公开Fork，分别核查`fork=true`、父仓库以及默认分支提交SHA；核查时10项均与上游相同。仅复制默认分支，保留该分支历史和GitHub Fork关系。此操作不等于迁移上游Issues、发布附件、外部数据服务、模型权重或部署应用，也不代表自动同步后续更新。

**评估依据与边界：**读取实时仓库元数据、README、选定官方文档及AKShare的一份采集源码。没有安装运行这些工具，没有复现缺陷，也没有实施下列建议。文档明示限制与针对行业分析用途的工程判断在各条中注明。Stars反映关注度，不能替代准确性或稳定性测试；近期推送也不等于稳定版本发布。

## 已搬迁目录

| 工具（你的Fork） | 上游Stars | 许可证 | 适用环节 | 改造优先级 |
|---|---:|---|---|---|
| [akshare](https://github.com/3416461284a-debug/akshare) | 23,061 | MIT | 中国行业、行情、宏观及公司财务数据采集 | 优先 |
| [FinanceDatabase](https://github.com/3416461284a-debug/FinanceDatabase) | 9,533 | MIT | 按国家、行业、资产类型筛选可比公司 | 优先 |
| [markitdown](https://github.com/3416461284a-debug/markitdown) | 191,993 | MIT | 把年报、行业报告和办公文档转成便于检索的文本 | 优先 |
| [duckdb](https://github.com/3416461284a-debug/duckdb) | 42,503 | MIT | 在个人电脑上用SQL分析CSV、Parquet与跨来源数据 | 优先 |
| [polars](https://github.com/3416461284a-debug/polars) | 40,186 | MIT | 高效清洗、聚合和处理多文件数据 | 第二步 |
| [statsmodels](https://github.com/3416461284a-debug/statsmodels) | 11,713 | BSD-3-Clause | 回归、时序建模、检验与统计推断 | 优先 |
| [metabase](https://github.com/3416461284a-debug/metabase) | 49,833 | AGPL / Commercial（分目录） | 面向非技术使用者的查询和业务看板 | 按需 |
| [superset](https://github.com/3416461284a-debug/superset) | 75,295 | Apache-2.0 | 复杂交互图表、SQL分析和团队看板 | 后续 |
| [jupyterlab](https://github.com/3416461284a-debug/jupyterlab) | 15,373 | BSD-3-Clause | 交互式研究、模型实验与过程留档 | 第二步 |
| [evidence](https://github.com/3416461284a-debug/evidence) | 7,057 | MIT | 用SQL和Markdown制作带说明文字的交互行业报告 | 第二步 |

## akshare

用途：中国行业、行情、宏观及公司财务数据采集。优先级：优先。

**缺陷、限制及风险：**官方 README 明确部分接口可能因不可控原因移除，数据还存在引用边界。已查看的东方财富行情代码直接依赖来源接口及字段映射；上游变化会影响采集。这是结构性依赖风险，本轮没有实测接口失败。

**可以怎么修改：**做统一数据适配层：配置超时、有限重试、缓存和提供方状态；校验列名、数据类型、日期跨度与缺失率；保留原始响应、采集时间、来源及版本。为行业代码、币种、单位、复权和财报可得日建立统一字典。

**改后如何验收：**故意制造超时/字段变化时应明确失败且保留最后成功数据；两次同口径采集可比较；报告可追溯到来源与采集时间。

依据：[来源1](https://github.com/akfamily/akshare/blob/main/README.md)；[来源2](https://github.com/akfamily/akshare/blob/main/akshare/stock_feature/stock_hist_em.py)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/akshare)；父仓库 akfamily/akshare；默认分支 main；核查时双方提交均为 `2ea08ff44512a9b0c008cd4ff77463b940959c7e`。上游最近推送 2026-10-23T23:47:22Z。

## FinanceDatabase

用途：按国家、行业、资产类型筛选可比公司。优先级：优先。

**缺陷、限制及风险：**README 明确本项目不提供实时基本面或股价。其市值字段示例为 Mega/Large 等分组，不能直接用于精确估值排序；多地上市记录还可能重复计算同一公司。

**可以怎么修改：**把它作为公司/证券基础目录，与经过授权的财务和行情源连接。使用主上市地筛选与稳定证券标识，增加申万/中证等分类映射、分类有效日期、实体合并规则和数据快照。

**改后如何验收：**行业同业名单可以复现；公司数与证券数明确分开；估值计算使用具体金额、币种、日期而非市值档位。

依据：[来源1](https://github.com/JerBouma/FinanceDatabase/blob/main/README.md)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/FinanceDatabase)；父仓库 JerBouma/FinanceDatabase；默认分支 main；核查时双方提交均为 `6b5a1ae19bc87eb96c702ca760828411f4f3f14b`。上游最近推送 2026-10-20T21:11:16Z。

## markitdown

用途：把年报、行业报告和办公文档转成便于检索的文本。优先级：优先。

**缺陷、限制及风险：**README 明确其目标是供文本分析工具消费，不能期待高保真版式转换。复杂表格、扫描件需要额外验证；OCR 插件若未提供 LLM 客户端可能跳过 OCR，云增强能力涉及额外服务。

**可以怎么修改：**按原生文字/扫描文档分流；先采用可用的本地解析路径，必要时配置 OCR。保留文件哈希、页码、坐标和原文；对金额、单位、合计、跨页表头做校验；加入人工复核队列，防止将解析失败当作空数据。

**改后如何验收：**同一套中文年报样本记录文本覆盖率、金额准确率、跨页表格准确率；每个提取指标都能返回原文页；缺 OCR 能力时明确提示。

依据：[来源1](https://github.com/microsoft/markitdown/blob/main/README.md)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/markitdown)；父仓库 microsoft/markitdown；默认分支 main；核查时双方提交均为 `7482c092d9c0074a89803c9fdb63a969e7fe17fc`。上游最近推送 2026-10-23T17:04:06Z。

## duckdb

用途：在个人电脑上用SQL分析CSV、Parquet与跨来源数据。优先级：优先。

**缺陷、限制及风险：**在进程内直接读写原生数据库时，并发模型有明确边界：多线程可写，但不同进程不能无协调直接共享写入。当前官方文档已介绍 Quack 远程协议及 DuckLake 等多进程方案，不能笼统声称不支持多进程。

**可以怎么修改：**个人工作流先用单个写入任务和事务队列，读分析用快照或只读连接；配置内存及临时磁盘，使用Parquet分区与列裁剪。多人部署再按需求评估官方远程方案及其具体版本。

**改后如何验收：**多个读取任务与一个写入任务可控；写冲突有清晰错误；大文件执行记录内存与磁盘，金额精度和空值处理通过样例检查。

依据：[来源1](https://duckdb.org/docs/2.0/connect/concurrency)；[来源2](https://github.com/duckdb/duckdb/blob/main/README.md)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/duckdb)；父仓库 duckdb/duckdb；默认分支 main；核查时双方提交均为 `1641475ef1db08ec063631ff6a8f08d9d6736ae7`。上游最近推送 2026-10-23T19:39:03Z。

## polars

用途：高效清洗、聚合和处理多文件数据。优先级：第二步。

**缺陷、限制及风险：**官方迁移文档说明其没有Pandas式索引/MultiIndex，类型和表达式语义也不同；旧脚本不能简单替换import后期待结果一致。README说明可对查询或部分查询流式处理，不代表任何操作都能无内存压力运行。

**可以怎么修改：**先做业务数据schema、日期时区和金额精度契约；使用lazy扫描和表达式；只在需要时转换到Pandas。为索引对齐、连接键、null/NaN和排序建立结果对照。

**改后如何验收：**与既有正确样本逐项比较行数、主键、金额及聚合结果；以目标数据量实测时间和峰值资源，不套用项目宣传速度。

依据：[来源1](https://docs.pola.rs/user-guide/migration/pandas/)；[来源2](https://github.com/pola-rs/polars/blob/main/README.md)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/polars)；父仓库 pola-rs/polars；默认分支 main；核查时双方提交均为 `d02c62175ad906f3c54cda7a0d917e6a72f73865`。上游最近推送 2026-10-24T16:57:59Z。

## statsmodels

用途：回归、时序建模、检验与统计推断。优先级：优先。

**缺陷、限制及风险：**官方文档明确：默认缺失值检查可能不启用；某些输入可静默产生NaN参数。秩亏设计矩阵可能不报错，接近共线会使结果不稳定，优化停止也不保证参数真正收敛。这些是官方列示陷阱，本轮未本机复现。

**可以怎么修改：**增加统一建模入口：缺失值用missing='raise'或事先显式处理；检查矩阵秩与条件数、常数项、残差和收敛标志；明确稳健/聚类标准误选择；输出样本与识别假设，不自动将相关当因果。

**改后如何验收：**注入缺失值和完全共线字段时能阻断或给出诊断；独立模型实例保存结果；报告列出样本量、变量定义、估计方法、标准误及敏感性分析。

依据：[来源1](https://www.statsmodels.org/stable/missing.html)；[来源2](https://www.statsmodels.org/stable/pitfalls.html)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/statsmodels)；父仓库 statsmodels/statsmodels；默认分支 main；核查时双方提交均为 `6ca2a285b4dac9ccf975cd4fa6e6083ea4f725ef`。上游最近推送 2026-10-24T22:57:58Z。

## metabase

用途：面向非技术使用者的查询和业务看板。优先级：按需。

**缺陷、限制及风险：**仓库包含AGPL开源部分和commercial许可的enterprise目录；GitHub元数据的NOASSERTION不能理解成无许可证。官方文档把行列权限列为Pro/Enterprise能力，并列出SQL查询、公开分享等权限边界。Fork不会使商业功能免费。

**可以怎么修改：**先按开源版能力设计个人看板；在数据层使用最小权限账号与受控视图，按身份和数据库连接方式验证隔离效果；补中文行业指标定义、日期及来源展示。商业代码与模型不混入自己的无条件开源许可。

**改后如何验收：**功能矩阵注明是否付费；不同身份分别验证可见数据、SQL结果及分享链接；不能只测图形查询界面就宣布权限安全。

依据：[来源1](https://github.com/metabase/metabase/blob/master/LICENSE.txt)；[来源2](https://www.metabase.com/docs/latest/permissions/row-and-column-security)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/metabase)；父仓库 metabase/metabase；默认分支 master；核查时双方提交均为 `1e53afdcadff2ef935702f0c438a2ffb8d44233c`。上游最近推送 2026-10-25T03:43:06Z。

## superset

用途：复杂交互图表、SQL分析和团队看板。优先级：后续。

**缺陷、限制及风险：**官方安装文档说明不正式支持Windows，且不推荐其Docker Compose构造直接用于生产高可用场景。它能展示和探索数据，但不会自动提供行业指标口径或保证来源数据质量。

**可以怎么修改：**Windows个人试用采用适合的Linux/WSL容器环境并固定发布版；团队环境按官方架构维护元数据库、缓存与任务服务。预置行业数据集、指标字典、角色与导出模板。

**改后如何验收：**从干净环境可复现启动；数据库与驱动连接通过；中文字体、时区、权限和图表导出用真实样本验证。

依据：[来源1](https://superset.apache.org/admin-docs/installation/docker-compose/)；[来源2](https://github.com/apache/superset/blob/master/README.md)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/superset)；父仓库 apache/superset；默认分支 master；核查时双方提交均为 `f829175e946de36305b16e3f26084c2ff71301e8`。上游最近推送 2026-10-25T02:59:54Z。

## jupyterlab

用途：交互式研究、模型实验与过程留档。优先级：第二步。

**缺陷、限制及风险：**扩展文档明确扩展管理器不保证扩展与当前JupyterLab版本兼容。Notebook工作流还可能保留乱序执行状态；后者是使用风险判断，不是本轮发现的项目Bug。

**可以怎么修改：**固定环境、内核和扩展版本；将通用取数清洗逻辑抽出为模块；研究模板包含数据来源、假设与口径；在发布结果前用新内核顺序执行全部单元格并记录数据版本。

**改后如何验收：**另一台干净环境或重建环境可从头执行；清空内核后结果一致；输出含依赖版本与随机种子。

依据：[来源1](https://jupyterlab.readthedocs.io/en/stable/user/extensions.html)；[来源2](https://github.com/jupyterlab/jupyterlab/blob/main/README.md)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/jupyterlab)；父仓库 jupyterlab/jupyterlab；默认分支 main；核查时双方提交均为 `196379a9b1bcafe3fdf68f52ac6f61ba6a907232`。上游最近推送 2026-10-23T15:10:33Z。

## evidence

用途：用SQL和Markdown制作带说明文字的交互行业报告。优先级：第二步。

**缺陷、限制及风险：**上游定位代码式报告工具，使用者需要掌握SQL/Markdown及构建发布流程。公开静态报告所包含的数据和实时更新行为需要按实际部署审查；不能把Studio的认证和发布能力一概视作本地开源构建已经具备。

**可以怎么修改：**制作中文行业报告模板，统一单位和同比/环比定义；建立数据更新、校验和构建流程；发布前检查实际产物中包含哪些明细数据，内部报告配置合适的访问控制。

**改后如何验收：**报告每个数字显示统计期与来源；固定数据快照可重建；过期数据、失败构建和不该公开的数据在发布检查中被识别。

依据：[来源1](https://github.com/evidence-dev/evidence/blob/main/README.md)；[来源2](https://docs.evidence.dev/publishing)。

搬迁证据：[你的Fork](https://github.com/3416461284a-debug/evidence)；父仓库 evidence-dev/evidence；默认分支 main；核查时双方提交均为 `505913ca3e03391fd4c1d06c1d2aa33653cdb27f`。上游最近推送 2026-10-23T14:42:41Z。

## 建议优先形成的工作流

1. AKShare + FinanceDatabase：获得行业指标和可比公司名单，保留来源、版本及统计口径。
2. MarkItDown：提取报告内容，给表格数字加原文定位和人工复核。
3. DuckDB + Polars：建立本地可复现清洗、聚合与数据质量检查。
4. statsmodels：做带诊断的统计分析，明确推断条件。
5. Evidence或Metabase：按需要选择报告或查询看板；Superset留待复杂团队需求。

优先在外围建立适配器、模板和检查层，再考虑改动这些成熟项目的核心；这样更容易合并上游更新。上述为建议，不是已经完成的开发。

## 与新增100个项目的关系

另行筛选的100个低热度项目见《低热度100项目筛选与改造清单》，实际Stars为35–4,945。GitHub对新增Fork返回HTTP 422 / was submitted too quickly，因此这100个项目不能计作已经搬迁；两批状态分开记录。
