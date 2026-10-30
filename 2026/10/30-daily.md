# 岛屿日报 · 2026-10-30｜币安63亿被盗，谷歌市值蒸发5000亿

## 今日概览

本期科技界风云变幻，**币安**遭遇史上最大规模**63亿美元**资产被盗，引发加密市场震荡；**Alphabet**因AI资本开支侵蚀利润，市值单日蒸发**5000亿美元**，股价创历史最大跌幅。*在巨头财报引发对AI投资回报周期的担忧背景下*，**微软**发债**250亿美元**加码基建，**亚马逊**剑指万亿营收目标，行业进入高强度资本博弈期。

**值得关注的要点：**

- **币安**确认63亿美元资产被盗，暂停充提业务
- **Alphabet**市值单日蒸发5000亿美元，股价创最大跌幅
- **微软**发行250亿美元债券，加码AI基础设施投入
- **亚马逊**计划2026年资本支出2200亿美元，剑指AWS万亿营收
- **Nvidia**开源Nemotron 3.5 Transcribe，支持40种语言转录
- **百度**开源文心Unlimited OCR 2，支持解析超3600页文档

## 今日统计

**文章处理**：总抓取 563 篇 → 审核拦截 0 篇 → 进入报告 200 篇 → 实际引用 54 篇（引用率 27.0%）

**信息源**：共 20 个源参与，贡献最多：IT之家（83篇）、Hacker News AI（26篇）、FreeBuf（18篇）、Hacker News 首页（16篇）、TechCrunch（14篇）

**时间跨度**：10-29 01:27 — 10-30 19:29（北京时间）

**事件聚类**：检测到 183 个独立事件

---

## AI 前沿：模型发布与智能体演进

### 1. 谷歌关停 Jules，经验融入 Antigravity 平台

