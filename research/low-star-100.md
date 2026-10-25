# 100个低热度实用与实验项目

核查日期：2026-10-25。账号：3416461284a-debug。

从135个定向候选中筛选100个；实际35–4,945 Stars，均未归档、2025-01-01后有推送、具明确SPDX许可证，已读取README/文档。没有安装或实测；风险包括上游明示限制和用途分析，不当作已复现Bug。

**这100个项目的Fork尚未完成。GitHub网页多次返回HTTP 422 / was submitted too quickly。下文仅列上游及创建Fork入口。已成功的10个热门Fork见[热门工具报告](popular-10.md)。**

代码许可不自动覆盖数据服务、模型权重或付费API。近期推送和Stars也不代表稳定性。

## 宏观与行业数据

### 1. [mortada/fredapi](https://github.com/mortada/fredapi) · 1666 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-01-28。
- 用途：读取FRED/ALFRED宏观数据与历史修订版本。
- 风险/限制：需要FRED密钥；若只取最新值，历史研究可能混入事后修订。
- 建议修改：同时保存观测期、发布时间和数据版本；增加缓存与重试。
- [README/文档依据](https://raw.githubusercontent.com/mortada/fredapi/master/README.md) · [创建Fork（待完成）](https://github.com/mortada/fredapi/fork)。

### 2. [7astro7/full_fred](https://github.com/7astro7/full_fred) · 115 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-06-05。
- 用途：覆盖FRED多类接口的完整客户端。
- 风险/限制：接口多，调用配额与服务变化需要单独处理。
- 建议修改：增加按系列增量更新、频率统一和错误日志。
- [README/文档依据](https://raw.githubusercontent.com/7astro7/full_fred/master/README.md) · [创建Fork（待完成）](https://github.com/7astro7/full_fred/fork)。

### 3. [tradingeconomics/tradingeconomics-python](https://github.com/tradingeconomics/tradingeconomics-python) · 135 Stars

- 实用候选，仍需实测；GPL-3.0；最近推送 2026-10-08。
- 用途：取得经济日历、宏观指标与市场数据。
- 风险/限制：客户端开源不代表数据订阅免费；依赖服务凭据。
- 建议修改：把免费/付费接口分开配置，增加配额预算和本地快照。
- [README/文档依据](https://raw.githubusercontent.com/tradingeconomics/tradingeconomics-python/main/README.md) · [创建Fork（待完成）](https://github.com/tradingeconomics/tradingeconomics-python/fork)。

### 4. [ShichenXie/pedquant](https://github.com/ShichenXie/pedquant) · 69 Stars

- 实用候选，仍需实测；GPL-3.0；最近推送 2026-10-14。
- 用途：在R中采集国家统计局、FRED等公共数据。
- 风险/限制：跨国家指标的单位、频率和统计口径需要对齐。
- 建议修改：建立中文指标字典及单位、频率、修订时间字段。
- [README/文档依据](https://raw.githubusercontent.com/ShichenXie/pedquant/master/README.md) · [创建Fork（待完成）](https://github.com/ShichenXie/pedquant/fork)。

### 5. [tgherzog/wbgapi](https://github.com/tgherzog/wbgapi) · 178 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-02-27。
- 用途：批量取得世界银行跨国指标。
- 风险/限制：缺失值、国家集合与指标口径影响跨国比较。
- 建议修改：固定国家名单和数据快照，导出缺失率与指标元数据。
- [README/文档依据](https://raw.githubusercontent.com/tgherzog/wbgapi/master/README.md) · [创建Fork（待完成）](https://github.com/tgherzog/wbgapi/fork)。

### 6. [ondata/opensdmx](https://github.com/ondata/opensdmx) · 55 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-10-24。
- 用途：用统一CLI查询Eurostat、OECD等SDMX接口。
- 风险/限制：上游明确标注实验性；不同提供方的维度并不一致。
- 建议修改：增加提供方契约测试、维度查询和中文示例。
- [README/文档依据](https://raw.githubusercontent.com/ondata/opensdmx/main/README.md) · [创建Fork（待完成）](https://github.com/ondata/opensdmx/fork)。

### 7. [portfolioplus/pystockfilter](https://github.com/portfolioplus/pystockfilter) · 35 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-03-18。
- 用途：按财务与技术指标筛选股票。
- 风险/限制：依赖外部数据源，筛选结果不证明策略有效。
- 建议修改：加入数据日期、财报可得日和无未来信息的回测。
- [README/文档依据](https://raw.githubusercontent.com/portfolioplus/pystockfilter/master/README.md) · [创建Fork（待完成）](https://github.com/portfolioplus/pystockfilter/fork)。

### 8. [mv/fundamentus-api](https://github.com/mv/fundamentus-api) · 111 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-10-06。
- 用途：抓取巴西上市公司基本面数据。
- 风险/限制：市场覆盖聚焦巴西；依赖Fundamentus页面结构。
- 建议修改：以适配器扩展其他市场，并检查字段和财报期变化。
- [README/文档依据](https://raw.githubusercontent.com/mv/fundamentus-api/main/README.md) · [创建Fork（待完成）](https://github.com/mv/fundamentus-api/fork)。

### 9. [zmcx16/Norn-StockScreener](https://github.com/zmcx16/Norn-StockScreener) · 85 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-25。
- 用途：美股筛选、行业对比和财务风险指标。
- 风险/限制：面向美股的规则不能直接推广到A股。
- 建议修改：参数化财务口径和市场规则，补中文解释与来源日期。
- [README/文档依据](https://raw.githubusercontent.com/zmcx16/Norn-StockScreener/master/README.md) · [创建Fork（待完成）](https://github.com/zmcx16/Norn-StockScreener/fork)。

## 计量与因果推断

### 10. [bashtage/linearmodels](https://github.com/bashtage/linearmodels) · 1077 Stars

- 实用候选，仍需实测；NCSA；最近推送 2026-10-22。
- 用途：面板回归、工具变量和资产定价估计。
- 风险/限制：README列示面板固定效应最多双向；推断仍依赖模型假设。
- 建议修改：封装实体/时间索引、聚类标准误和识别假设检查。
- [README/文档依据](https://raw.githubusercontent.com/bashtage/linearmodels/main/README.md) · [创建Fork（待完成）](https://github.com/bashtage/linearmodels/fork)。

### 11. [py-econometrics/pyfixest](https://github.com/py-econometrics/pyfixest) · 358 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：高维固定效应回归与计量估计。
- 风险/限制：便捷估计不能替代政策识别和样本诊断。
- 建议修改：增加事件研究模板、聚类说明及预趋势检查。
- [README/文档依据](https://raw.githubusercontent.com/py-econometrics/pyfixest/master/README.md) · [创建Fork（待完成）](https://github.com/py-econometrics/pyfixest/fork)。

### 12. [QuantEcon/QuantEcon.py](https://github.com/QuantEcon/QuantEcon.py) · 2412 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：马尔可夫链、动态规划和经济模型求解。
- 风险/限制：属于研究库，仍需要经济模型和参数设定。
- 建议修改：封装行业情景模板、参数校准和敏感性分析。
- [README/文档依据](https://raw.githubusercontent.com/QuantEcon/QuantEcon.py/main/README.md) · [创建Fork（待完成）](https://github.com/QuantEcon/QuantEcon.py/fork)。

### 13. [econ-ark/HARK](https://github.com/econ-ark/HARK) · 403 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-12。
- 用途：异质性家庭/主体经济行为建模。
- 风险/限制：校准、状态空间和数值收敛需要专业判断。
- 建议修改：保存校准依据，添加网格收敛和情景对比报告。
- [README/文档依据](https://raw.githubusercontent.com/econ-ark/HARK/main/README.md) · [创建Fork（待完成）](https://github.com/econ-ark/HARK/fork)。

### 14. [google/CausalImpact](https://github.com/google/CausalImpact) · 1865 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-03-31。
- 用途：用贝叶斯时序模型评估干预效果。
- 风险/限制：上游强调非实验因果分析需要有效假设；对照序列选择关键。
- 建议修改：增加安慰剂检验、干预前拟合和不受干预对照说明。
- [README/文档依据](https://raw.githubusercontent.com/google/CausalImpact/master/README.md) · [创建Fork（待完成）](https://github.com/google/CausalImpact/fork)。

### 15. [pymc-labs/CausalPy](https://github.com/pymc-labs/CausalPy) · 1209 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-25。
- 用途：准实验设计的因果分析工作流。
- 风险/限制：模型结果依赖准实验假设和先验设定。
- 建议修改：加入中文设计向导、先验敏感性与诊断报告。
- [README/文档依据](https://raw.githubusercontent.com/pymc-labs/CausalPy/main/README.md) · [创建Fork（待完成）](https://github.com/pymc-labs/CausalPy/fork)。

### 16. [BiomedSciAI/causallib](https://github.com/BiomedSciAI/causallib) · 834 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-05-26。
- 用途：对观测数据估计处理效应并评估模型。
- 风险/限制：无法自动排除未观测混杂或缺乏共同支持的问题。
- 建议修改：强制输出协变量平衡、重叠和敏感性诊断。
- [README/文档依据](https://raw.githubusercontent.com/BiomedSciAI/causallib/master/README.md) · [创建Fork（待完成）](https://github.com/BiomedSciAI/causallib/fork)。

### 17. [py-why/causaltune](https://github.com/py-why/causaltune) · 242 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-07-19。
- 用途：自动选择和调优因果估计器。
- 风险/限制：自动调参不能自动证明因果识别。
- 建议修改：限制搜索预算，区分识别假设与模型评分。
- [README/文档依据](https://raw.githubusercontent.com/py-why/causaltune/main/README.md) · [创建Fork（待完成）](https://github.com/py-why/causaltune/fork)。

### 18. [FenTechSolutions/CausalDiscoveryToolbox](https://github.com/FenTechSolutions/CausalDiscoveryToolbox) · 1244 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-10-13。
- 用途：从数据探索候选因果图和依赖关系。
- 风险/限制：同时依赖Python、R和部分深度学习组件；发现的图需要验证。
- 建议修改：做容器化依赖和已知图基准，允许录入领域约束。
- [README/文档依据](https://raw.githubusercontent.com/FenTechSolutions/CausalDiscoveryToolbox/master/README.md) · [创建Fork（待完成）](https://github.com/FenTechSolutions/CausalDiscoveryToolbox/fork)。

### 19. [ycroissant/plm](https://github.com/ycroissant/plm) · 65 Stars

- 实用候选，仍需实测；GPL-2.0；最近推送 2026-06-25。
- 用途：R面板数据估计、检验与稳健协方差。
- 风险/限制：模型选择与非平衡面板处理需要判断。
- 建议修改：统一缺失样本统计、模型对照和稳健性表格。
- [README/文档依据](https://raw.githubusercontent.com/ycroissant/plm/main/README.md) · [创建Fork（待完成）](https://github.com/ycroissant/plm/fork)。

### 20. [Nosferican/Econometrics.jl](https://github.com/Nosferican/Econometrics.jl) · 79 Stars

- 实用候选，仍需实测；ISC；最近推送 2025-03-27。
- 用途：在Julia中做计量估计。
- 风险/限制：Julia生态与现有Python/Excel工作流存在衔接成本。
- 建议修改：提供CSV输入、可复现实例及跨软件估计对照。
- [README/文档依据](https://raw.githubusercontent.com/Nosferican/Econometrics.jl/master/README.md) · [创建Fork（待完成）](https://github.com/Nosferican/Econometrics.jl/fork)。

### 21. [djvanderlaan/reclin2](https://github.com/djvanderlaan/reclin2) · 53 Stars

- 实用候选，仍需实测；GPL-3.0；最近推送 2026-01-08。
- 用途：在R中做记录匹配与去重。
- 风险/限制：README说明不向后兼容reclin，且功能并非完全对应。
- 建议修改：增加迁移说明、候选对抽样和人工复核界面。
- [README/文档依据](https://raw.githubusercontent.com/djvanderlaan/reclin2/master/README.md) · [创建Fork（待完成）](https://github.com/djvanderlaan/reclin2/fork)。

## 文档与表格提取

### 22. [xavctn/img2table](https://github.com/xavctn/img2table) · 901 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-07-12。
- 用途：提取PDF和图片里的表格。
- 风险/限制：README说明OpenCV检测有局限；Tesseract需单独安装。
- 建议修改：按扫描/原生PDF分流，给单元格加置信度并检查合计。
- [README/文档依据](https://raw.githubusercontent.com/xavctn/img2table/main/README.md) · [创建Fork（待完成）](https://github.com/xavctn/img2table/fork)。

### 23. [galkahana/pdf-text-extraction](https://github.com/galkahana/pdf-text-extraction) · 81 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2026-08-14。
- 用途：用CLI提取PDF文本及实验性表格。
- 风险/限制：上游明确表格提取仍为实验功能。
- 建议修改：建立中文年报样本集，保留页码坐标和失败页。
- [README/文档依据](https://raw.githubusercontent.com/galkahana/pdf-text-extraction/main/README.md) · [创建Fork（待完成）](https://github.com/galkahana/pdf-text-extraction/fork)。

### 24. [BobLd/tabula-sharp](https://github.com/BobLd/tabula-sharp) · 217 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-05-04。
- 用途：在.NET应用内提取PDF表格。
- 风险/限制：主要依赖PDF文字与布局；扫描文档需要额外OCR流程。
- 建议修改：加入扫描识别、OCR适配器及跨页表头合并。
- [README/文档依据](https://raw.githubusercontent.com/BobLd/tabula-sharp/master/README.md) · [创建Fork（待完成）](https://github.com/BobLd/tabula-sharp/fork)。

### 25. [ispras/dedoc](https://github.com/ispras/dedoc) · 736 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-09-29。
- 用途：把文档结构、文本、表格和元数据统一输出。
- 风险/限制：复杂文档结构提取需要针对样本验证，依赖链较多。
- 建议修改：给输出保留页码与原文位置，做中文文档类型回归集。
- [README/文档依据](https://raw.githubusercontent.com/ispras/dedoc/master/README.md) · [创建Fork（待完成）](https://github.com/ispras/dedoc/fork)。

### 26. [drmingler/docling-api](https://github.com/drmingler/docling-api) · 1665 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-08-04。
- 用途：把Docling包装成可部署文档转换服务。
- 风险/限制：新增服务层带来上传、超时和并发管理需求。
- 建议修改：加文件大小限制、任务队列、缓存和转换版本记录。
- [README/文档依据](https://raw.githubusercontent.com/drmingler/docling-api/main/README.md) · [创建Fork（待完成）](https://github.com/drmingler/docling-api/fork)。

### 27. [genieincodebottle/parsemypdf](https://github.com/genieincodebottle/parsemypdf) · 197 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-09-07。
- 用途：用同一组样例比较多种PDF解析器。
- 风险/限制：README明确没有真值评分、未展示成本，视觉输出可能波动。
- 建议修改：补人工标注真值、单页成本和表格准确率评估。
- [README/文档依据](https://raw.githubusercontent.com/genieincodebottle/parsemypdf/main/README.md) · [创建Fork（待完成）](https://github.com/genieincodebottle/parsemypdf/fork)。

### 28. [coregx/gxpdf](https://github.com/coregx/gxpdf) · 53 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-22。
- 用途：在Go中解析、提表并生成PDF。
- 风险/限制：需要较新Go环境；中文生成还需合适字体。
- 建议修改：固定工具链与中文字体，测试合并单元格及金额符号。
- [README/文档依据](https://raw.githubusercontent.com/coregx/gxpdf/main/README.md) · [创建Fork（待完成）](https://github.com/coregx/gxpdf/fork)。

## 采集与实体匹配

### 29. [teaguesterling/duckdb_webbed](https://github.com/teaguesterling/duckdb_webbed) · 77 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：直接用SQL解析HTML/XML和网页表格。
- 风险/限制：网页字段变化及扩展版本适配需要验证。
- 建议修改：固定扩展版本，保存原网页及XPath/字段契约。
- [README/文档依据](https://raw.githubusercontent.com/teaguesterling/duckdb_webbed/main/README.md) · [创建Fork（待完成）](https://github.com/teaguesterling/duckdb_webbed/fork)。

### 30. [ispras/web-scraper-chrome-extension](https://github.com/ispras/web-scraper-chrome-extension) · 289 Stars

- 实用候选，仍需实测；LGPL-3.0；最近推送 2026-04-02。
- 用途：通过浏览器站点地图采集网页数据。
- 风险/限制：页面DOM或登录状态变化可能使既有采集规则失效。
- 建议修改：增加选择器失效提示、去重和断点记录。
- [README/文档依据](https://raw.githubusercontent.com/ispras/web-scraper-chrome-extension/master/README.md) · [创建Fork（待完成）](https://github.com/ispras/web-scraper-chrome-extension/fork)。

### 31. [paulrobello/par_scrape](https://github.com/paulrobello/par_scrape) · 220 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-07-12。
- 用途：浏览器抓取结合AI结构化提取。
- 风险/限制：README记录非OpenAI提供方效果不稳定；调用有成本。
- 建议修改：保存原网页，做JSON字段验证、成本记录和提供方对照。
- [README/文档依据](https://raw.githubusercontent.com/paulrobello/par_scrape/main/README.md) · [创建Fork（待完成）](https://github.com/paulrobello/par_scrape/fork)。

### 32. [helgeho/ArchiveSpark](https://github.com/helgeho/ArchiveSpark) · 164 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-10-08。
- 用途：用Spark分析历史网页档案集合。
- 风险/限制：Spark和档案格式增加个人电脑部署成本。
- 建议修改：提供小数据本地示例，按域名/时间分区并保存溯源。
- [README/文档依据](https://raw.githubusercontent.com/helgeho/ArchiveSpark/master/README.md) · [创建Fork（待完成）](https://github.com/helgeho/ArchiveSpark/fork)。

### 33. [dedupeio/dedupe](https://github.com/dedupeio/dedupe) · 4521 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-07-29。
- 用途：识别名称地址近似的重复公司或客户记录。
- 风险/限制：训练标注和阈值会影响误合并；需要审核。
- 建议修改：增加人工标注样本、误合并指标与可撤销合并日志。
- [README/文档依据](https://raw.githubusercontent.com/dedupeio/dedupe/main/README.md) · [创建Fork（待完成）](https://github.com/dedupeio/dedupe/fork)。

### 34. [moj-analytical-services/splink](https://github.com/moj-analytical-services/splink) · 2532 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-22。
- 用途：用SQL后端做大规模概率记录链接。
- 风险/限制：版本5已发布，旧例子需要迁移；匹配仍需阈值验证。
- 建议修改：固定版本，输出匹配解释及人工复核队列。
- [README/文档依据](https://raw.githubusercontent.com/moj-analytical-services/splink/master/README.md) · [创建Fork（待完成）](https://github.com/moj-analytical-services/splink/fork)。

### 35. [alex9smith/gdelt-doc-api](https://github.com/alex9smith/gdelt-doc-api) · 232 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-04-22。
- 用途：检索新闻并分析行业媒体热度。
- 风险/限制：README定位小规模新闻分析；媒体覆盖不能代表真实市场规模。
- 建议修改：记录检索窗口、语言和媒体来源，增加去重与偏差说明。
- [README/文档依据](https://raw.githubusercontent.com/alex9smith/gdelt-doc-api/main/README.md) · [创建Fork（待完成）](https://github.com/alex9smith/gdelt-doc-api/fork)。

### 36. [vaneseltine/nominally](https://github.com/vaneseltine/nominally) · 41 Stars

- 实用候选，仍需实测；AGPL-3.0；最近推送 2025-09-03。
- 用途：把姓名拆成用于记录匹配的结构字段。
- 风险/限制：姓名结构与语言相关；中文人名适配需要专门验证。
- 建议修改：建立中英多语言标注集，并为不确定拆分保留原文。
- [README/文档依据](https://raw.githubusercontent.com/vaneseltine/nominally/master/README.md) · [创建Fork（待完成）](https://github.com/vaneseltine/nominally/fork)。

## 数据质量与清洗

### 37. [pyjanitor-devs/pyjanitor](https://github.com/pyjanitor-devs/pyjanitor) · 1499 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：以链式API清洗、整理DataFrame。
- 风险/限制：自动清洗步骤可能改变字段或丢失记录。
- 建议修改：给每步保存输入输出行数、字段变化和数据校验。
- [README/文档依据](https://raw.githubusercontent.com/pyjanitor-devs/pyjanitor/dev/README.md) · [创建Fork（待完成）](https://github.com/pyjanitor-devs/pyjanitor/fork)。

### 38. [akanz1/klib](https://github.com/akanz1/klib) · 523 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-23。
- 用途：快速清洗数据并生成探索图。
- 风险/限制：类型压缩、删列等便捷操作需确认业务含义。
- 建议修改：默认仅预览变更，输出清洗前后差异和回滚文件。
- [README/文档依据](https://raw.githubusercontent.com/akanz1/klib/main/README.md) · [创建Fork（待完成）](https://github.com/akanz1/klib/fork)。

### 39. [posit-dev/pointblank](https://github.com/posit-dev/pointblank) · 496 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-25。
- 用途：以可读规则验证和监测数据质量。
- 风险/限制：规则仍需人工定义；通过规则不代表全部业务正确。
- 建议修改：加入行业模板、严重度分级和异常样本导出。
- [README/文档依据](https://raw.githubusercontent.com/posit-dev/pointblank/main/README.md) · [创建Fork（待完成）](https://github.com/posit-dev/pointblank/fork)。

### 40. [awslabs/deequ](https://github.com/awslabs/deequ) · 3656 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-20。
- 用途：基于Spark给大数据定义质量约束。
- 风险/限制：Spark依赖较重，规则和基线仍需配置。
- 建议修改：提供行业约束模板与增量质量趋势，限制扫描成本。
- [README/文档依据](https://raw.githubusercontent.com/awslabs/deequ/master/README.md) · [创建Fork（待完成）](https://github.com/awslabs/deequ/fork)。

### 41. [datavane/datavines](https://github.com/datavane/datavines) · 766 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-07-27。
- 用途：整合元数据和数据质量检查。
- 风险/限制：平台化运行需维护连接器、服务与任务环境。
- 建议修改：做轻量单机配置，优先接入常用数据库并记录失败原因。
- [README/文档依据](https://raw.githubusercontent.com/datavane/datavines/dev/README.md) · [创建Fork（待完成）](https://github.com/datavane/datavines/fork)。

### 42. [WeBankFinTech/Qualitis](https://github.com/WeBankFinTech/Qualitis) · 771 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-04-02。
- 用途：建立数据质量规则、执行检查和通知管理。
- 风险/限制：平台组件与企业环境配置增加部署成本。
- 建议修改：提供最小部署路径、中文行业规则和可复现演示数据。
- [README/文档依据](https://raw.githubusercontent.com/WeBankFinTech/Qualitis/master/README.md) · [创建Fork（待完成）](https://github.com/WeBankFinTech/Qualitis/fork)。

### 43. [datacleaner/DataCleaner](https://github.com/datacleaner/DataCleaner) · 649 Stars

- 实用候选，仍需实测；LGPL-3.0；最近推送 2026-07-27。
- 用途：用桌面/平台方式发现和清理脏数据。
- 风险/限制：Java生态和连接器适配需要维护。
- 建议修改：固定运行环境，提供可审计清洗流程及数据来源记录。
- [README/文档依据](https://raw.githubusercontent.com/datacleaner/DataCleaner/main/README.md) · [创建Fork（待完成）](https://github.com/datacleaner/DataCleaner/fork)。

### 44. [capitalone/datacompy](https://github.com/capitalone/datacompy) · 664 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-21。
- 用途：比较Pandas、Polars、Spark等表格差异。
- 风险/限制：需要正确主键与数值容差，否则差异难解释。
- 建议修改：默认检查键唯一性，分开输出新增、删除、数值及口径变化。
- [README/文档依据](https://raw.githubusercontent.com/capitalone/datacompy/main/README.md) · [创建Fork（待完成）](https://github.com/capitalone/datacompy/fork)。

### 45. [capitalone/DataProfiler](https://github.com/capitalone/DataProfiler) · 1595 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-09-14。
- 用途：自动统计字段、识别模式与数据实体。
- 风险/限制：自动识别结果需要校验；大数据扫描有开销。
- 建议修改：增加抽样策略、中文实体样本和敏感字段脱敏报告。
- [README/文档依据](https://raw.githubusercontent.com/capitalone/DataProfiler/main/README.md) · [创建Fork（待完成）](https://github.com/capitalone/DataProfiler/fork)。

### 46. [unionai-oss/pandera](https://github.com/unionai-oss/pandera) · 4497 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-25。
- 用途：对DataFrame施加类型与统计约束。
- 风险/限制：数据契约需自己编写，统计检查有参数选择。
- 建议修改：封装行业schema模板，区分警告和阻断，导出失败行。
- [README/文档依据](https://raw.githubusercontent.com/unionai-oss/pandera/main/README.md) · [创建Fork（待完成）](https://github.com/unionai-oss/pandera/fork)。

### 47. [Data-Centric-AI-Community/fg-data-quality](https://github.com/Data-Centric-AI-Community/fg-data-quality) · 455 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-04-23。
- 用途：一行代码进行数据质量初检。
- 风险/限制：通用启发式不能覆盖行业业务规则。
- 建议修改：把自动发现的问题转成人工确认后的持久质量规则。
- [README/文档依据](https://raw.githubusercontent.com/Data-Centric-AI-Community/fg-data-quality/master/README.md) · [创建Fork（待完成）](https://github.com/Data-Centric-AI-Community/fg-data-quality/fork)。

## 探索与统计

### 48. [MaxHalford/prince](https://github.com/MaxHalford/prince) · 1486 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：对混合变量做PCA、对应分析等多元探索。
- 风险/限制：成分解释、缩放和类别编码会影响结论。
- 建议修改：输出贡献率、变量贡献和标准化选择说明。
- [README/文档依据](https://raw.githubusercontent.com/MaxHalford/prince/main/README.md) · [创建Fork（待完成）](https://github.com/MaxHalford/prince/fork)。

### 49. [pysal/esda](https://github.com/pysal/esda) · 261 Stars

- 实用候选，仍需实测；BSD-3-Clause；最近推送 2026-10-15。
- 用途：计算空间自相关并分析区域聚集。
- 风险/限制：空间权重矩阵的选择影响统计结果。
- 建议修改：记录权重构造、置换次数和多重检验处理。
- [README/文档依据](https://raw.githubusercontent.com/pysal/esda/main/README.md) · [创建Fork（待完成）](https://github.com/pysal/esda/fork)。

### 50. [pysal/giddy](https://github.com/pysal/giddy) · 76 Stars

- 实用候选，仍需实测；BSD-3-Clause；最近推送 2026-10-15。
- 用途：分析地区分布与空间时间动态。
- 风险/限制：区域划分、时间间隔和缺失地区影响可比性。
- 建议修改：固定区域版本和时间口径，补样本覆盖检查。
- [README/文档依据](https://raw.githubusercontent.com/pysal/giddy/main/README.md) · [创建Fork（待完成）](https://github.com/pysal/giddy/fork)。

### 51. [pysal/mgwr](https://github.com/pysal/mgwr) · 433 Stars

- 实用候选，仍需实测；BSD-3-Clause；最近推送 2026-10-14。
- 用途：估计多尺度地理加权回归。
- 风险/限制：带宽选择、局部共线性与计算量需评估。
- 建议修改：报告带宽与诊断，比较全局回归并限制小样本解释。
- [README/文档依据](https://raw.githubusercontent.com/pysal/mgwr/main/README.md) · [创建Fork（待完成）](https://github.com/pysal/mgwr/fork)。

### 52. [pysal/segregation](https://github.com/pysal/segregation) · 122 Stars

- 实用候选，仍需实测；BSD-3-Clause；最近推送 2026-10-13。
- 用途：计算城市与群体隔离指标。
- 风险/限制：指标易受空间聚合和群体定义影响。
- 建议修改：输出多尺度对照、置信区间和指标选择理由。
- [README/文档依据](https://raw.githubusercontent.com/pysal/segregation/main/README.md) · [创建Fork（待完成）](https://github.com/pysal/segregation/fork)。

### 53. [josecamachop/MEDA-Toolbox](https://github.com/josecamachop/MEDA-Toolbox) · 36 Stars

- 实用候选，仍需实测；GPL-3.0；最近推送 2026-10-14。
- 用途：在Matlab中做多元探索和实验数据分析。
- 风险/限制：需要Matlab环境，移植到常用Python工作流有成本。
- 建议修改：先做算法与示例对照，再封装批量输入和导出。
- [README/文档依据](https://raw.githubusercontent.com/josecamachop/MEDA-Toolbox/master/README.md) · [创建Fork（待完成）](https://github.com/josecamachop/MEDA-Toolbox/fork)。

### 54. [fbdesignpro/sweetviz](https://github.com/fbdesignpro/sweetviz) · 3131 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-04-11。
- 用途：快速比较数据集、目标变量与关联。
- 风险/限制：EDA图和相关性不能自动给出因果解释。
- 建议修改：对大表做可复现抽样，增加中文变量说明和漂移对照。
- [README/文档依据](https://raw.githubusercontent.com/fbdesignpro/sweetviz/master/README.md) · [创建Fork（待完成）](https://github.com/fbdesignpro/sweetviz/fork)。

## 预测与实验模型

### 55. [Nixtla/statsforecast](https://github.com/Nixtla/statsforecast) · 4945 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-22。
- 用途：快速运行ARIMA、ETS等统计预测基线。
- 风险/限制：没有天然理解行业结构变化；仍需回测选择模型。
- 建议修改：加滚动回测、预测区间与朴素基线对照。
- [README/文档依据](https://raw.githubusercontent.com/Nixtla/statsforecast/main/README.md) · [创建Fork（待完成）](https://github.com/Nixtla/statsforecast/fork)。

### 56. [Nixtla/hierarchicalforecast](https://github.com/Nixtla/hierarchicalforecast) · 765 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-19。
- 用途：让公司/区域/品类分层预测总分一致。
- 风险/限制：需要正确的层级结构与预测误差估计。
- 建议修改：校验层级矩阵，报告各层误差及协调前后变化。
- [README/文档依据](https://raw.githubusercontent.com/Nixtla/hierarchicalforecast/main/README.md) · [创建Fork（待完成）](https://github.com/Nixtla/hierarchicalforecast/fork)。

### 57. [Nixtla/mlforecast](https://github.com/Nixtla/mlforecast) · 1296 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-23。
- 用途：用机器学习进行多序列预测。
- 风险/限制：滞后和外生变量处理不当可能引入未来信息。
- 建议修改：按时间切分训练集，检查特征可得时间并保存模型配置。
- [README/文档依据](https://raw.githubusercontent.com/Nixtla/mlforecast/main/README.md) · [创建Fork（待完成）](https://github.com/Nixtla/mlforecast/fork)。

### 58. [winedarksea/AutoTS](https://github.com/winedarksea/AutoTS) · 1434 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：自动搜索时序模型和组合预测。
- 风险/限制：自动搜索可能耗时，并存在过拟合选择风险。
- 建议修改：限定预算和模型集，固定滚动验证与随机种子。
- [README/文档依据](https://raw.githubusercontent.com/winedarksea/AutoTS/master/README.md) · [创建Fork（待完成）](https://github.com/winedarksea/AutoTS/fork)。

### 59. [tidyverts/fable](https://github.com/tidyverts/fable) · 593 Stars

- 实用候选，仍需实测；GPL-3.0；最近推送 2026-09-15。
- 用途：用整洁时序框架做ARIMA与指数平滑。
- 风险/限制：需要学习R的tsibble/fable工作流。
- 建议修改：提供行业月报模板、时间缺口检查与统一误差表。
- [README/文档依据](https://raw.githubusercontent.com/tidyverts/fable/main/README.md) · [创建Fork（待完成）](https://github.com/tidyverts/fable/fork)。

### 60. [SalesforceAIResearch/uni2ts](https://github.com/SalesforceAIResearch/uni2ts) · 1615 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2026-06-02。
- 用途：研究通用时序Transformer的预训练与预测。
- 风险/限制：上游提示研究用途与下游需评估；模型权重还要独立核查。
- 建议修改：用真实行业样本与统计基线对照，记录权重许可和资源消耗。
- [README/文档依据](https://raw.githubusercontent.com/SalesforceAIResearch/uni2ts/main/README.md) · [创建Fork（待完成）](https://github.com/SalesforceAIResearch/uni2ts/fork)。

### 61. [time-series-foundation-models/lag-llama](https://github.com/time-series-foundation-models/lag-llama) · 1601 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2025-06-06。
- 用途：试验通用概率时序模型与零样本预测。
- 风险/限制：预训练数据和目标行业可能分布不同；依赖权重。
- 建议修改：记录权重版本，评估区间校准、领域迁移和简单基线。
- [README/文档依据](https://raw.githubusercontent.com/time-series-foundation-models/lag-llama/main/README.md) · [创建Fork（待完成）](https://github.com/time-series-foundation-models/lag-llama/fork)。

### 62. [PriorLabs/tabpfn-time-series](https://github.com/PriorLabs/tabpfn-time-series) · 469 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2026-10-24。
- 用途：用TabPFN进行零样本时序预测。
- 风险/限制：代码许可与模型许可分开；本地模式需接受模型条款，客户端依赖云API。
- 建议修改：显式选择本地/云模式，记录授权、成本和泄漏检查。
- [README/文档依据](https://raw.githubusercontent.com/PriorLabs/tabpfn-time-series/main/README.md) · [创建Fork（待完成）](https://github.com/PriorLabs/tabpfn-time-series/fork)。

### 63. [GestaltCogTeam/BasicTS](https://github.com/GestaltCogTeam/BasicTS) · 1829 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2025-12-23。
- 用途：统一时序模型的训练、测试与比较。
- 风险/限制：基准数据的好成绩不证明实际行业预测有效。
- 建议修改：加入行业数据适配器，固定切分、指标和运行环境。
- [README/文档依据](https://raw.githubusercontent.com/GestaltCogTeam/BasicTS/master/README.md) · [创建Fork（待完成）](https://github.com/GestaltCogTeam/BasicTS/fork)。

### 64. [kwuking/TimeMixer](https://github.com/kwuking/TimeMixer) · 1995 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2025-10-05。
- 用途：实验多尺度混合时序预测模型。
- 风险/限制：论文复现代码的配置与算力要求需要验证。
- 建议修改：加入朴素和统计基线，记录消融实验与单次训练成本。
- [README/文档依据](https://raw.githubusercontent.com/kwuking/TimeMixer/main/README.md) · [创建Fork（待完成）](https://github.com/kwuking/TimeMixer/fork)。

### 65. [KimMeen/Time-LLM](https://github.com/KimMeen/Time-LLM) · 2707 Stars

- 实验/研究或包含实验能力；Apache-2.0；最近推送 2025-10-15。
- 用途：把大语言模型重编程用于时序预测。
- 风险/限制：大模型和训练流程增加显存、依赖与复现成本。
- 建议修改：先做小样本CPU/GPU可运行检查，再对比更便宜基线。
- [README/文档依据](https://raw.githubusercontent.com/KimMeen/Time-LLM/main/README.md) · [创建Fork（待完成）](https://github.com/KimMeen/Time-LLM/fork)。

### 66. [thuml/iTransformer](https://github.com/thuml/iTransformer) · 2237 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2025-07-17。
- 用途：实验反转Transformer结构的多变量预测。
- 风险/限制：论文模型需要针对行业频率与变量数重新验证。
- 建议修改：提供行业数据读取器、固定随机种子和滚动回测。
- [README/文档依据](https://raw.githubusercontent.com/thuml/iTransformer/main/README.md) · [创建Fork（待完成）](https://github.com/thuml/iTransformer/fork)。

### 67. [AIStream-Peelout/flow-forecast](https://github.com/AIStream-Peelout/flow-forecast) · 2308 Stars

- 实用候选，仍需实测；GPL-3.0；最近推送 2026-10-12。
- 用途：整合多种深度时序预测、分类和异常检测模型。
- 风险/限制：模型多导致配置复杂；README标出部分Transformer推理还需目标输入。
- 建议修改：逐模型记录推理输入契约，排查目标泄漏并裁剪依赖。
- [README/文档依据](https://raw.githubusercontent.com/AIStream-Peelout/flow-forecast/master/README.md) · [创建Fork（待完成）](https://github.com/AIStream-Peelout/flow-forecast/fork)。

## 文本与主题研究

### 68. [charlesdedampierre/BunkaTopics](https://github.com/charlesdedampierre/BunkaTopics) · 201 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-21。
- 用途：清洗和可视化行业新闻/访谈文本主题。
- 风险/限制：嵌入、聚类和图布局的变化可能影响主题解释。
- 建议修改：固定模型与种子，加入中文样本、原文链接和人工标签。
- [README/文档依据](https://raw.githubusercontent.com/charlesdedampierre/BunkaTopics/main/README.md) · [创建Fork（待完成）](https://github.com/charlesdedampierre/BunkaTopics/fork)。

### 69. [MilaNLProc/contextualized-topic-models](https://github.com/MilaNLProc/contextualized-topic-models) · 1274 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-07-24。
- 用途：结合上下文嵌入做主题建模。
- 风险/限制：嵌入模型和语种选择影响主题质量。
- 建议修改：固定多语言模型，加入中文分词对照与主题稳定性检查。
- [README/文档依据](https://raw.githubusercontent.com/MilaNLProc/contextualized-topic-models/master/README.rst) · [创建Fork（待完成）](https://github.com/MilaNLProc/contextualized-topic-models/fork)。

### 70. [bab2min/tomotopy](https://github.com/bab2min/tomotopy) · 602 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-02-21。
- 用途：用C++加速多种贝叶斯主题模型。
- 风险/限制：词袋模型依赖分词与词表，主题数量需选择。
- 建议修改：增加中文停用词、领域词典及主题数敏感性分析。
- [README/文档依据](https://raw.githubusercontent.com/bab2min/tomotopy/main/README.rst) · [创建Fork（待完成）](https://github.com/bab2min/tomotopy/fork)。

### 71. [MIND-Lab/OCTIS](https://github.com/MIND-Lab/OCTIS) · 807 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-06-21。
- 用途：比较与优化多类主题模型。
- 风险/限制：自动指标不总与分析人员可理解程度一致。
- 建议修改：加入人工可解释性评分，限定搜索预算并保存数据切分。
- [README/文档依据](https://raw.githubusercontent.com/MIND-Lab/OCTIS/master/README.rst) · [创建Fork（待完成）](https://github.com/MIND-Lab/OCTIS/fork)。

### 72. [bmabey/pyLDAvis](https://github.com/bmabey/pyLDAvis) · 1850 Stars

- 实用候选，仍需实测；BSD-3-Clause；最近推送 2025-12-04。
- 用途：交互查看主题间距离和关键词。
- 风险/限制：可视化依赖输入主题模型；图形接近不等于业务结论相同。
- 建议修改：附原文证据与主题标签，检查输入词表和概率归一化。
- [README/文档依据](https://raw.githubusercontent.com/bmabey/pyLDAvis/master/README.rst) · [创建Fork（待完成）](https://github.com/bmabey/pyLDAvis/fork)。

### 73. [ArikReuter/TopicGPT](https://github.com/ArikReuter/TopicGPT) · 117 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2025-09-19。
- 用途：用LLM生成更易理解的主题表示。
- 风险/限制：README明确随机性和LLM局限；有API成本与结果波动。
- 建议修改：缓存响应，保留原文出处，加入无LLM基线和人工复核。
- [README/文档依据](https://raw.githubusercontent.com/ArikReuter/TopicGPT/master/README.md) · [创建Fork（待完成）](https://github.com/ArikReuter/TopicGPT/fork)。

### 74. [x-tabdeveloping/topicwizard](https://github.com/x-tabdeveloping/topicwizard) · 149 Stars

- 实用候选，仍需实测；MIT；最近推送 2025-03-19。
- 用途：以交互界面探索主题模型和文档。
- 风险/限制：展示效果取决于底层模型及输入格式适配。
- 建议修改：统一主题接口，支持中文字体、源文档跳转和标签导出。
- [README/文档依据](https://raw.githubusercontent.com/x-tabdeveloping/topicwizard/main/README.md) · [创建Fork（待完成）](https://github.com/x-tabdeveloping/topicwizard/fork)。

### 75. [bobxwu/TopMost](https://github.com/bobxwu/TopMost) · 294 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2025-10-14。
- 用途：统一训练与比较多种主题模型。
- 风险/限制：研究框架依赖环境和数据预处理一致性。
- 建议修改：固定依赖与词表，加入中文行业语料及重复实验。
- [README/文档依据](https://raw.githubusercontent.com/bobxwu/TopMost/main/README.rst) · [创建Fork（待完成）](https://github.com/bobxwu/TopMost/fork)。

### 76. [MaartenGr/KeyBERT](https://github.com/MaartenGr/KeyBERT) · 4223 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-08-25。
- 用途：从行业报告和新闻中提取关键词。
- 风险/限制：相似度关键词不保证覆盖数字事实或行业专名。
- 建议修改：使用领域候选词、中文嵌入，并显示关键词对应原句。
- [README/文档依据](https://raw.githubusercontent.com/MaartenGr/KeyBERT/master/README.md) · [创建Fork（待完成）](https://github.com/MaartenGr/KeyBERT/fork)。

## 可视化与报告

### 77. [mckinsey/vizro](https://github.com/mckinsey/vizro) · 3810 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-23。
- 用途：低代码创建Python数据可视化应用。
- 风险/限制：可视化配置仍需要数据建模；生产服务还需认证与运维。
- 建议修改：加入中文行业看板模板、统一指标字典和只读数据连接。
- [README/文档依据](https://raw.githubusercontent.com/mckinsey/vizro/main/README.md) · [创建Fork（待完成）](https://github.com/mckinsey/vizro/fork)。

### 78. [holoviz/holoviews](https://github.com/holoviz/holoviews) · 2913 Stars

- 实用候选，仍需实测；BSD-3-Clause；最近推送 2026-10-23。
- 用途：通过数据语义生成交互可视化。
- 风险/限制：后端及大数据渲染策略需要选型。
- 建议修改：固定绘图库版本，对大表做聚合并提供静态导出。
- [README/文档依据](https://raw.githubusercontent.com/holoviz/holoviews/main/README.md) · [创建Fork（待完成）](https://github.com/holoviz/holoviews/fork)。

### 79. [zcreativelabs/react-simple-maps](https://github.com/zcreativelabs/react-simple-maps) · 3387 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-09-12。
- 用途：在React中创建SVG地图图表。
- 风险/限制：只负责地图展示；地理编码、边界口径仍要准备。
- 建议修改：加入地区代码映射、边界版本和缺失地区提示。
- [README/文档依据](https://raw.githubusercontent.com/zcreativelabs/react-simple-maps/main/README.md) · [创建Fork（待完成）](https://github.com/zcreativelabs/react-simple-maps/fork)。

### 80. [vasturiano/globe.gl](https://github.com/vasturiano/globe.gl) · 3206 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-08-22。
- 用途：展示全球供应链、运输路线等三维地球数据。
- 风险/限制：3D遮挡和浏览器性能可能影响准确比较。
- 建议修改：提供2D备选视图、数据聚合和明确单位/比例尺。
- [README/文档依据](https://raw.githubusercontent.com/vasturiano/globe.gl/master/README.md) · [创建Fork（待完成）](https://github.com/vasturiano/globe.gl/fork)。

### 81. [running-elephant/datart](https://github.com/running-elephant/datart) · 2309 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2025-02-10。
- 用途：创建报表、看板和数据大屏。
- 风险/限制：最近推送为2025年2月，维护活跃度需特别复核。
- 建议修改：先锁定可用版本，做连接器兼容测试和中文行业模板。
- [README/文档依据](https://raw.githubusercontent.com/running-elephant/datart/master/README.md) · [创建Fork（待完成）](https://github.com/running-elephant/datart/fork)。

### 82. [Kanaries/Rath](https://github.com/Kanaries/Rath) · 4686 Stars

- 实用候选，仍需实测；AGPL-3.0；最近推送 2026-08-14。
- 用途：试验自动探索分析和可视化。
- 风险/限制：自动推荐图表仍需业务解释；AGPL需要按上游条款使用。
- 建议修改：给每张图显示筛选、聚合及指标口径，并允许人工修改。
- [README/文档依据](https://raw.githubusercontent.com/Kanaries/Rath/master/README.md) · [创建Fork（待完成）](https://github.com/Kanaries/Rath/fork)。

### 83. [markmarkoh/datamaps](https://github.com/markmarkoh/datamaps) · 3798 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-02-10。
- 用途：用D3/SVG快速生成地区地图。
- 风险/限制：README正在招募维护者；旧依赖兼容性需验证。
- 建议修改：固定依赖，增加维护状态提示及新版前端适配。
- [README/文档依据](https://raw.githubusercontent.com/markmarkoh/datamaps/master/README.md) · [创建Fork（待完成）](https://github.com/markmarkoh/datamaps/fork)。

### 84. [observablehq/framework](https://github.com/observablehq/framework) · 3671 Stars

- 实用候选，仍需实测；ISC；最近推送 2026-05-15。
- 用途：用代码生成交互数据报告和静态站点。
- 风险/限制：需掌握JavaScript/构建流程；静态发布内容要审核。
- 建议修改：增加中文报告模板、构建检查和数据更新日期。
- [README/文档依据](https://raw.githubusercontent.com/observablehq/framework/main/README.md) · [创建Fork（待完成）](https://github.com/observablehq/framework/fork)。

### 85. [sqlrooms/sqlrooms](https://github.com/sqlrooms/sqlrooms) · 515 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：基于React和DuckDB-WASM搭建浏览器分析工具。
- 风险/限制：浏览器内存和WASM运行环境限制分析规模。
- 建议修改：增加文件大小预检、增量加载及服务端计算选项。
- [README/文档依据](https://raw.githubusercontent.com/sqlrooms/sqlrooms/main/README.md) · [创建Fork（待完成）](https://github.com/sqlrooms/sqlrooms/fork)。

### 86. [conveyal/transitive.js](https://github.com/conveyal/transitive.js) · 701 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-06-21。
- 用途：用交通网络数据生成易读的线路示意图。
- 风险/限制：适用场景偏交通；依赖规定的网络输入数据。
- 建议修改：提供GTFS/行业物流适配与路线完整性检查。
- [README/文档依据](https://raw.githubusercontent.com/conveyal/transitive.js/master/README.md) · [创建Fork（待完成）](https://github.com/conveyal/transitive.js/fork)。

## 分析数据库扩展

### 87. [duckdb/duckdb-wasm](https://github.com/duckdb/duckdb-wasm) · 2148 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-10-22。
- 用途：在浏览器本地用SQL分析文件。
- 风险/限制：README说明默认单线程，多线程仍实验性；浏览器内存有限。
- 建议修改：增加Web Worker、体量预检和分块读取。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-wasm/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-wasm/fork)。

### 88. [duckdb/duckdb-spatial](https://github.com/duckdb/duckdb-spatial) · 720 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-10-21。
- 用途：在DuckDB里做地理空间分析。
- 风险/限制：README标记开发中且列出限制，实际支持范围需对当前版本复核。
- 建议修改：先建立坐标系/空间索引能力测试，再提供区域行业分析示例。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-spatial/v2.0-cyanoptera/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-spatial/fork)。

### 89. [duckdb/duckdb-vss](https://github.com/duckdb/duckdb-vss) · 271 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-10-14。
- 用途：在DuckDB内实验向量索引与相似检索。
- 风险/限制：README明确仅FLOAT向量，索引需全部放RAM，持久化非增量。
- 建议修改：做容量预估、重启恢复与召回率基准，并提供精确搜索回退。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-vss/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-vss/fork)。

### 90. [duckdb/duckdb-ui](https://github.com/duckdb/duckdb-ui) · 475 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-21。
- 用途：给DuckDB增加浏览器分析界面。
- 风险/限制：README说明大部分UI代码尚未公开，Fork不包含完整UI实现。
- 建议修改：明确开源边界，优先通过公开接口扩展查询模板。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-ui/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-ui/fork)。

### 91. [duckdb/duckdb-delta](https://github.com/duckdb/duckdb-delta) · 234 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-23。
- 用途：直接查询Delta Lake表。
- 风险/限制：README说明写入支持有限，需核对DuckDB与扩展版本。
- 建议修改：默认只读，加入版本兼容矩阵和写入能力检查。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-delta/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-delta/fork)。

### 92. [duckdb/duckdb-sqlite](https://github.com/duckdb/duckdb-sqlite) · 293 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-24。
- 用途：用DuckDB读写SQLite并跨源分析。
- 风险/限制：跨引擎数据类型和并发行为需要验证。
- 建议修改：默认只读连接，检查金额精度、时区和写锁错误。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-sqlite/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-sqlite/fork)。

### 93. [duckdb/duckdb-azure](https://github.com/duckdb/duckdb-azure) · 79 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-20。
- 用途：在DuckDB内读取Azure Blob数据。
- 风险/限制：README说明当前支持读取和glob；仍需云凭据。
- 建议修改：把读写能力显式化，加入凭据隔离、分区过滤与流量预算。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-azure/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-azure/fork)。

### 94. [evidence-dev/duckdb_gsheets](https://github.com/evidence-dev/duckdb_gsheets) · 359 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-02-21。
- 用途：用SQL读写Google Sheets。
- 风险/限制：README标记实验性，不支持WASM，写入前表格必须已存在。
- 建议修改：加表格存在性检查、写入预览及批量/配额管理。
- [README/文档依据](https://raw.githubusercontent.com/evidence-dev/duckdb_gsheets/main/README.md) · [创建Fork（待完成）](https://github.com/evidence-dev/duckdb_gsheets/fork)。

### 95. [duckdb/duckdb-excel](https://github.com/duckdb/duckdb-excel) · 64 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-14。
- 用途：在DuckDB中处理Excel相关格式与文件。
- 风险/限制：支持范围及数值格式语义需核对，不能当作完整Excel计算引擎。
- 建议修改：用金额、百分比和日期样本验证，逐项列出支持能力。
- [README/文档依据](https://raw.githubusercontent.com/duckdb/duckdb-excel/main/README.md) · [创建Fork（待完成）](https://github.com/duckdb/duckdb-excel/fork)。

### 96. [cwida/duckpgq-extension](https://github.com/cwida/duckpgq-extension) · 506 Stars

- 实验/研究或包含实验能力；MIT；最近推送 2026-10-23。
- 用途：用SQL/PGQ研究图关系和图算法。
- 风险/限制：上游明确研究项目、开发中；语法与能力可能变化。
- 建议修改：锁定版本，增加供应链/股权关系样本及图查询契约测试。
- [README/文档依据](https://raw.githubusercontent.com/cwida/duckpgq-extension/main/README.md) · [创建Fork（待完成）](https://github.com/cwida/duckpgq-extension/fork)。

### 97. [lance-format/lance-duckdb](https://github.com/lance-format/lance-duckdb) · 133 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-17。
- 用途：在DuckDB中读写Lance数据表。
- 风险/限制：README说明与DuckDB发布周期绑定，版本耦合需管理。
- 建议修改：固定DuckDB/扩展组合，校验类型与读取结果一致性。
- [README/文档依据](https://raw.githubusercontent.com/lance-format/lance-duckdb/main/README.md) · [创建Fork（待完成）](https://github.com/lance-format/lance-duckdb/fork)。

### 98. [ywelsch/duckdb-prql](https://github.com/ywelsch/duckdb-prql) · 333 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-05-28。
- 用途：用PRQL表达查询并交给DuckDB执行。
- 风险/限制：多一层查询翻译，需要验证语义与扩展兼容。
- 建议修改：保留生成SQL，比较聚合、空值和窗口查询的等价结果。
- [README/文档依据](https://raw.githubusercontent.com/ywelsch/duckdb-prql/main/README.md) · [创建Fork（待完成）](https://github.com/ywelsch/duckdb-prql/fork)。

### 99. [Query-farm/airport](https://github.com/Query-farm/airport) · 349 Stars

- 实用候选，仍需实测；MIT；最近推送 2026-10-23。
- 用途：让DuckDB通过Arrow Flight访问远程数据服务。
- 风险/限制：需要远端Flight服务、认证和网络运行环境。
- 建议修改：增加连接配置、超时与重试，并校验远程结果和本地一致性。
- [README/文档依据](https://github.com/Query-farm/airport/blob/v2.0/docs/README.md) · [创建Fork（待完成）](https://github.com/Query-farm/airport/fork)。

### 100. [chdb-io/chdb](https://github.com/chdb-io/chdb) · 2919 Stars

- 实用候选，仍需实测；Apache-2.0；最近推送 2026-10-13。
- 用途：把ClickHouse分析引擎嵌入Python等程序。
- 风险/限制：多平台包与引擎语义、资源开销需实际验证。
- 建议修改：固定版本，增加中文CSV/Parquet与DuckDB对照基准。
- [README/文档依据](https://raw.githubusercontent.com/chdb-io/chdb/main/README.md) · [创建Fork（待完成）](https://github.com/chdb-io/chdb/fork)。