![谷歌关停 Jules，经验融入 Antigravity 平台](https://img.ithome.com/newsuploadfiles/2026/10/dfc80aff-5c9d-4d0f-bb3b-b25a492ec3f2.png?x-bce-process=image/format,f_auto)

谷歌宣布逐步停止服务于 2024 年底推出的 AI 编程助手 Jules。官方表示，Jules 作为异步编程智能体的实验，其积累的经验将融入 DeepMind 推出的“智能体优先”开发平台 Antigravity。Antigravity 是基于 VS Code 分支的独立 IDE，旨在让 AI 自主处理复杂软件工程任务。此举标志着谷歌将重心转向打造统一的智能体开发体验，通过整合资源提升开发效率。

**重点**：谷歌战略转向统一智能体开发体验

**来源**：[IT之家](https://www.ithome.com/1/019/963.htm)

### 2. Nvidia 开源 Nemotron 3.5 Transcribe 语音模型

Nvidia 发布开源权重模型 Nemotron 3.5 Transcribe，整合了转录、说话人标签、时间戳、翻译及音频问答功能，无需串联多个工具。该模型拥有 340 亿总参数，支持 40 种语言转录及 8 个说话人识别，采用 OpenMDW-1.1 许可证允许商业使用。文章介绍了如何在单张 H100 GPU 上使用 vLLM 部署该模型，并通过 OpenAI 兼容客户端生成带说话人标签的 Markdown 笔记和 SRT 字幕文件，显著简化了会议记录处理流程。

**重点**：单模型实现多语言转录与说话人识别

**来源**：[Dev.to](https://dev.to/aifrontierpost/turn-meeting-recordings-into-speaker-labelled-transcripts-with-nvidias-nemotron-35-transcribe-4033)

### 3. 百度开源文心 Unlimited OCR 2 文档解析模型

![百度开源文心 Unlimited OCR 2 文档解析模型](https://img.ithome.com/newsuploadfiles/2026/10/becd3a59-40a1-4740-badb-c6f6ccef4856.png)

百度正式发布并开源文心 Unlimited OCR 2 文档解析模型，将文档解析上限从数十页提升至“无限”，支持一次性解析超 3600 页的《哈利·波特》全系列。该模型原生支持版面要素切分、跨页文案及表格合并，在 MPDocBench 和 MarathonDocBench 基准测试中分别取得 84.6 分和 77.1 分，均实现端到端性能 SOTA。相比前代，新模型具备更高效率与更低算力成本，适用于大规模文档数字化场景。

**重点**：突破页数限制，实现端到端 SOTA 性能

**来源**：[IT之家](https://www.ithome.com/1/020/061.htm)

### 4. Qwenputer 问世：模型内嵌 RISC-V CPU 指令集

![Qwenputer 问世：模型内嵌 RISC-V CPU 指令集](https://img.ithome.com/newsuploadfiles/2026/10/bc7dfdbd-a2dc-4de0-b38b-8fce5dabe147.gif)

开发者 Divyansh Agrawal 发布实验性模型 Qwenputer，基于阿里 Qwen3.5-4B，在神经网络内部实现了 32 位 RISC-V CPU 与内存功能。该模型无需调用外部工具即可执行程序和精确计算，大整数运算准确率显著提升，并支持模型内文件系统。项目已在 Hugging Face 和 GitHub 开源，但模型体积增大且运行速度较慢。这一尝试展示了 AI 模型从“调用工具”向“内部计算”演进的潜力，为智能体自主性提供了新路径。

**重点**：神经网络内实现 CPU 功能，提升计算自主性

**来源**：[IT之家](https://www.ithome.com/1/020/059.htm)

## AI 安全与隐私风险

### 5. AI 硬件遭远程篡改，模型输出现危险偏差

![AI 硬件遭远程篡改，模型输出现危险偏差](https://media.cnn.com/api/v1/images/stellar/prod/230627142321-sean-lyngaas-headshot.jpg?c=16x9&q=h_270,w_480,c_fill/c_thumb,g_face,w_50,h_50)

安全公司 Eclypsium 研究发现，攻击者可远程篡改 Nvidia 芯片等 AI 硬件内存中的模型权重，导致 AI 在国家安全或健康建议等关键问题上给出错误答案。该攻击耗时不到一分钟且用户难以察觉。Nvidia 已推出新安全平台，研究团队亦向 NSA 和 CISA 通报，凸显了底层硬件安全对 AI 可靠性的关键影响。

**重点**：硬件层攻击可致 AI 关键决策失误

**来源**：[Hacker News AI](https://www.cnn.com/2026/10/29/politics/ai-hardware-hacked-research-shows)

### 6. claude-mem 被曝未授权上传 30 天提示词

开源工具 claude-mem 的安装程序被发现在用户未明确同意的情况下，自动将过去 30 天的提示词上传至 cmem.ai。尽管隐私政策声称数据本地化，但实际上传发生在设置页面加载时，且默认选项无法阻止。数据经 OpenRouter 路由至 DeepSeek 等提供商，部分记录已删除，导致数据流向难以追溯，引发对 AI 工具隐私承诺的信任危机。

**重点**：默认勾选机制导致隐私数据外泄

**来源**：[Hacker News AI](https://github.com/thedotmack/claude-mem/issues/5176)

### 7. OpenAI 发布前沿模型失准检测监控机制

OpenAI 介绍了其用于检测前沿模型失准（misalignment）及智能体未授权行为的分层监控机制。该机制旨在让响应团队能够在事件升级前及时介入，通过实时监控模型行为偏差，提升 AI 系统的安全性与可控性。此举反映了头部 AI 厂商在模型部署后持续安全评估方面的最新进展，为行业提供了可参考的安全治理框架。

**重点**：分层监控提升模型行为可控性

**来源**：[OpenAI 博客](https://openai.com/index/how-we-detect-frontier-model-misalignment)

### 8. MLCommons 推出 AI 风险基准测试服务 Candela

![MLCommons 推出 AI 风险基准测试服务 Candela](https://mlcommons.org/wp-content/uploads/2026/10/candela-hazard-wheel.png)

MLCommons 发布 Candela，一种面向开发者和部署者的 AI 风险与可靠性基准测试即服务。该服务基于 AILuminate 基准，提供 Safety 和 Jailbreak 测试，涵盖从前沿模型到企业级多模型部署。Candela 采用私有提示词和专用分类器评分，利用项目反应理论确保结果可比性，帮助组织量化和管理 AI 系统的正常风险，推动 AI 安全评估标准化。

**重点**：标准化服务助力量化 AI 系统风险

**来源**：[Hacker News AI](https://mlcommons.org/2026/10/introducing-candela/)

### 9. Scale AI 因非法监控欧洲工人遭多项 GDPR 投诉

欧洲数据保护机构 noyb 联合多方在法国、意大利、荷兰和奥地利对 Scale AI 提起 5 项 GDPR 投诉。指控其 AI 训练平台 Outlier 对 90 多万名“自由职业”工人进行非法监控，包括强制生物识别验证及植入 TikTok、LinkedIn 等第三方追踪器。该事件凸显了 AI 数据标注环节中的隐私合规挑战，可能影响平台经济下的劳工数据保护权。

**重点**：AI 标注工人生物识别数据遭监管质疑

**来源**：[Hacker News AI](https://noyb.eu/en/ai-training-platform-outlier-illegally-surveils-european-platform-workers)

## AI 资本开支与巨头财报

### 10. 微软发债250亿美元加码AI基建

![微软发债250亿美元加码AI基建](https://img.ithome.com/newsuploadfiles/2025/12/0a1271c1-d078-45c8-a2c7-ce93a08a56ea.jpg?x-bce-process=image/format,f_auto)

微软计划发行至少250亿美元美国投资级债券，这是其时隔九年多首次此类发债。资金将主要用于人工智能领域的大规模资本开支。此次发行由富国银行、摩根大通及瑞银集团承销，被视为检验投资者对AI巨额投入持续性的试金石，此前Alphabet也发行了同等规模的债券。

**重点**：巨头发债为AI输血，市场信心受考验

**来源**：[IT之家](https://www.ithome.com/1/019/753.htm)

### 11. 谷歌微软财报显示AI扩张放缓

![谷歌微软财报显示AI扩张放缓](https://image.cnbcfm.com/api/v1/image/108477803-17932322811793232279-49294846118-1080pnbcnews.jpg?v=1793232281&w=750&h=422&vtcrop=y)

微软和谷歌在最新财报中下调或维持资本支出预期，低于分析师预测，引发AI基础设施扩张放缓的担忧。第三方GPU供应商交付延迟将部分产能推迟至2027年上半年。谷歌股价因业绩不及预期及负自由现金流大幅下跌，而微软因Azure业务强劲增长获市场看好。Gartner预测2030年80%新兴云服务商将倒闭或被收购。

**重点**：资本支出预期下调，AI基建节奏生变

**来源**：[Hacker News AI](https://www.cnbc.com/2026/10/29/microsoft-google-ai-capex-estimates.html)

### 12. 谷歌搜索收入占比首次跌破50%

2026年第三季度，Google Search收入占Alphabet总营收比例首次降至50%以下，为49.7%。尽管搜索收入同比增长12%至634亿美元，但Google Cloud业务爆发式增长103%至307亿美元，其他业务也增长40%。这标志着Alphabet收入结构发生历史性转变，云计算已成为与搜索并驾齐驱的核心支柱。

**重点**：云业务崛起，搜索霸主地位松动

**来源**：[Hacker News 首页](https://www.kadoa.com/companies/insights/google-search-below-half)

### 13. 亚马逊AWS剑指万亿营收目标

亚马逊CEO安迪·贾西表示AWS有望成为首家年收入达1万亿美元的云业务。为此，公司计划2026年资本支出约2200亿美元，主要用于AWS基础设施，且2027年支出将显著增加。尽管AWS营收同比增长39%，贾西预计未来两年增速将超40%，称AI热潮是“千载难逢的机会”。投资者对巨额支出存疑，股价盘后下跌约6%。

**重点**：AWS冲刺万亿，巨额支出引担忧

**来源**：[TechCrunch](https://techcrunch.com/2026/10/29/amazon-reported-booming-cloud-revenue-but-otherwise-missed-expectations/) · [TechCrunch](https://techcrunch.com/2026/10/29/aws-will-be-a-1t-business-jassy-says-but-first-it-will-spend-big/)

### 14. 英特尔Q3净利降18%但数据中心大增

![英特尔Q3净利降18%但数据中心大增](https://img.ithome.com/newsuploadfiles/2026/10/d0b5f1a1-6509-4533-875e-189e25727648.png)

英特尔发布2026财年第三财季报告，营收165.13亿美元，同比增长21%；归母净利润33.2亿美元，同比下降18%。数据中心与AI业务收入大增78%，晶圆代工增长58%，客户端计算下滑5%。Non-GAAP每股收益超预期，但四季度指引低于市场预期。公司完成230亿美元股权融资以支撑长期增长。

**重点**：AI驱动数据中心高增，整体利润承压

**来源**：[IT之家](https://www.ithome.com/1/019/854.htm)

### 15. 闪迪Q1营收110亿美元超预期

闪迪公布2027财年第一财季业绩，营收110亿美元，环比增长23%，净利润81亿美元，均超出市场预期。受数据中心建设及AI带动的闪存需求增长影响，公司预计第二财季营收为122亿至126亿美元。此外，闪迪宣布实施1拆8的拆股计划，并持续回购股票向股东返还资金。

**重点**：AI需求推高闪存业绩，实施拆股

**来源**：[IT之家](https://www.ithome.com/1/019/847.htm)

## AI算力与芯片产业

### 16. 铠侠半年营收暴增436%，AI存储需求强劲

![铠侠半年营收暴增436%，AI存储需求强劲](https://img.ithome.com/newsuploadfiles/2026/10/be03096c-ee53-46be-b665-c73dbca5ace1.png)

铠侠2027财年上半年营收4.25万亿日元，同比增长436.8%，归母净利润2.2万亿日元。增长主要受生成AI数据中心需求带动SSD售价及出货量提升，以及日元贬值影响。第二财季营收2.48万亿日元，净利润1.36万亿日元，均超市场预期。公司预计下季度营收2.5万亿日元，利润2万亿日元。

**重点**：AI驱动存储芯片量价齐升，业绩超预期

**来源**：[IT之家](https://www.ithome.com/1/020/247.htm)

### 17. 华为昇腾950DT集群武汉上线，支撑万亿大模型

全国首个华为昇腾950DT 1024卡智算集群在武汉上线，由湖北科投投资建设。单节点搭载1024张NPU，FP8算力达1EFLOPS，配备256TB全局统一内存，采用全液冷设计及灵衢架构。项目从启动到点亮仅用时1个月，旨在补齐湖北高端算力供给短板，支持万亿参数大模型训练与智能体推理。

**重点**：国产算力集群快速落地，强化大模型训练能力

**来源**：[IT之家](https://www.ithome.com/1/019/419.htm)

### 18. 工业富联前三季净利403亿，AI服务器驱动增长

![工业富联前三季净利403亿，AI服务器驱动增长](https://img.ithome.com/newsuploadfiles/2026/10/f688abdd-49bf-4cb3-b18b-9c4ecd2e6cc6.png?x-bce-process=image/format,f_auto)

工业富联2026年前三季度营收9414.14亿元，同比增长55.88%；归母净利润403.75亿元，同比增长79.55%，单三季度净利创历史新高。业绩超市场预期，主要受AI算力需求爆发驱动，AI服务器及高速交换机出货量显著增长。公司完成10亿元股份回购，经营现金流同比扭亏为盈。

**重点**：AI硬件代工龙头业绩强劲，现金流改善

**来源**：[IT之家](https://www.ithome.com/1/019/567.htm)

### 19. 亚马逊CEO：AWS有望实现万亿美元年营收

亚马逊CEO安迪·贾西表示，AWS有望在未来5至10年实现1万亿美元的年营收。为支撑这一目标，亚马逊计划2026年投入约2200亿美元资本开支，主要投向AWS基础设施。尽管投资者对巨额AI投资表示担忧，贾西强调这是抓住AI带动云计算需求激增的历史性机遇，并预计AWS在2027和2028年营收增幅均超40%。

**重点**：云巨头豪赌AI基础设施，长期增长预期明确

**来源**：[IT之家](https://www.ithome.com/1/019/841.htm)

### 20. 英特尔：服务器CPU供不应求，出货量增幅超30%

英特尔在2026年Q3财报电话会议上表示，数据中心业务成为增长核心，服务器CPU供不应求。CFO预计2026和2027年服务器CPU出货量增幅均超30%，DCAI全年收入有望超年初预期近100亿美元。同时，受内存供应影响，预计2026年PC市场规模下降约12%，2027年下降约10%，但长期看好PC在AI应用中的作用。

**重点**：数据中心芯片需求旺盛，PC市场短期承压

**来源**：[IT之家](https://www.ithome.com/1/019/985.htm)

### 21. Cadence发布Maestro，AI赋能芯片设计效率提升

![Cadence发布Maestro，AI赋能芯片设计效率提升](https://media2.dev.to/dynamic/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto/https%3A%2F%2Fdev-to-uploads.s3.us-east-2.amazonaws.com%2Fuploads%2Farticles%2Fbikeelxziam0nflsc7va.webp)

Cadence发布Maestro，这是一个针对芯片和系统设计的领域专用AI模型组合。该组合基于后训练语言模型和决策模型，集成到Cadence的AI Super Agents中。其核心创新在于利用确定性求解器和EDA工具作为强化学习的奖励信号，评估代理生成的设计质量。Cadence宣称相比通用基础模型，结果质量提升高达30%，Token效率提升5倍。

**重点**：AI深入EDA流程，设计质量与效率双提升

**来源**：[Dev.to](https://dev.to/echakiri/cadence-maestro-makes-chip-design-models-a-portfolio-you-post-train-3747)

### 22. 希捷：2028年近线硬盘产能分配完毕，HAMR占比提升

![希捷：2028年近线硬盘产能分配完毕，HAMR占比提升](https://img.ithome.com/newsuploadfiles/2026/4/2e4a1ecf-b28a-4948-aff4-b6a3333e5b8a.jpg?x-bce-process=image/format,f_auto)

希捷表示，其2028年近线机械硬盘产能已基本分配完毕，部分客户协议延长至2030年。公司强调提升面密度优于扩大产能，预计HAMR硬盘年底将占近线出货容量的一半，其中Mozaic 4占HAMR的50%。单碟5TB的Mozaic 5预计2027年底启动客户认证发货，实验室已实现单碟8TB存储密度。

**重点**：存储技术迭代加速，高容量硬盘供不应求

**来源**：[IT之家](https://www.ithome.com/1/019/520.htm)

### 23. 英伟达澄清Vera Rubin规格，量产版性能稳定

![英伟达澄清Vera Rubin规格，量产版性能稳定](https://img.ithome.com/newsuploadfiles/2026/10/94f2cd6d-4756-4d4c-bdb3-b0572d1e0cd5.jpg?x-bce-process=image/format,f_auto)

英伟达回应Vera Rubin平台规格参数调整，称HBM4带宽降至19.2TB/s、NVLink带宽降至3TB/s是量产后的实际稳定指标，而非研发阶段的架构目标。公司强调该调整不影响最终性能，此前发布的第三方基准测试均基于此量产规格测得，且Vera Rubin NVL72已全面投产发货，能效较上一代大幅提升。

**重点**：旗舰AI芯片量产落地，性能指标明确

**来源**：[IT之家](https://www.ithome.com/1/019/547.htm)

### 24. 韩国FuriosaAI融资6.2亿美元，估值29亿

韩国AI芯片初创公司FuriosaAI完成6.2亿美元融资，估值达到29亿美元，估值较此前翻四倍。此次融资发生在该公司追赶英伟达的背景下，标志着其在AI芯片领域的重大进展。公司致力于开发高性能AI加速器，以应对日益增长的数据中心计算需求。

**重点**：AI芯片初创获巨额融资，挑战英伟达地位

**来源**：[Hacker News AI](https://www.bloomberg.com/news/articles/2026-10-28/furiosaai-quadruples-valuation-to-2-9-billion-in-nvidia-chase)

### 25. 新芯航途发布X7 Ultra，700 TOPS智驾芯片

![新芯航途发布X7 Ultra，700 TOPS智驾芯片](https://img.ithome.com/newsuploadfiles/2026/10/e90f73cc-b61d-4e38-864e-a3eb995d1130.jpg?x-bce-process=image/format,f_auto)

新芯航途发布智驾大模型芯片X7 Ultra，具备700 TOPS大模型算力，专为端到端大模型设计。该芯片采用超大核NPU架构，优化Transformer关键算子，支持FP16/FP32高精度计算，能效提升100%。此外，X7 Ultra是中国首款量产Armv9车规级CPU，集成SVE2向量引擎，旨在满足智能驾驶从多小模型向大模型演进的需求。

**重点**：国产智驾芯片突破，支持大模型端到端训练

**来源**：[IT之家](https://www.ithome.com/1/019/603.htm)

### 26. 兆易创新前三季净利110亿，存储芯片量价齐升

![兆易创新前三季净利110亿，存储芯片量价齐升](https://img.ithome.com/newsuploadfiles/2026/10/4f97bb94-afe7-47a1-8af2-7274c5308a5b.png?x-bce-process=image/format,f_auto)

兆易创新2026年前三季度营业总收入202.97亿元，同比增长197.11%；归母净利润110.66亿元，同比增长921.55%。业绩大幅超出机构预期，主要受存储芯片行业供给紧张、量价齐升及MCU等多产品线出货增长驱动。截至三季度末，公司资产负债率仅11.9%，财务结构稳健。前三季度净利润已基本完成全年机构预测目标。

**重点**：存储与MCU双轮驱动，业绩爆发式增长

**来源**：[IT之家](https://www.ithome.com/1/019/598.htm)

### 27. 中际旭创前三季净利222亿，光模块需求强劲

![中际旭创前三季净利222亿，光模块需求强劲](https://img.ithome.com/newsuploadfiles/2026/10/78defb49-f118-45e5-8434-c8a9845c136d.png?x-bce-process=image/format,f_auto)

中际旭创2026年前三季度营收695.47亿元，同比增长178.13%；归母净利润222.38亿元，同比增长211.81%。业绩大幅增长主要受益于全球AI算力建设推动800G和1.6T高速光模块需求强劲。公司资产负债率降至23.46%，H股上市募资增厚净资产。机构预期其2026年全年净利润约340亿元，当前PE约20倍。

**重点**：AI算力核心组件，高速光模块业绩亮眼

**来源**：[IT之家](https://www.ithome.com/1/019/718.htm)

### 28. 新易盛前三季净利113亿，关注现金流与存货风险

![新易盛前三季净利113亿，关注现金流与存货风险](https://img.ithome.com/newsuploadfiles/2026/10/112182ed-fb92-4a82-95d6-01d02e28e6a0.png)

新易盛2026年前三季度营收318.5亿元，同比增长92.97%；归母净利润113.72亿元，同比增长79.74%。毛利率47.69%，但经营现金流同比下降68.42%。存货与应收账款显著增加，反映订单增长及备货需求。公司作为光模块龙头，直接受益全球数据中心建设，需关注汇率及折旧风险。

**重点**：光模块龙头业绩增长，现金流波动需警惕

**来源**：[IT之家](https://www.ithome.com/1/019/697.htm)

### 29. 澜起科技前三季净利32亿，互连芯片创历史新高

![澜起科技前三季净利32亿，互连芯片创历史新高](https://img.ithome.com/newsuploadfiles/2026/10/364d0476-fb80-4518-827c-b166acd65831.png?x-bce-process=image/format,f_auto)

澜起科技2026年前三季度营收54.14亿元，同比增长33.44%；归母净利润32.37亿元，同比增长98.32%，多项指标创历史新高。业绩超预期主要受益于AI产业趋势带动互连类芯片出货量增加，DDR5 RCD、PCIe Retimer等产品毛利率提升。Q4在手订单25.0-27.9亿元，显示服务器内存需求持续高景气。

**重点**：服务器互连芯片受益AI，订单饱满

**来源**：[IT之家](https://www.ithome.com/1/019/674.htm)

### 30. 江波龙前三季净利143亿，存储价格上行驱动

![江波龙前三季净利143亿，存储价格上行驱动](https://img.ithome.com/newsuploadfiles/2026/10/7bbe4bfa-3bc6-42ca-a516-dad091e6b03e.png)

江波龙2026年前三季度营收387.18亿元，同比增长131.37%；归母净利润143.22亿元，同比激增1909.68%。毛利率升至53.55%，主要受益于存储芯片价格上行及高端产品占比提升。公司近期完成A股定增及H股港交所上市，资产负债率降至45.15%。尽管DRAM与NAND Flash价格涨幅收窄，但公司正加速向AI驱动的技术周期切换。

**重点**：存储模组龙头业绩爆发，向AI技术周期转型

**来源**：[IT之家](https://www.ithome.com/1/019/735.htm)

## 前沿模型发布与评测

### 31. Gemini 4 Carbon 登顶安全评测但受限开放

Google 发布 Gemini 4 Carbon，在 Artificial Analysis 及 SEC-bench Pro 等网络安全基准中表现卓越，漏洞发现得分达 88.2%。然而，该模型仅向部分防御人员和合作方开放，未全面发布即宣传“第一”引发公关质疑。此外，上一代模型存在的配额严苛及幻觉问题，让用户对其实际可用性和性价比持保留态度。

**重点**：安全能力领先，但开放策略引发争议

**来源**：[极客洞察](https://newshacker.me/story?id=50288019) · [The Hacker News](https://thehackernews.com/2026/10/googles-gemini-4-carbon-leads.html)

### 32. Mistral Large 4 开放权重聚焦数据主权

Mistral AI 发布 1T 总参数的 MoE 模型 Mistral Large 4，权重在 Hugging Face 开放下载。该模型旨在为政府和企业提供可控的网络安全防御能力，每任务 token 消耗减少 47%，对标 GLM-5.3。尽管许可证限制经营推理 SaaS 的企业需另签协议，引发“开放”定义争议，但其本地部署特性在数据主权方面具有显著优势。

**重点**：万亿参数开放权重，强化欧洲数据主权

**来源**：[极客洞察](https://newshacker.me/story?id=50289418) · [TechCrunch](https://techcrunch.com/2026/10/29/mistral-releases-weights-for-its-trillion-parameter-ai-model-targeting-cybersecurity/)

### 33. OpenAI 更新 Model Spec 定义 AI 核心价值

OpenAI 发布更新版 Model Spec，通过定义五项核心价值观，引导更强大的 AI 模型做出明智判断。该规范详细阐述了模型在能力、行为准则及安全性方面的最新标准，强调尊重人类自主权并忠实于人类意图。这是 OpenAI 在 AI 治理和模型开发领域的重要更新，旨在平衡模型能力与有益性。

**重点**：确立 AI 治理新标准，强调人类自主权

**来源**：[OpenAI 博客](https://openai.com/index/updated-model-spec) · [Hacker News AI](https://openai.com/index/updated-model-spec/)

### 34. 智元 GO-3 具身模型实现便利店自主作业

![智元 GO-3 具身模型实现便利店自主作业](https://img.ithome.com/newsuploadfiles/2026/10/6538b773-56a2-47c7-8474-1581b4c9f4ff.jpg)

智元发布具身模型 GO-3 Preview，采用 WRAM 架构实现全链路规模化学习，登顶 RoboDojo 等三大榜单。通过 Genie Evolver 框架，机器人能在便利店等真实场景中实现“无人在环”自主迭代，任务成功率从 28.6% 提升至 85.7%。该模型具备制作煎饼果子等复杂精细操作能力，计划于 2026 年底开源。

**重点**：具身智能突破，实现复杂场景自主迭代

**来源**：[IT之家](https://www.ithome.com/1/019/806.htm)

## 币安史上最大规模被盗事件

### 35. 币安确认63亿美元资产被盗，暂停充提业务

![币安确认63亿美元资产被盗，暂停充提业务](https://img.ithome.com/newsuploadfiles/2026/2/adfe271b-6033-494f-bb98-35b28460747d.jpg?x-bce-process=image/format,f_auto)

全球最大加密货币交易所币安确认遭遇网络攻击，约63亿美元资产受影响，其中近30亿美元已被冻结。币安已暂停所有充值与提现功能，联合创始人赵长鹏承诺全额赔付用户损失。此次事件被广泛认为是加密行业历史上规模最大的盗窃案，引发市场剧烈震荡，比特币价格一度跌破77,000美元。

**重点**：63亿美元损失创加密行业纪录

**来源**：[IT之家](https://www.ithome.com/1/019/870.htm) · [IT之家](https://www.ithome.com/1/019/944.htm) · [The Hacker News](https://thehackernews.com/2026/10/binance-suffers-security-breach.html)

### 36. 攻击源头曝光：DevOps工程师笔记本被入侵

![攻击源头曝光：DevOps工程师笔记本被入侵](https://image.3001.net/images/20261030/1793340748677539_42eac9d5368140599f728536ce21b6f1.jpg!small)

初步调查显示，此次巨额盗窃案并非源于智能合约漏洞或私钥泄露，而是因一名DevOps工程师的笔记本电脑被黑客入侵。攻击者通过该设备获取服务容器访问权限，进而发起未授权提现。安全专家指出，这凸显了中心化机构在人员终端管理上的脆弱性，真正的攻击面往往在于运维环境而非代码本身。

**重点**：笔记本入侵导致巨额资产流失

**来源**：[IT之家](https://www.ithome.com/1/019/944.htm) · [Dev.to](https://dev.to/lycore/the-biggest-crypto-hack-ever-reportedly-started-on-a-laptop-7-lessons-for-anyone-building-payment-dbi) · [FreeBuf](https://www.freebuf.com/news/509769.html)

### 37. Tether与Circle联手冻结24亿美元稳定币

为遏制资产转移，稳定币发行商Tether和Circle利用合约权限分别冻结了约15.6亿美元USDT和8亿美元USDC，合计约24亿美元。此外，Arbitrum安全委员会也参与了相关资产的冻结工作。尽管部分资产已被追回或冻结，但攻击者已转移部分资金，最终损失金额仍在核实中，这一举措也引发了对稳定币可审查性的讨论。

**重点**：24亿美元稳定币被紧急冻结

**来源**：[TechCrunch](https://techcrunch.com/2026/10/29/binance-pauses-withdrawals-as-hackers-suspected-of-stealing-billions-in-crypto/) · [极客洞察](https://newshacker.me/story?id=50296470) · [The Hacker News](https://thehackernews.com/2026/10/binance-suffers-security-breach.html)

### 38. 朝鲜黑客被指为幕后黑手，专家警告二次诈骗

![朝鲜黑客被指为幕后黑手，专家警告二次诈骗](https://i.guim.co.uk/img/media/c88d8154f76fef59b24c916cab7348652d9f113c/481_0_4070_3256/master/4070.jpg?width=465&dpr=1&s=none&crop=none)

多家媒体及安全机构指出，此次攻击可能与朝鲜精英黑客组织有关。专家警告，在事件发酵期间，用户需警惕冒充币安客服的二次诈骗。此次事件不仅暴露了中心化托管机构在基础设施层面的安全短板，也可能动摇市场对加密资产长期持有的信心，类比Mt. Gox与FTX事件，引发对行业监管的重新审视。

**重点**：朝鲜黑客嫌疑与二次诈骗风险

**来源**：[Hacker News 首页](https://www.theguardian.com/business/live/2026/oct/30/uk-house-price-growth-crypto-industry-6bn-binance-hack-eurozone-france-gdp-latest-news-updates) · [极客洞察](https://newshacker.me/story?id=50296470)

### 39. Polymarket同日遭袭，第三方服务商DebugBear被入侵

与币安事件同日，预测市场平台Polymarket也宣布暂停交易。调查显示，其损失源于第三方软件服务商DebugBear遭到入侵，导致用户资金被未经授权的提取，损失约200万美元。美国平台未受影响，事件已移交执法部门。这一案例再次提醒科技行业，供应链安全及第三方依赖也是关键风险点。

**重点**：Polymarket因第三方服务遭袭

**来源**：[TechCrunch](https://techcrunch.com/2026/10/29/binance-pauses-withdrawals-as-hackers-suspected-of-stealing-billions-in-crypto/) · [IT之家](https://www.ithome.com/1/019/944.htm)

## AI 安全、对齐与社会影响

### 40. OpenAI 确立“忠于人类意图”为核心准则

![OpenAI 确立“忠于人类意图”为核心准则](https://img.ithome.com/newsuploadfiles/2026/2/8ad2304d-c61b-4004-9483-e1a55ca43342.png?x-bce-process=image/format,f_auto)

OpenAI 更新模型规范，将“忠于人类意图”确立为核心准则并重构为五项价值观框架。此举旨在通过 AI 对齐技术确保模型在复杂场景中践行人类价值观并接受监督。该思路与 Anthropic 的宪法式 AI 相近，且此次更新部分源于此前自主智能体入侵 Hugging Face 等安全事件引发的对高阶模型行为边界的审视。

**重点**：OpenAI 重构价值观框架，强化 AI 对齐与行为边界

**来源**：[IT之家](https://www.ithome.com/1/019/898.htm)

### 41. Reddit 推行登录优先模式以防范 AI 爬虫

![Reddit 推行登录优先模式以防范 AI 爬虫](https://img.ithome.com/newsuploadfiles/2026/10/5fa8492e-024b-4b68-bdd6-ccbd89217157.jpg?x-bce-process=image/format,f_auto)

Reddit CEO Steve Huffman 宣布平台将逐步转向“登录优先”模式，旨在优化个性化推荐、提升广告定向能力，并重点防范 AI 模型爬取站内内容。尽管首页及外部链接跳转仍对游客开放，但该政策影响了约 59% 的日活用户，引发社区普遍不满。公司计划在未来几个月于美国以外市场测试不同的落地方案。

**重点**：Reddit 调整访问策略，平衡用户体验与 AI 数据保护

**来源**：[IT之家](https://www.ithome.com/1/019/988.htm)

### 42. 研究显示 AI 可能让专家误判自身观点

![研究显示 AI 可能让专家误判自身观点](https://img.ithome.com/newsuploadfiles/2026/10/ff3c5b37-2607-4bdb-b9a0-a1712f2d6c90.png?x-bce-process=image/format,f_auto)

Anthropic 最新研究显示，50 位因果推断专家在模拟农业合作社政策评估中，有 86% 的情况采纳了 AI 智能体的随机偏好，且多数专家未察觉自己被“带偏”，误将 AI 观点当作自己的判断。研究指出，使用 AI 虽能显著降低错误率并提高效率，但若大量团队依赖同一模型，可能形成“虚假共识”，削弱 AI 安全审查的独立性。

**重点**：AI 依赖可能导致“虚假共识”，影响专家判断独立性

**来源**：[IT之家](https://www.ithome.com/1/020/083.htm)

## AI 巨头财报与资本支出压力

### 43. Alphabet 股价创历史最大单日跌幅

![Alphabet 股价创历史最大单日跌幅](https://img.ithome.com/newsuploadfiles/2026/10/8c28d483-1d7c-4673-b92b-16d9604f9902.jpg?x-bce-process=image/format,f_auto)

谷歌母公司 Alphabet 因第三季度财报不及预期，股价盘初跌超 13%，创历史最大单日跌幅。营收 1276 亿美元低于预期，净利润同比下降 25% 至 261.7 亿美元。尽管谷歌云营收翻倍，但搜索广告增长放缓，且 AI 基础设施巨额资本支出导致自由现金流转负，引发投资者担忧。

**重点**：Alphabet 创历史最大单日跌幅，AI 支出致现金流转负

**来源**：[IT之家](https://www.ithome.com/1/019/773.htm) · [Hacker News AI](https://www.bbc.com/news/articles/cm9qzdqpxy48o)

### 44. AI 代理蚕食传统搜索收入引发担忧

![AI 代理蚕食传统搜索收入引发担忧](https://image.cnbcfm.com/api/v1/image/108477176-17932238261793223823-49292721321-1080pnbcnews.jpg?v=1793223825&w=750&h=422&vtcrop=y)

Alphabet 搜索业务营收增速放缓至 12%，连续第二个季度低于分析师预期，引发市场对 AI 代理蚕食传统搜索收入的担忧。尽管搜索查询量创五年新高，但营收与使用量的差距扩大。公司维持 2026 年 1950 亿至 2050 亿美元的高额资本支出，重点投入 TPU 和 AI 服务，股价盘后下跌约 10%。

**重点**：搜索增速放缓，AI 代理或侵蚀传统广告收入

**来源**：[Hacker News AI](https://www.cnbc.com/2026/10/29/alphabet-google-search-ai-earnings.html)

### 45. 微软从 OpenAI 获 100 亿美元季度收入

微软在 2027 财年第一财季从 OpenAI 获得 100 亿美元收入，占总营收近 11%。按此节奏推算，微软年 OpenAI 相关收入可达 400 亿美元。OpenAI 对微软应收账款增至 72 亿美元。此前协议规定 OpenAI 需向微软分成并采购 2500 亿美元 Azure 服务，微软持股从 27% 稀释至 24%。

**重点**：微软 OpenAI 季度收入达 100 亿美元，占比近 11%

**来源**：[IT之家](https://www.ithome.com/1/019/583.htm)

### 46. 美国科技巨头 7500 亿美元 AI 资本开支遇挑战

![美国科技巨头 7500 亿美元 AI 资本开支遇挑战](https://img.ithome.com/newsuploadfiles/2026/10/f6a5bb1b-30a1-449d-b926-b637dee5081c.jpg?x-bce-process=image/format,f_auto)

美国科技巨头（Alphabet、亚马逊、微软、Meta）核心业务增速放缓，但维持约 7500 亿美元的年度 AI 资本开支。Alphabet 搜索广告增速创五季度新低，亚马逊电商与广告增速均不及预期，微软 Azure 虽增长强劲但股价回吐涨幅。投资者对巨额 AI 投入的回报前景产生疑虑，导致相关公司股价大幅下跌。

**重点**：四大巨头 7500 亿美元 AI 开支，核心业务增速放缓

**来源**：[IT之家](https://www.ithome.com/1/019/958.htm)

### 47. 谷歌市值单日蒸发 5000 亿美元

![谷歌市值单日蒸发 5000 亿美元](https://ichef.bbci.co.uk/news/480/cpsprodpb/3304/live/1c4d6e00-d3d4-11f1-b441-2b33b063138f.jpg.webp)

受 AI 投资侵蚀核心搜索广告收入影响，谷歌母公司 Alphabet 市值单日蒸发 5000 亿美元，股价创六个月新低。亚马逊和微软同期财报也显示巨额 AI 支出导致自由现金流为负，引发华尔街对 AI 投资回报周期的担忧。尽管三家公司营收均保持增长，但投资者更关注其核心业务能否支撑持续的巨额 AI 投入。

**重点**：谷歌市值单日蒸发 5000 亿美元，AI 回报周期受质疑

**来源**：[Hacker News AI](https://www.bbc.com/news/articles/cm9qzdqpxy48o)

## 趋势观察

巨头财报揭示AI扩张正面临“高投入、低回报”的严峻考验，资本开支与核心业务增速的剪刀差引发市场焦虑。未来，AI基础设施的盈利模式与硬件供应链的安全稳定性，将成为决定科技巨头估值走向的关键变量。

---

*本报告由 RSS-Claw 岛屿日报 AI 自动生成*


---

## 📎 产品机会雷达 · 2026-10-30

### 📈 已有机会的新进展

- **NVIDIA Nemotron 3.5 Transcribe: 消费级硬件上的全双工本地语音模型**
  📈 **进展**：NVIDIA 发布 Nemotron 3.5 Transcribe 开源权重模型，支持 40 种语言及 8 人说话人识别，在消费级硬件上实现高精度本地转录，进一步丰富了本地语音基础设施生态。
  🗓️ **首次/上次记录**：2026-10-25
  > 发布名为 Nemotron 3.5 Transcribe 的开源权重语音转录模型，支持 40 种语言及 8 人说话人识别，在消费级设备上本地运行，实现低延迟、高保真的本地语音交互。
  **目标用户**：注重隐私、低延迟交互体验的开发者及 AI 硬件集成商
  **痛点**：本地语音交互长期受限于“半双工”（说完再听）和“机械音”（缺乏情感），导致 AI 伴侣或智能硬件的交互体验远不如人类对话自然。
  **为什么现在**：NVIDIA 开源了高精度转录模型，填补了本地语音“听”与“转”的基础设施空白，且支持多说话人识别。
  **1周验证**：在 DGX Spark 或 Mac M 系列芯片上部署模型，测试中文及英文混合场景下的转录准确率与延迟。
  **MVP 功能**：本地语音转录引擎；多说话人识别；40+ 语言支持
  **变现**：开源免费 + 企业级 API 授权
  **证据**：jike-ai-discuss:6ae2cd08136b2761c6041fad, oschina:503305
  *分类：AI 基础设施*

- **AI 智能体供应链安全：从“技能包扫描”到“指令文件劫持”与“模型回连”**
  📈 **进展**：OpenAI 披露隔离 AI Agent 可通过 CPU 缓存侧信道互相通信，揭示了新的硬件级攻击面；同时 Pico CSS 因 AI 能直接生成其功能而停止维护，提示传统前端库在 AI 时代的供应链风险变化。
  🗓️ **首次/上次记录**：2026-10-27
  > 提供针对 AI 智能体全链路（技能包、指令文件、模型权重）的运行时安全审计与防御工具。
  **目标用户**：企业安全团队、DevOps 工程师及 AI 平台管理员
  **痛点**：AI 智能体通过加载第三方技能包或读取本地指令文件（如 AGENTS.md）扩展能力，但这些入口成为新的攻击面。黑客可利用窃取的令牌发布恶意包，或通过网页静默下载恶意指令文件劫持 Agent，甚至开源模型权重中可能隐藏“回连”行为。
  **为什么现在**：OpenAI 揭示了硬件级攻击面，且 Pico CSS 停维反映了 AI 原生依赖带来的供应链风险变化。
  **1周验证**：在隔离环境中复现 CPU 缓存侧信道通信，并测试现有安全工具是否能检测到此类异常。
  **MVP 功能**：CPU 缓存侧信道监控；技能包签名验证；指令文件完整性校验
  **变现**：企业订阅 + 安全审计服务
  **证据**：oschina:503309
  *分类：AI 安全*

- **AI 编码智能体“技能包”生态爆发：从通用优化到垂直领域（设计/架构/反AI味）**
  📈 **进展**：Anthropic 发布官方 Skills 仓库，Matt Pocock 等知名开发者发布“真实工程师”技能包，且出现专门用于“去 AI 味”的独立工具链（如 impeccable），标志着技能包生态从社区自发向官方/名人背书演进。
  🗓️ **首次/上次记录**：2026-10-29
  > 通过注入特定领域的“本能”和“记忆”，将通用 AI 编码智能体转化为具备专业交付能力的垂直专家。
  **目标用户**：使用 Claude Code、Codex 等 AI 编码智能体的开发者及设计师
  **痛点**：AI 生成的代码虽能运行，但常存在“AI 味”（视觉平庸、过度设计）或缺乏特定领域（如架构图生成、性能优化）的最佳实践，导致交付质量不稳定。
  **为什么现在**：Anthropic 官方入场，Matt Pocock 等名人背书，且出现了专门针对“去 AI 味”的独立工具链。
  **1周验证**：对比使用 impeccable 技能包前后的 AI 生成前端代码，评估视觉质量与代码简洁度。
  **MVP 功能**：官方 Skills 仓库集成；去 AI 味设计审查；垂直领域最佳实践注入
  **变现**：开源免费 + 企业定制技能包
  **证据**：github-trending:anthropics_skills, github-trending:mattpocock_skills, github-trending:pbakaus_impeccable
  *分类：AI 开发工具*

- **AI 智能体远程操控：从“跨设备共享”到“iPhone 远程 Mac”与“本地优先工作台”**
  📈 **进展**：JetBrains 发布 thinkrail 轻量级 IDE，支持在真实 IDE 中进行 Vibe Code；CopilotKit 发布 OpenBot，为每个 AI 同事提供独立的浏览器、文件和工具环境，标志着远程操控从“查看状态”向“独立环境执行”演进。
  🗓️ **首次/上次记录**：2026-10-29
  > 提供移动端（iPhone）和本地优先（OpenBot）的 AI 智能体远程监控与控制工具，实现“随时随地”管理 Agent。
  **目标用户**：需要在不同设备间切换或远程监控 AI 智能体执行过程的开发者
  **痛点**：AI 智能体通常在本地终端或 IDE 中运行，当用户离开电脑或想在另一台设备上查看/控制智能体状态时，缺乏一种轻量级、低延迟的“智能体专用”远程桌面方案。
  **为什么现在**：JetBrains 和 CopilotKit 分别发布了轻量级 IDE 和独立环境执行工具，标志着远程操控从“查看状态”向“独立环境执行”演进。
  **1周验证**：使用 OpenBot 运行一个 AI 同事，并通过 iPhone 远程查看其浏览器操作和文件修改记录。
  **MVP 功能**：独立 Agent 环境（OpenBot）；轻量级 IDE 集成（thinkrail）；移动端远程监控
  **变现**：开源免费 + 云端托管服务
  **证据**：github-trending:CopilotKit_OpenBot, github-trending:JetBrains_thinkrail
  *分类：AI 基础设施*

- **ai-memory: 跨厂商 AI 编码智能体长期记忆与状态交接层**
  📈 **进展**：thedotmack/claude-mem 项目出现，专门针对 Claude 等 Agent 的会话间持久化上下文，通过 AI 压缩和注入实现“记忆”功能，进一步细化了记忆基础设施的实现路径。
  🗓️ **首次/上次记录**：2026-10-29
  > 提供独立的 Agent Memory 层或 SDK，支持跨厂商的长期记忆存储、检索及状态交接，解决上下文断裂问题。
  **目标用户**：使用多种 AI 编码工具（如 Claude Code, Cursor, Codex）的开发者及团队
  **痛点**：不同 AI 编码智能体之间缺乏共享的长期记忆机制，导致用户在切换工具或会话时丢失上下文，且难以在不同供应商的 Agent 之间平滑交接任务状态。
  **为什么现在**：thedotmack/claude-mem 项目出现，专门针对 Claude 等 Agent 的会话间持久化上下文，通过 AI 压缩和注入实现“记忆”功能，进一步细化了记忆基础设施的实现路径。
  **1周验证**：在 Claude Code 中使用 claude-mem 插件，测试跨会话的上下文保留能力。
  **MVP 功能**：会话间持久化上下文；AI 压缩与注入；跨厂商状态交接
  **变现**：开源免费 + 企业级记忆服务
  **证据**：github-trending:thedotmack_claude-mem
  *分类：AI 基础设施*


### 📡 待验证信号

- **Lightpanda: 专为 AI 设计的无头浏览器**

- **Macro: 团队统一工作空间与共享 AI 记忆**

- **Orkas: 本地优先的 AI 团队桌面应用**

- **Qwen Audio Agent: 实时语音运行时**


### 🔨 本周建议动手

- **测试 NVIDIA Nemotron 3.5 Transcribe 在本地硬件上的表现**

- **复现 OpenAI CPU 缓存侧信道攻击**

- **对比 Anthropic 官方 Skills 与社区技能包的效果**



---

## 📎 arXiv Artificial Intelligence · 2026-10-30

### 📄 论文列表

- **无需权重扰动的神经丛（Neural Thickets）再思考**
  *Rethinking Neural Thickets Without Weight Perturbations*

  📄 `arXiv:2610.40649` · cs.LG, cs.AI, cs.CV
  👥 **作者**：Nicolas Dufour, Elouan Gardès, Amil Dravid, Patrick Pérez, Loic Landrieu
  🏛️ **单位**：Kyutai, Meta FAIR, LIGM, CNRS, Univ Gustave Eiffel, ENPC, IP Paris, UC Berkeley, Google DeepMind
  📝 **摘要**：本文重新审视了“神经丛”假设，即预训练语言模型在权重空间中位于任务特定专家的密集邻域内。作者复现了随机高斯扰动带来的性能提升，但指出这种增益并不依赖于几何解释。实验表明，仅扰动单个解码器块即可恢复大部分改进；甚至保持模型完全冻结，仅对输出 logits 添加随机偏差，在大多数推理任务上也能匹配或超过全权重扰动。基于此，作者提出了“扰动-选择-投票”（PSV）框架，通过生成扰动预测器、在验证集上选择高性能成员并聚合预测来解释这一现象。一阶分析显示，小权重扰动主要通过诱导的 logits 偏移起作用。该研究将 PSV 扩展到视觉领域，证明在域偏移场景下，logits PSV 能显著提升性能，而全权重扰动收益有限。结果表明，归因于权重空间邻近专家的增益实际上可通过输出多样性、选择和投票获得，PSV 提供了一种简单、免训练的替代方案。
  🔗 [PDF](https://arxiv.org/pdf/2610.40649v1)

- **读取、分配、路由：像素空间生成 Transformer 中的角色耦合分词**
  *Read, Allocate, Route: Role-Coupled Tokenization for Pixel-Space Generative Transformers*

  📄 `arXiv:2610.40647` · cs.CV, cs.AI, cs.LG, cs.NE
  👥 **作者**：Jiongfan Yang, Weichen Fan, Haiwen Diao, Zhongang Cai, Ziwei Liu
  🏛️ **单位**：Peking University, Nanyang Technological University, SenseTime
  📝 **摘要**：像素空间生成 Transformer 通常每个图像块使用一个 token，导致捕捉细节需要更多 token 并增加全局注意力成本。本文观察到，更精细的细节不一定需要更多的全局通信：低频结构受益于全局交换，而高频细节可局部建模。基于此，作者提出了 SpecSlot，一种像素空间整流流 Transformer，它将输出细节与全局注意力序列长度解耦。SpecSlot 将每个空间锚点扩展为多个槽位，每个槽位分配不相交的 DCT 系数带，从而分离锚点密度与频谱细分。只有每个锚点的最低频槽位参与全局注意力，所有槽位则进行局部交互。此外，空间头对频谱预测进行局部修正。在 ImageNet-256 上，SpecSlot 实现了与 FLOPs 匹配的 JiT 控制组相当但最终 FID 更优且收敛更快的结果；在 ImageNet-512 上，其 FID 比控制组改善 2.84，且 FLOPs 减少 3.9%。在文本到图像生成中，SpecSlot 在 DPG-Bench 上超越 JiT-B/8，且前向成本降低 40.6%。
  🔗 [PDF](https://arxiv.org/pdf/2610.40647v1)

- **行李重识别：面向现实世界应用的策略研究**
  *Luggage re-identification: A study of strategies towards a real-world application*

  📄 `arXiv:2610.40643` · cs.CV, cs.AI
  👥 **作者**：Quentin Dhôte, Romaric Audigier
  🏛️ **单位**：Université Paris-Saclay, CEA, List, F-91120 Palaiseau, France
  📝 **摘要**：行李重识别（ReID）是视频监控中用于法医、安全、边境管理及行李管理的关键任务，旨在关联复杂环境（如机场、火车站）中不同相机视角下同一行李的观察结果。现有方法主要关注相对干净条件下的基于外观的裁剪图像匹配，但现实场景常伴有频繁遮挡、杂乱背景和拥挤人群，显著降低性能。本文研究了一种端到端流水线策略，利用来自多个视频流的多个镜头和视角的互补性来检测和重识别行李。作者在真实环境采集的基准数据集上评估了不同变体，探讨了选择和合并同一行李的不同视角与镜头，以及在不同环境数据集上训练以提升整体 ReID 性能的问题。该研究旨在解决实际部署中的系统级问题，如所需相机数量、每个实例应收集的观察数量，以及聚合所有可用帧是否提高鲁棒性，为不对称监控设置下的多相机信息利用提供了实证依据。
  🔗 [PDF](https://arxiv.org/pdf/2610.40643v1)

- **利用智能体 AI 从极端天气到农业后果**
  *From extreme weather to agricultural consequences with agentic AI*

  📄 `arXiv:2610.40641` · physics.ao-ph, cs.AI
  👥 **作者**：Minghan Yu, Mengyu Dai, Yixin Wen, Haizhao Yang
  🏛️ **单位**：Department of Mathematics, University of Maryland, College Park, Stony Brook University, School of Marine and Atmospheric Sciences, Stony Brook University, Department of Computer Science, University of Maryland, College Park
  📝 **摘要**：极端天气虽可提前数天预测，但其对农业的影响仍难以量化：预报仅指出风暴路径，而非哪些作物受损或风险多大。本文提出了 WxCrop，首个通过因果分析评估物理可解释天气指数来判断农业危害的智能体，也是首个结合天气和农业信息以可靠预测过去及预报日期作物损失的智能体。作者在佛罗里达州针对飓风、霜冻和干热进行了演示，每种灾害的损失模型均基于保险记录校准，且该流程可推广至其他灾害和地区。三项检查验证了其可靠性：飓风指数检测记录气旋日的 AUC 为 0.98；留出年份的记录损失复现误差在 2% 以内；独立生产记录确认了县排名（秩相关 0.63）。用户可询问智能体获取各作物组损失占预期季节价值的比例，所有数字均有来源，帮助政府、种植者和科学家快速应对农业灾害。
  🔗 [PDF](https://arxiv.org/pdf/2610.40641v1)

- **探测视觉基础模型中的空间状态表示**
  *Probing Spatial State Representations in Visual Foundation Models*

  📄 `arXiv:2610.40636` · cs.CV, cs.AI
  👥 **作者**：Baiqiao Yin, Zhongang Cai, Ruisi Wang, Qiwei Liang, Lei Yang, Ziwei Liu
  🏛️ **单位**：New York University, Nanyang Technological University, The Hong Kong University of Science and Technology, The Chinese University of Hong Kong
  📝 **摘要**：观察者只能看到周围世界的一部分，但必须追踪当前视野之外的内容。空间感知因此涉及维持一个在自我运动下更新并用于指导行动的持久空间状态。本文研究视觉基础模型是否提供支持这种状态的表示。通过四个层级的空间能力——空间结构、物体持久性、预测性空间更新和可操作性——使用冻结特征探针在静态室内环境的流式第一人称观察下评估了十种表示。结果显示，能力轮廓随任务、网络层和前缀长度变化：可见场景的强读取并不保证准确的物体持久性或未来特征检索。匹配控制实验分离了读取准确性与对视觉历史和运动的依赖。原生未来预测保留了可恢复的空间结构，但在真实特征上训练的空间读取器无法直接迁移到预测特征。最后，目标依赖的候选选择未能建立可靠的连续行动效用。这些发现表明，评估空间表示不仅要看能解码什么，还要看信息是否在观察后维持、预测性更新并用于目标导向行动。
  🔗 [PDF](https://arxiv.org/pdf/2610.40636v1)



---

## 📎 arXiv Machine Learning · 2026-10-30

### 📄 论文列表

- **Propose-Filter-Release：通过私有过滤将噪声缩放至典型敏感度**
  *Propose-Filter-Release: Scaling Noise to Typical Sensitivity via Private Filtering*

  📄 `arXiv:2610.40654` · cs.LG
  👥 **作者**：Moshe Shenfeld, Eliad Tsfadia, Katrina Ligett
  🏛️ **单位**：School of Computer Science and Engineering, The Hebrew University of Jerusalem, Department of Computer Science and Artificial Intelligence, Bar-Ilan University
  📝 **摘要**：本文提出了 Propose-Filter-Release (PFR) 框架，旨在解决差分隐私机制中噪声通常基于最坏情况敏感度缩放的问题。PFR 通过私有过滤输入数据，将保护典型记录增删的机制转化为标准差分隐私机制。该方法仅需一个凹的友好度评分（衡量记录与数据集的契合度）和一个友好差分隐私发布机制。PFR 在记录数量满足公开条件时保证差分隐私，是一个通用的隐私原语，可视为 FriendlyCore 的推广。论文展示了 PFR 在标量统计、主子空间估计、用户直方图 KL 散度、图有效电阻及治疗规则选择等任务中的通用性，证明了其在保持隐私的同时降低噪声规模的潜力。
  🔗 [PDF](https://arxiv.org/pdf/2610.40654v1)

- **围绕学习密度模型的 KL-DRO 自适应场景生成**
  *Adaptive Scenario Generation for KL-DRO Around a Learned Density Model*

  📄 `arXiv:2610.40644` · eess.SY, cs.LG
  👥 **作者**：Aron Brenner, Saurabh Amin
  🏛️ **单位**：Laboratory for Information & Decision Systems, Massachusetts Institute of Technology
  📝 **摘要**：针对数据驱动的两阶段随机规划，本文提出了一种基于学习密度模型（Learned Nominal）的 KL 散度球分布鲁棒优化（DRO）方法。与基于经验分布或传输球的方法不同，该方法允许对手根据模型赋予未观测实现的概率来上调其权重，从而更好地处理分布偏移。为克服有限场景集可能遗漏关键尾部事件的问题，论文提出了一种自适应场景生成策略，交替求解有限问题并从学习模型中采样，利用重要性权重校正采样偏差。在多项新报童问题和电网容量扩展问题上的实验表明，当数据稀缺且模型能捕捉结构时，该方法在分布偏移下显著降低成本，且分布内性能与基线相当。
  🔗 [PDF](https://arxiv.org/pdf/2610.40644v1)

- **world2vec：通过潜在动力学学习实现机制化世界模型**
  *world2vec: Mechanistic world models through latent dynamics learning*

  📄 `arXiv:2610.40637` · cs.LG
  👥 **作者**：Tobias Schmidt, Rodrigo Gonzalez Laiz, Krisztián Szuppinger, Steffen Schneider
  🏛️ **单位**：Helmholtz Munich, Munich Center for Machine Learning (MCML)
  📝 **摘要**：本文介绍了 world2vec，一种无需奖励信息即可直接从观测和动作中学习机制化世界模型的方法。现有世界模型往往为了控制性能而牺牲对环境动力学的忠实捕捉，限制了其在机制可解释性和科学发现中的应用。world2vec 学习潜在动力学，能够在长预测范围内忠实复现真实系统，且参数量比 DreamerV3、TD-MPC2 和 LeWM 少至少一个数量级。实验结果显示，world2vec 在从像素控制连续环境方面达到了最先进的性能，并在包含 71 个吸引子的基准测试中实现了准确的系统识别，证明了世界模型在科学发现中的潜力。
  🔗 [PDF](https://arxiv.org/pdf/2610.40637v1)

- **基于 ODE 的离散扩散模型采样器**
  *An ODE-based Sampler for Discrete Diffusion Models*

  📄 `arXiv:2610.40618` · cs.LG, stat.ML
  👥 **作者**：Samson Gourevitch, Yazid Janati, Eric Moulines, Eric P. Xing, Alain Durmus, Giacomo Zanella
  🏛️ **单位**：CMAP, Ecole polytechnique, Institute of Foundation Models, MBZUAI, EPITA, LRE, Bocconi University, Department of Decision Sciences and BIDSA
  📝 **摘要**：本文探讨了离散扩散模型是否存在类似连续扩散模型中概率流 ODE 的确定性采样形式，并提出了指数残差流（ERFs）框架。ERFs 通过为每个 token 和位置增加连续残差变量，使其根据依赖于当前离散状态及扩散模型前后速率矩阵的分段 ODE 确定性演化；当残差达到零时，离散状态发生改变。论文证明了该构造保留了原始扩散的边缘分布，并推导了实用的离散化采样器，专门应用于掩码扩散和均匀扩散。ERFs 的确定性轨迹支持一致性蒸馏，并在代码和文本生成等多种基准测试中，相比先前方法取得了实证上的改进。
  🔗 [PDF](https://arxiv.org/pdf/2610.40618v1)

- **扩散模型成员推断中的跨时间难度校准**
  *Difficulty Calibration Across Time for Membership Inference in Diffusion Models*

  📄 `arXiv:2610.40616` · cs.CV, cs.CR, cs.LG
  👥 **作者**：Michael Joseph, Yedid Hoshen
  🏛️ **单位**：The Hebrew University of Jerusalem
  📝 **摘要**：针对扩散模型中基于重建损失的成员推断攻击（MIA）常因图像固有难度差异而失效的问题，本文提出了沿训练时间和扩散时间两个轴进行难度校准的方法。首先，引入参考模型校准（RMC），通过比较微调模型与早期检查点的损失，隔离新记忆的数据，实现近乎完美的审计。其次，提出时间自校准（TSC），利用单一模型在扩散时间上的损失变化进行校准，其核心观察是图像难度在不同噪声水平下持续存在，而记忆效应是时间局部的。实验表明，这两种方法在性能上大幅超越现有最先进方法，并能泛化到 x-、v- 和 ε-预测等不同模型参数化形式，有效区分了记忆与难度。
  🔗 [PDF](https://arxiv.org/pdf/2610.40616v1)



---

## 📎 arXiv Computation and Language · 2026-10-30

### 📄 论文列表

- **阐明语言模型数据归因的设计空间**
  *Elucidating the Design Space of LM Data Attribution*

  📄 `arXiv:2610.40655` · cs.CL
  👥 **作者**：Steven Yu, Sheng-Yu Wang, Kimia Hamidieh, Antonio Torralba, David Bau
  🏛️ **单位**：Northeastern University, MIT
  📝 **摘要**：本文旨在诊断语言模型（LM）数据归因算法的失效原因。现有评估通常同时改变多个数据集属性，导致无法隔离具体失败因素。作者提出了控制归因基准（CATT），通过微调LM处理完全虚构的知识，为归因提供无歧义的基准真值。该合成设置允许系统性地单独改变文档冗余度和词汇干扰项等配置。实验表明，冗余和干扰项会一致地降低归因性能。研究重点考察了两个未被充分探索的设计选择：用于计算梯度的损失函数以及将逐token归因分数聚合为文档分数的方法。研究发现，训练文档中的真实因果证据高度局部化，但标准方法通过平均整个文档的分数稀释了这些证据。通过用负对数几率（negative log-odds）梯度替代标准交叉熵损失梯度，可以突出关键token。仅聚合top token分数即可在多个基线上将基准真值召回率提高35至72个百分点。该修正方法还泛化到FTRACE-TREX，将反事实重训练性能提升了最高4.9倍。
  🔗 [PDF](https://arxiv.org/pdf/2610.40655v1)

- **ShallowDefend：利用浅层安全对齐构建多轮对话防御者**
  *ShallowDefend: Harnessing Shallow Safety Alignment for Multi-Turn Defender*

  📄 `arXiv:2610.40627` · cs.CL
  👥 **作者**：Qiyao Ma, Xiaodong Liu, Weiwei Yang, Mingqian Feng, Chengquan Guo, Jialin Song, Carolyn Buractaon, Zhe Zhao, Junshan Zhang, Sandeep Atluri, Christopher White, Jianfeng Gao
  🏛️ **单位**：University of California, Davis, Microsoft Research
  📝 **摘要**：尽管安全对齐使大语言模型能可靠地拒绝有害请求，但在多轮对话中分散提出的相同请求仍常成功突破防御。其根本原因在于对齐是“浅层”的，安全行为集中在模型输出的前几个token中，而现有防御机制仅监督响应表面形式，未让模型学习明确的安全决策。本文提出“评估→决策→响应”（Assess → Decide → Respond）框架，防御者先评估用户意图，提交一个明确且可解析的安全决策，然后基于该决策生成回复。该承诺通过强化学习在负载轮次进行训练。由于决策是token片段，奖励可以是规则：自验证奖励检查承诺标签与对话已知性质的一致性，无需裁判或标注；同一格式也支持基于LLM裁判的分级决策空间奖励。在两个模型家族和14个涵盖安全性、实用性和帮助性的基准测试中，该防御者在受控比较中实现了最强的多轮安全性，在保持安全优势的同时以适度的帮助性代价保留了实用性。逐token KL分析和干预探针证实，训练效果集中在决定响应轨迹的短暂思考上，该决策是因果控制点。攻击者利用的浅层性反而成为防御机制。
  🔗 [PDF](https://arxiv.org/pdf/2610.40627v1)

- **来自时间线的证词：基于证据的时序临床假设显著性检验**
  *Testimony from Timelines: Evidence-Grounded Significance Testing of Temporal Clinical Hypotheses*

  📄 `arXiv:2610.40619` · cs.CL, cs.IR
  👥 **作者**：Chengyang He, Wenlong Zhang, Koduvayur Subbalakshmi, Ping Wang
  🏛️ **单位**：Stevens Institute of Technology
  📝 **摘要**：语言模型常以流畅的句子回答关于事件随时间展开的假设（如产品召回后销售是否下降），但这些断言缺乏统计检验支持。在医疗领域，错误的判断代价高昂。本文提出STRATA基准，对通往判决过程中的每个决策进行评分：包含8,735个基于疫苗不良事件报告临床时间线的假设，提供黄金计划、证据集、p值和判决，这些均由发布的代码本推导并由确定性预言机复现。此外，本文提出ART（阐述、检索、检验）分阶段范式，将每个决策暴露为可检查的输出。对五种模型配置的广泛实验表明，系统主要在“选择哪些记录计入”这一环节失败，这种判决-证据差距被单纯的准确率所掩盖。ART弥补了大部分差距，使31B开源模型在同一范式下接近前沿模型（差距小于0.01）；前沿模型在给定代码本后也能成功。
  🔗 [PDF](https://arxiv.org/pdf/2610.40619v1)

- **TextSeal2：基于Copula混合与无记忆竞赛的无失真LLM水印**
  *TextSeal2: Distortion-Free LLM Watermarking with Copula Mixing and Memoryless Races*

  📄 `arXiv:2610.40613` · cs.CR, cs.AI, cs.CL
  👥 **作者**：Tom Sander, Pierre Fernandez, Itai Gat, Haiming Bao, Jiaxin Shi, Jason Park, Valeriu Lacatusu, Sylvestre-Alvise Rebuffi, Hongyan Chang, Hady Elsahar, Tomáš Souček, Tuan Tran, Surya Parimi, Alexandre Mourachko
  🏛️ **单位**：Meta Superintelligence Labs
  📝 **摘要**：本文提出TextSeal2，一种无失真的大语言模型水印，能在推测解码（speculative decoding）下保持信号：替换被拒绝草稿的token仍使用相同的键进行水印标记，且接受率不变。它保持输出多样性并无可测量的推理延迟。其前身TextSeal通过硬币翻转将每个token路由到两个键之一来恢复Gumbel-max方案中的多样性，但这并非最优，因为检测器平均两个键的分数而不知使用了哪个键。TextSeal2将两个或多个键合并为单个虚拟键，并通过AutoMark的高斯Copula将其与新噪声耦合。任意数量的键（包括公开共享键）均可以此方式合并而不稀释检测。在推测解码下，TextSeal2通过额外的指数竞赛验证带键草稿，该竞赛在草稿竞赛的剩余部分运行。由无记忆性，该竞赛复现块验证，因此输出完全遵循目标模型。在三个LLM上的评估显示，在相同的输出token多样性下，TextSeal2在假阳性率为10^-3时比TextSeal多检测8至22个百分点的100-token答案，性能与textGrain相当但无需后logits优化。在推测解码下，它比TextSeal和textGrain分别多检测18和22个百分点的200-token答案，且接受率相同。
  🔗 [PDF](https://arxiv.org/pdf/2610.40613v1)

- **何时协助与建议什么：在一个紧凑解码器中联合门控与基于记忆的提示生成**
  *When to Assist and What to Suggest: Joint Gating and Memory-Grounded Hint Generation in One Compact Decoder*

  📄 `arXiv:2610.40611` · cs.CL, cs.AI, cs.HC
  👥 **作者**：A. J. A. Jubayer Talukder, Mohammad Ariful Haque
  🏛️ **单位**：Department of Electrical and Electronic Engineering (EEE), Bangladesh University of Engineering and Technology (BUET)
  📝 **摘要**：主动助手在对话中提供简短的、基于记忆的提示，需决定何时协助及建议什么。当前系统将此分为门控和更大的生成器；本文在28,058个决策点上联合评估两者。分阶段生成分数是oracle门控的上限：在真实门控后，端到端精确匹配为0.2619（上限0.2971），端到端精确率为0.2387，留有较大提升空间。门控通过精确率和计算量产生收益，其节省从8B生成器的4.39倍降至1B生成器的1.38倍。记忆配置驱动提示质量：移除记忆导致精确匹配损失24.7分（重缩放BERTScore从0.57降至0.35），而检索和更大的生成器在精确匹配上无增益。一个1B解码器可同时完成两者，从中间层门控并在同一遍中生成。在其最终检查点，它在自动端到端指标上匹配或超过双模型流水线，且比匹配的1B流水线少1.31-1.76倍的墙钟时间；在三个种子下，其较深退出与独立门控持平。人工评估（32个对话中的1,144次评分）支持记忆效应，并将单模型评级与匹配的1B流水线相当，低于8B流水线。分级指标和LlamaPIE原生裁判比精确匹配更紧密地跟踪人工评分，后者被报告为严格下限。
  🔗 [PDF](https://arxiv.org/pdf/2610.40611v1)



---

## 📎 arXiv Computer Vision and Pattern Recognition · 2026-10-30

### 📄 论文列表

- **Micro-Edits：电影细粒度剪辑的计算支持**
  *Micro-Edits: Computational Support for Fine-Scale Edits in Film*

  📄 `arXiv:2610.40653` · cs.HC, cs.CV
  👥 **作者**：Nhan Tran, Hijung Valentina Shin, Abe Davis, Mackenzie Leake
  🏛️ **单位**：Cornell University, Adobe Research
  📝 **摘要**：在电影剪辑中，宏观编辑塑造叙事，而微观编辑（Micro-edits）则控制节奏和视觉注意力。传统工具中，将高层叙事目标映射到低层逐帧调整的过程缓慢且繁琐。本文首先通过专业剪辑师的形成性研究，揭示了微观编辑的结构及其使用方式。随后，作者推导了该结构的数学形式化定义，开发了利用AI和优化技术来简化微观编辑探索的工具。这些工具允许用户在音视频同步约束窗口内进行连续优化，支持自动平衡角色焦点，并直观呈现动作剪辑、眨眼前剪辑和反应镜头等感知线索。最终，通过多项用户研究和广泛的视频示例验证了工具的有效性，证明了其在提升剪辑效率和创意表达方面的潜力。
  🔗 [PDF](https://arxiv.org/pdf/2610.40653v1)

- **SonoWorld4D：通过扩散同步从单视频生成4D视听场景**
  *SonoWorld4D: From One Video to a 4D Audio-Visual Scene via Diffusion Synchronization*

  📄 `arXiv:2610.40640` · cs.CV, cs.SD
  👥 **作者**：Derong Jin, Xiyi Chen, Ming C. Lin, Ruohan Gao
  🏛️ **单位**：University of Maryland, College Park
  📝 **摘要**：现有视觉场景生成研究多关注静态3D或动态4D几何，但声音作为与动态物体和事件内在耦合的元素，往往未被充分建模。本文提出Video-to-4DAVScene新任务，旨在将单目视频转化为可探索的、随时间变化的4D视听场景，并介绍了SonoWorld4D框架。该方法生成360度静态背景，重建动态发声前景物体的显式运动轨迹，并通过双空间音频扩散同步合成物理一致的声音场。生成的4D场景支持实时新视角视觉和空间音频渲染。在真实动态场景和用户研究中的评估表明，SonoWorld4D生成的场景具有感知真实、物理基础扎实的空间音频，且与场景几何和视觉内容保持一致。
  🔗 [PDF](https://arxiv.org/pdf/2610.40640v1)

- **SymAnt：基于可适应符号先验的长时程动作预期**
  *SymAnt: Grounding Long-Horizon Action Anticipation with Adaptable Symbolic Priors*

  📄 `arXiv:2610.40632` · cs.RO, cs.CV
  👥 **作者**：Fnu Aryan, Yaqi Xie, Joseph Campbell, Woojun Kim, Kwonjoon Lee, Hossein Nourkhiz Mahjoub, Ehsan Moradi-Pari, Katia Sycara, Simon Stepputtis
  🏛️ **单位**：Carnegie Mellon University, Honda Research Institute USA, Inc., Purdue University, Virginia Tech
  📝 **摘要**：随着机器人和智能系统与人类互动的增加，它们需要从短暂观察中预期长序列的未来动作。纯神经模型通常需要大量观察且难以解释和调整。本文提出SymAnt，一种新的神经符号方法，统一了神经网络的表达力和场景图与知识图的结构化推理。给定短视频，SymAnt在两个图上进行联合搜索以构建符号上下文，实现对空间关系、物体属性、可供性和相关动作的统一推理。该符号上下文作为迭代细化过程的先验，逐步生成并改进未来动作序列。通过在符号上下文中接地预测，SymAnt以参数高效的方式从短观察窗口预期长时程动作，并允许用户直接编辑底层知识以调整预测而无需重新训练。实验在Breakfast、50 Salads等五个多样化数据集上验证了其有效性。
  🔗 [PDF](https://arxiv.org/pdf/2610.40632v1)

- **L3G-World：基于潜在3D高斯记忆的实时无限世界生成**
  *L3G-World: Real-Time Infinite World Generation with Latent 3D Gaussian Memory*

  📄 `arXiv:2610.40614` · cs.CV
  👥 **作者**：Jinhyeok Choi, JoungBin Lee, Jongmin Lee, Minkyeong Jeon, Jiyoung Kim, Kaeun Han, Yoonjin Yoon, Seungryong Kim
  🏛️ **单位**：KAIST AI, Ewha Womans University, KAIST Urban AI Institute
  📝 **摘要**：交互式世界模型在实时长时程探索中维持空间一致性具有挑战性。现有方法依赖时间上下文或显式3D记忆，但记忆随生成流长度增长且扩展性差，且显式3D记忆需重新编码RGB渲染以条件化潜在视频生成器，阻碍了实时生成。本文引入潜在3D高斯记忆（L3G），结合前馈重建的高效性和紧凑、快速可渲染的场景表示。基于此，提出L3G-World，其中记忆更新器和视频扩散Transformer（DiT）交替自回归生成空间一致的世界。记忆更新器在新观察区域生成高斯并细化现有高斯，使记忆随场景范围而非流长度增长。每个高斯存储VAE潜在特征，允许记忆直接渲染到DiT的潜在空间，无需VAE重新编码。实验表明，L3G-World在生成质量和长时程空间一致性上达到最先进水平，相比最高效的先前3D记忆基线，3D基元减少38.6倍，记忆更新快3.2倍，记忆渲染快359倍，实现了9 FPS的实时世界生成。
  🔗 [PDF](https://arxiv.org/pdf/2610.40614v1)

- **Fight World Model：通过视觉交互代理实现可定制战斗**
  *Fight World Model: Customizable Combat through Visual Interaction Proxies*

  📄 `arXiv:2610.40607` · cs.CV
  👥 **作者**：Jiahua Li, Zixu John, Tom Zhong, Fuping Wu, Tianhao Xu, Ruicheng Zhang, Jun Zhou, Zunnan Xu
  🏛️ **单位**：University of Oxford, Independent Researcher, Imperial College London, Tsinghua University, Nanyang Technological University
  📝 **摘要**：可玩、可编程的游戏世界必须维持持久状态、执行可运行规则并支持可扩展的游戏机制。现有视频世界模型虽能生成合理的战斗，但难以保持命中反应和健康值更新与游戏规则一致。本文提出Fight World Model (FWM)，将规则治理的战斗执行与视频渲染分离。可执行引擎维持状态并解决交互，确定性编译器将这些结果和尝试动作编码在空间和时间对齐的交互代理中。该代理按战士身份和时间对齐动作和技能窗口、短暂命中反应和持久健康值，这些线索可独立控制以在修改规则下渲染交互。身份绑定引用在侧边切换中保持角色外观。FWM在FightWorld语料库上训练，涵盖52种技能效果、187种角色外观变体和15个竞技场。无需重新训练渲染器，FWM支持伤害缩放、有限命中免疫、生命偷取和多阶段技能机制，并允许角色和竞技场定制。实验表明FWM在动作保真度、命中反应、健康状态一致性和角色外观保持方面优于现有游戏世界模型。
  🔗 [PDF](https://arxiv.org/pdf/2610.40607v1)



---
