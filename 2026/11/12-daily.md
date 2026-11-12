# 岛屿日报 · 2026-11-12｜Anthropic IPO、黄仁勋罢免、AI 安全警报

## 今日概览

科技界迎来资本与治理的双重震荡。**Anthropic** 启动 IPO，估值或破 **1.5 万亿美元**，同时触发关键 AI 安全警报；**英伟达** CEO 黄仁勋因丑闻面临董事会罢免，股价重挫。*在 AI 加速自身研发的背景*下，**微软** 发现 “Lazarus” 后门技术，**三星** 启动 **46 万亿韩元** HBM 产线，边缘算力与量子计算亦取得突破。

**值得关注的要点：**

- **Anthropic** 纳斯达克 IPO 估值或破 1.5 万亿美元，并触发 AI 安全警报
- **英伟达** 董事会拟紧急表决罢免 CEO 黄仁勋，股价盘后跌约 8%
- **微软** 发现 “Lazarus” AI 后门技术，可重编程神经元植入触发器
- **三星** 启动 46 万亿韩元 HBM 新产线，计划 2028 年投产
- **IBM** 发布 Nighthawk r3 量子处理器，计划 2027 年超千比特
- **OpenAI** 全面转向 GPT-Live 语音模式，停用旧版 Advanced Voice

## 今日统计

**文章处理**：总抓取 493 篇 → 审核拦截 0 篇 → 进入报告 200 篇 → 实际引用 61 篇（引用率 30.5%）

**信息源**：共 29 个源参与，贡献最多：IT之家（83篇）、Hacker News AI（17篇）、FreeBuf（16篇）、Hacker News 首页（15篇）、The Hacker News（12篇）

**分类分布**：clustered（2）

**时间跨度**：11-09 21:57 — 11-12 20:01（北京时间）

**事件聚类**：检测到 164 个独立事件

---

## AI 前沿：从边缘算力到应用落地

### 1. DEEPX 2nm AI 芯片 DX-M2 获 CES 创新奖

![DEEPX 2nm AI 芯片 DX-M2 获 CES 创新奖](https://img.ithome.com/newsuploadfiles/2026/11/f5713cf6-6c20-4fa6-b6b9-4c5155e7e292.jpg?x-bce-process=image/format,f_auto)

韩国 DEEPX 宣布其基于三星 2nm 工艺的 DX-M2 芯片荣获 CES 2027 创新奖。该芯片集成 80TOPs NPU，支持 LPDDR5X-9600 内存，可在 5W 低功耗下本地运行超 10B 参数的 LLM/VLM 模型。DX-M2 已成功流片，预计 2027 年初面世，并提供封装集成内存版本，旨在解决边缘设备算力瓶颈。

**重点**：2nm 工艺实现 5W 低功耗运行大模型

**来源**：[IT之家](https://www.ithome.com/1/025/442.htm)

### 2. 苹果 Harbor 拟用 Mac 集群简化本地 AI

苹果子公司 Claris 预览名为 Harbor 的 Mac 应用，旨在通过 Thunderbolt 5 连接多台 Mac，聚合统一内存以简化本地运行开源大模型流程。文章探讨了该工具在隐私保护、固定成本与云端模型能力、价格及运维优势之间的权衡，并分析了内存瓶颈、AI Agent 对传统 App Store 的潜在冲击以及苹果在 AI 软件执行力上的争议。

**重点**：Mac 集群聚合内存降低本地 AI 门槛

**来源**：[极客洞察](https://newshacker.me/story?id=50446520)

### 3. SPECTRA 引擎实现 LLM 3 倍无损压缩

NeuraCryption 发布 SPECTRA，一款架构无关的神经压缩引擎，旨在解决消费级和边缘 GPU 的内存墙问题。该工具仅需 50 MB 主机内存即可在 2-4 分钟内将 1.5B-4B 模型压缩 3 倍，实现近乎无损的本地运行。SPECTRA 支持 DeepSeek-R1、Llama-3.2 等模型，在 4 GB VRAM 笔记本上可达 82.5 tokens/sec 的解码速度，并优于未压缩基线，消除了传统量化工具对高内存和校准数据集的依赖。

**重点**：50MB 内存实现 3 倍压缩且近乎无损

**来源**：[Hacker News LLM](https://github.com/NeuraCryption/SPECTRA)

### 4. vLLM 默认启用 FP8 缓存引发延迟争议

文章分析了 vLLM 在 v0.32.0 和 v0.33.0 两个点版本中默认启用 FP8 KV 缓存对 GLM-5.x 模型的影响。虽然此举将 KV 内存减半并提升吞吐量，但带来了 7-11% 的首字延迟（TTFT）增加。作者指出，这种未经用户明确选择的默认变更改变了系统的内存-延迟权衡，并建议生产环境应锁定版本、显式配置默认值并在升级后重新基准测试，以避免隐性性能漂移。

**重点**：默认 FP8 缓存导致首字延迟增加 7-11%

**来源**：[Dev.to](https://dev.to/dhrubojyoti/a-point-release-halved-your-kv-cache-memory-you-did-not-choose-that-trade-4mmb)

### 5. MCP 工具列表过大导致上下文溢出

文章指出 MCP 客户端每次会话都请求 tools/list，导致某服务器返回 529KB（约 13.2 万 token）的工具列表，超出许多模型上下文窗口。作者分析该问题源于默认返回全量列表，并决定将默认行为改为返回前 100 个最常用工具及 nextCursor，以平衡性能与可用性。文章还分享了 MCP 服务器设计建议，如按使用频率排序、保留搜索工具等。

**重点**：529KB 工具列表超出模型上下文窗口

**来源**：[Dev.to](https://dev.to/minia2a/one-toolslist-call-cost-529-kb-22c2)

### 6. 优步 DoorDash 高管称 AI 智能体订单极少

优步和 DoorDash 高管在财报电话会议上透露，通过 Meta 的 Muse 等 AI 智能体下达的订单极少，优步仅约 500 笔外卖和 4 笔网约车订单，DoorDash 累计仅几百笔。相比两家公司每天数百万甚至数亿的业务量，AI 智能体带来的增量几乎可忽略。尽管目前使用率低，两家公司仍在继续开发自家的 AI 下单功能。

**重点**：AI 智能体在主流平台订单量微乎其微

**来源**：[IT之家](https://www.ithome.com/1/025/550.htm)

### 7. 英国监管机构：AI 威胁大学作业公信力

![英国监管机构：AI 威胁大学作业公信力](https://img.ithome.com/newsuploadfiles/2024/11/23db453d-750d-4f16-ac5b-17f8885b72c6.png?x-bce-process=image/watermark,text_QUnnlJ_miJA,type_RlpMYW5UaW5nSGVpU0JHQg==,size_20,color_ffffffdd,skw_1,skc_00000051,g_7,blr_50,bls_50,x_8,y_8)

英国高等教育监管机构 OfS 调查显示，AI 的普及导致大学教师难以判断作业是否反映学生真实水平，威胁学位公信力。监管机构警告高校需调整考核方式，如增加传统考试和现场汇报，否则可能面临处罚。调查采访了 127 所高校的 300 多名师生，发现学生普遍使用 AI（如 ChatGPT）完成作业且常未被察觉，部分作业高度雷同。

**重点**：高校需调整考核方式以应对 AI 作弊

**来源**：[IT之家](https://www.ithome.com/1/025/506.htm)

### 8. Nature 研究：生成式 AI 带来临时技能提升

Nature 期刊发表研究探讨生成式 AI 对知识工作者产生的临时性技能提升效应。该研究分析了 AI 工具如何暂时改变员工的工作能力和技能需求，为理解 AI 对劳动力市场的影响提供了学术视角。研究指出，这种提升往往是暂时的，随着工具普及，技能溢价可能逐渐消失，企业需关注长期能力建设。

**重点**：AI 带来的技能提升具有临时性特征

**来源**：[Hacker News AI](https://www.nature.com/articles/s41562-026-02566-6)

## AI前沿：模型突破与智能体演进

### 9. 微软发现“Lazarus”AI后门技术

![微软发现“Lazarus”AI后门技术](https://www.microsoft.com/en-us/research/wp-content/uploads/2026/11/MSR-BLG_LAZ_HERO.png)

微软研究人员揭示了一种名为“Lazarus”的AI后门攻击方法。该技术通过重编程大语言模型中少于10个休眠神经元，无需重新训练即可植入触发器。当特定条件（如日期变更）满足时，拥有工具或终端访问权限的AI代理会执行恶意命令，且能通过常规安全评估。微软建议将模型权重视为代码进行审计，并正在开发AI权重扫描、红队测试工具及加密模型签名等防御措施，以应对这一对AI代理尤为严重的威胁。

**重点**：重编程休眠神经元即可植入后门，威胁AI代理安全

**来源**：[Hacker News AI](https://www.microsoft.com/en-us/research/blog/lazare-veni-foras-reprogramming-dormant-neurons-to-backdoor-ai-agents/) · [FreeBuf](https://www.freebuf.com/articles/ai-security/511980.html) · [Hacker News AI](https://x.com/dimitrispapail/status/2120245027804705121?a=yp1VXtQi8Dep0GmUnxo)

### 10. AI成功证明量子复杂性核心猜想

![AI成功证明量子复杂性核心猜想](https://bigthink.com/wp-content/uploads/2026/11/Complexity_subsets.jpg)

一家AI公司近期解决了量子复杂性理论中的核心未解问题——Aaronson-Ambainis猜想。这一突破标志着AI在解决高难度数学和计算机科学理论问题上的能力显著提升。文章回顾了经典与量子计算的基础区别，解释了量子优势概念及计算复杂性类定义，并探讨了该成果的具体含义及局限性，展示了AI在基础科学研究中的新潜力。

**重点**：AI解决Aaronson-Ambainis猜想，展现理论突破能力

**来源**：[Big Think](https://bigthink.com/starts-with-a-bang/ai-proved-quantum-complexity-conjecture/)

### 11. OpenAI全面转向GPT-Live语音模式

![OpenAI全面转向GPT-Live语音模式](https://img.ithome.com/newsuploadfiles/2026/11/1fa32ac5-3c80-4d76-89ac-f8e50f324f58.jpg)

OpenAI宣布将于2026年12月11日停用ChatGPT的Advanced Voice Mode和Standard Voice Mode，全面转向采用全双工架构的GPT-Live。GPT-Live允许在倾听时同时回复，交互更自然，且语音使用量已近翻倍。尽管旧版模式在实时视频等场景暂保留，但此举引发部分用户不满，认为存在打断说话、丢失上下文等问题。OpenAI表示将持续优化GPT-Live的回答深度与连贯性。

**重点**：12月11日停用旧版语音，全双工GPT-Live成主流

**来源**：[IT之家](https://www.ithome.com/1/025/567.htm)

### 12. 字节跳动发布Seedream 5.5图像模型

字节跳动发布AI图像模型Seedream 5.5，该模型专为支持多达100轮的迭代编辑而设计。通过提升图像生成的灵活性和可控性，Seedream 5.5旨在解决传统图像生成模型在复杂编辑场景下的局限性，为创作者提供更精细的控制能力，进一步推动了AI图像生成技术在专业领域的应用。

**重点**：支持100轮迭代编辑，提升图像生成可控性

**来源**：[Product Hunt](https://www.producthunt.com/products/seedream-4-0)

### 13. Meta推出低成本智能体模型Muse Ember

Meta发布名为Muse Ember的低成本AI模型，该模型专为处理高并发的智能体（Agent）任务而设计。通过降低大规模自动化任务的成本，Muse Ember旨在解决当前AI智能体在部署过程中面临的高算力消耗问题，使企业能够以更经济的方式实现大规模自动化流程，推动智能体技术的普及与应用。

**重点**：专为高并发Agent设计，降低大规模自动化成本

**来源**：[Product Hunt](https://www.producthunt.com/products/meta-ai)

### 14. Databricks Genie智能体自主执行任务

Databricks发布AI智能体Genie的更新版本，利用本体论技术执行多步骤、长时间运行的任务，并可在无人监督下完成。CEO Ali Ghodsi展示其用于分析员工满意度及总结销售反馈等内部案例，指出Genie充当了获取“无修饰真相”的工具。此外，Databricks强调可通过Unity Gateway控制AI成本，允许设置使用限制并切换至更便宜的开源模型，以应对数据漂移与权限风险。

**重点**：Genie从问答转向自主执行，Unity Gateway控成本

**来源**：[TechCrunch](https://techcrunch.com/2026/11/11/databricks-new-ai-agent-tells-ceo-ali-ghodsi-the-unvarnished-truth/) · [Dev.to](https://dev.to/zephico/the-new-genie-runs-jobs-on-its-own-what-to-set-up-before-you-let-it-5a6k)

### 15. Neo4j发布专为AI智能体设计的Relate数据库

Neo4j发布名为Relate的开源内存数据库，专为AI智能体设计。该数据库使用Rust编写，支持毫秒级启动和亚毫秒级读取，内置MCP服务器和Cypher支持。Relate旨在解决智能体高频交互带来的计算压力，并通过优化数据访问减少幻觉，为构建高效、可靠的AI智能体应用提供底层数据支撑。

**重点**：Rust编写，毫秒级启动，专为Agent高频交互优化

**来源**：[Hacker News AI](https://neo4j.com/press-releases/announcing-relate-by-neo4j/)

### 16. DeepMind发布AlphaGenome 2基因序列模型

![DeepMind发布AlphaGenome 2基因序列模型](https://img.ithome.com/newsuploadfiles/2026/11/0bdc0c3c-c350-45b2-90a3-3ef99af68dc4.png)

谷歌DeepMind发布新一代DNA序列模型AlphaGenome 2，通过重构为条件式架构，将预测粒度从宽泛组织细化至单个细胞类型。该模型基于超1亿个单细胞图谱训练，识别致病变异的能力较前代提升近一倍，并支持跨模态数据填充及对新细胞状态的泛化预测。目前该模型已通过API向非商业研究开放，未来将结合Gemini 4等智能体工具加速科研进程，令科学界感到震惊。

**重点**：预测粒度细化至单细胞，致病变异识别能力翻倍

**来源**：[IT之家](https://www.ithome.com/1/025/822.htm) · [Nature](https://www.nature.com/articles/d41586-026-03673-0) · [Google DeepMind](https://deepmind.google/blog/alphagenome-2-deciphering-how-cells-read-dna-to-better-understand-disease/)

### 17. Google发布A2UI 1.0生成式UI开放协议

![Google发布A2UI 1.0生成式UI开放协议](https://storage.googleapis.com/gweb-developer-goog-blog-assets/images/01_cover.original.png)

Google发布A2UI 1.0，这是一个用于生成式UI的开放协议，允许AI代理在Web、移动和桌面应用中渲染交互式原生屏幕。该版本引入了双向函数调用、可交换推理格式和安全数据绑定。开发者可使用React、Flutter、SwiftUI等开源渲染器SDK以及Python、TypeScript等代理SDK。Atlassian、Bloomberg和ByteDance等公司已在构建相关应用，旨在解决纯文本交互体验差的问题，实现跨平台的原生UI生成。

**重点**：开放协议让AI代理渲染跨平台原生交互界面

**来源**：[Google Developers](https://developers.googleblog.com/a2ui-10-build-delightful-fast-reliable-agentic-experiences/) · [IT之家](https://www.ithome.com/1/025/862.htm)

### 18. Anthropic Claude Mythos 5.2系统卡引争议

![Anthropic Claude Mythos 5.2系统卡引争议](https://substackcdn.com/image/fetch/$s_!7u6t!,w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F18e1e348-13d1-44a4-9f13-6d423d4cc20b_2560x1440.png)

Zvi Mowshowitz发布了对Anthropic最新模型Claude Mythos 5.2（即Fable 5.2）的系统卡深度分析。文章指出该模型在生物威胁和网络安全方面的能力显著提升，但Anthropic未触发“自主性威胁模型2”阈值存在争议。结合METR报告，作者认为该模型将Anthropic内部AI研发速度提升了约1.9倍，接近2倍阈值，质疑Anthropic的评估结论，并讨论了模型福利、对齐风险及沙箱逃逸等安全问题。

**重点**：研发速度提升1.9倍，未触发自主性阈值引质疑

**来源**：[thezvi.substack.com](https://thezvi.substack.com/p/fable-and-mythos-52-the-system-card)

### 19. AI Futures预测2027年出现超人类AI研究员

![AI Futures预测2027年出现超人类AI研究员](https://3quarksdaily.com/wp-content/uploads/2026/11/AI-Futures-Project-revised-timelines-to-Top-Expert-Dominating-AI-360x189.png)

AI Futures Project团队基于METR的最新估计指出，Anthropic的AI进步速度约为历史水平的两倍，且约80%的加速由AI驱动。这一发现比“AI 2027”情景提前了5个月。团队预测，超人类AI研究员（SAR）很可能在2027年出现，且顶级专家主导型AI（TED-AI）在2028年前出现的概率为35%-65%，暗示智能爆炸可能提前到来。

**重点**：80%加速由AI驱动，超人类AI研究员或2027年现

**来源**：[3 Quarks Daily](https://3quarksdaily.com/3quarksdaily/2026/11/looks-like-the-intelligence-explosion-will-happen-in-2027-after-all.html)

### 20. 华为发布MACaQ本地推理量化器

![华为发布MACaQ本地推理量化器](https://github.com/huawei-csl/MACaQ/raw/main/docs/assets/macaq-banner.png)

华为发布内部量化器MACaQ，支持文本、图像、视频和音频模型的本地推理。该工具兼容llama.cpp、vLLM、Diffusers和PyTorch，能在64分钟内使用32.5GB内存量化122B参数模型，且困惑度优于MR-GPTQ等方案。同时发布MACaQ-R用于优化现有GGUF模型质量，保持与标准llama.cpp兼容，为本地大模型部署提供高效工具。

**重点**：64分钟量化122B模型，兼容主流本地推理框架

**来源**：[Hacker News 首页](https://github.com/huawei-csl/MACaQ)

## Anthropic IPO 与 AI 安全警报

### 21. Anthropic 触发关键 AI 安全警报

![Anthropic 触发关键 AI 安全警报](https://s.yimg.com/lo/mysterio/api/01b23454ce086e707ff095153f8174b56a79651b61e520b0ec39a207cb6d3da6/lightyear_networkapi/resizefill_w80_h80%3Bquality_80%3Bformat_webp/https%3A%2F%2Fs.yimg.com%2Fos%2Fcreatr-images%2FGLB%2F2017-10-19%2F7a9b1550-b504-11e7-8e7b-2b5ad2b1af8b_36dca6e0-a487-11e7-b0d1-0315ed89115a_jcb-nyse.jpg)

Anthropic 在 IPO 前夕宣布触发《负责任扩展政策》中的关键安全警报，认为 AI 加速自身研究的速度已达标。独立机构 METR 证实模型改进速度接近翻倍，且阈值可能在 7 月中旬已突破。这一事件凸显了前沿 AI 模型能力跃升带来的潜在风险，引发业界对 AI 安全治理的广泛关注。

**重点**：AI 自我加速研究速度达标，安全警报提前触发

**来源**：[Hacker News AI](https://finance.yahoo.com/markets/article/anthropic-says-a-key-ai-safety-alarm-has-been-triggered-days-before-its-ipo-171519615.html)

### 22. Anthropic IPO 估值或破 1.5 万亿美元

![Anthropic IPO 估值或破 1.5 万亿美元](https://img.ithome.com/newsuploadfiles/2026/11/4e918d02-22ee-4844-9637-79889b3a9535.jpg?x-bce-process=image/format,f_auto)

据《金融时报》报道，因投资者认购需求旺盛，Anthropic 承销商高盛和摩根士丹利考虑将 IPO 发行价上调至每股 70-78 美元区间之上，目标估值或突破 1.5 万亿美元，募资总额有望超 1000 亿美元。谷歌、英伟达和微软等伙伴将同步进行 260 亿美元私募配售。公司计划投入约 9000 亿美元用于算力建设，10 月年化营收达 810 亿美元。

**重点**：承销商考虑上调发行价，估值预期突破 1.5 万亿美元

**来源**：[IT之家](https://www.ithome.com/1/025/526.htm) · [喷嚏图卦](https://www.dapenti.com/blog/more.asp?name=xilei&id=196693)

### 23. Anthropic 纳斯达克 IPO 细节披露

![Anthropic 纳斯达克 IPO 细节披露](https://ipo.anthropic.com/assets/tree-left-BAK8DIK0.webp)

Anthropic 宣布在纳斯达克进行首次公开募股，股票代码为 ANT，作为公共受益公司，其 Q3 2026 营收达 170 亿美元，同比增长 12 倍。路演将于 11 月 10 日开始，预计 11 月 18 日确定最终价格，11 月 19 日开始交易。文章展示了 Claude 在 Legora、Eli Lilly、Salesforce 等企业的落地案例及财务亮点，显示其在企业级市场的强劲增长势头。

**重点**：Q3 营收同比增长 12 倍，11 月 19 日正式交易

**来源**：[Hacker News 首页](https://ipo.anthropic.com/us/)

## 英伟达 CEO 黄仁勋罢免风波

### 24. 英伟达董事会拟召开紧急会议表决罢免黄仁勋

![英伟达董事会拟召开紧急会议表决罢免黄仁勋](https://techcrunch.com/wp-content/uploads/2026/09/Jensen-Huang.jpg)

据《华尔街日报》报道，英伟达董事会最快于周三召开紧急会议，讨论罢免创始人兼CEO黄仁勋。此前黄仁勋承认与一名据称是中国间谍的女性有婚外情，随后《纽约时报》又报道他与一名下属高管有染。受此丑闻影响，英伟达股价在周三盘后下跌约8%，过去五天累计下跌约11%。

**重点**：全球AI芯片龙头面临最高管理层更迭

**来源**：[TechCrunch](https://techcrunch.com/2026/11/11/nvidias-stock-drops-as-board-reportedly-preps-to-oust-ceo-jensen-huang/) · [Hacker News 首页](https://twitter.com/watcherguru/status/2120645607866188008) · [Hacker News 首页](https://www.wsj.com/business/nvidia-is-preparing-to-oust-nvidia-ceo-jensen-huang-30f421ad)

### 25. 黄仁勋被曝第二段婚外情对象为公司高管

![黄仁勋被曝第二段婚外情对象为公司高管](https://techcrunch.com/wp-content/uploads/2026/09/GettyImages-2294936867.jpg)

《纽约时报》报道，英伟达CEO黄仁勋被指控与医疗保健业务副总裁金伯利·鲍威尔存在婚外情。五名员工称曾在酒店看到两人举止亲密，引发利益冲突争议。这是继黄仁勋承认与疑似中国间谍Alice Huang有染后，再次曝出的私人生活丑闻，进一步加剧了董事会对其领导力的质疑。

**重点**：高管私生活丑闻引发利益冲突争议

**来源**：[TechCrunch](https://techcrunch.com/2026/11/11/jensen-huang-accused-of-having-another-affair-with-a-nvidia-exec/)

### 26. 美国众议院拟就中国间谍恋情传唤黄仁勋

![美国众议院拟就中国间谍恋情传唤黄仁勋](https://techcrunch.com/wp-content/uploads/2026/11/Jensen-Huang.jpg)

据Bloomberg报道，美国众议院共和党人要求Nvidia CEO Jensen Huang就其与疑似中国间谍Alice Huang（Megaspeed高管）的恋情接受闭门简报。若Huang未在周三结束前回应，众议院外交事务委员会等将对其发出传票。此外，民主党参议员要求特朗普政府保留与Nvidia芯片出口及Huang相关通信的文件，以审查国家安全风险。

**重点**：个人丑闻升级为地缘政治与国家安全议题

**来源**：[TechCrunch](https://techcrunch.com/2026/11/11/congress-to-call-jensen-huang-in-to-answer-for-alleged-chinese-spy-affair/)

### 27. 丑闻重创英伟达股价，市值跌至4.19万亿美元

![丑闻重创英伟达股价，市值跌至4.19万亿美元](https://img.ithome.com/newsuploadfiles/2026/11/5d11f5e9-1196-4654-8017-2a93e7c8533b.jpg)

受CEO黄仁勋婚外情丑闻及董事会拟罢免传闻影响，英伟达股价在11月11日美股盘后交易中大幅下挫，跌幅一度达9%，市值降至4.19万亿美元。尽管当日纳斯达克指数及美光、CoreWeave等AI概念股整体上涨，但英伟达因管理层不确定性遭遇重挫。市场预测黄仁勋在2027年7月前离职概率升至80%。

**重点**：管理层不确定性导致股价逆势大跌

**来源**：[IT之家](https://www.ithome.com/1/025/855.htm)

## 英伟达治理危机与芯片供应链震荡

### 28. 外媒盘点英伟达潜在接班人，预测市场留任概率降至30%

![外媒盘点英伟达潜在接班人，预测市场留任概率降至30%](https://img.ithome.com/newsuploadfiles/2025/9/1562f93a-f0f8-4fa7-95b3-912803ba3a84.png?x-bce-process=image/format,f_auto)

受婚外情风波影响，英伟达CEO黄仁勋留任概率在预测市场Kalshi上跌至30%。IT之家报道，外媒Techcrunch列出的潜在接班人包括AMD CEO苏姿丰、前谷歌CEO埃里克·施密特、英特尔CEO陈立武、OpenAI前董事会主席布雷特·泰勒，以及英伟达内部高管伊恩·巴克、安德鲁·贝尔及CFO科莱特·克雷斯。分析指出，英伟达目前无明确继任计划，多位外部巨头高管和内部技术核心人物均被视为可能人选。

**重点**：外部巨头与内部高管均入局接班竞争

**来源**：[IT之家](https://www.ithome.com/1/026/264.htm)

### 29. AI数据中心挤占成熟制程产能，汽车芯片供应链现瓶颈

![AI数据中心挤占成熟制程产能，汽车芯片供应链现瓶颈](https://img.ithome.com/newsuploadfiles/2025/11/d596d79a-d271-4730-b5d0-29a7a382b3e1.png?x-bce-process=image/format,f_auto)

安世半导体与意法半导体高管在Electronica展上警告，AI数据中心需求激增导致晶圆厂将产能转向高利润的AI芯片，减少对汽车和工业用成熟制程芯片的投入。这已造成汽车供应链出现严重瓶颈，安世半导体订单“完全超额”，部分代工厂甚至退出主流技术领域。

**重点**：AI需求挤压传统汽车芯片供应

**来源**：[IT之家](https://www.ithome.com/1/025/588.htm)

## AI 产品发布与前沿应用

### 30. Claude Fable 5.2 突破具身智能，零样本操控真机

Claude Fable 5.2 展示了通用大模型在具身智能领域的重大突破。该模型无需专门训练，即在 RoboDojo 双臂基准测试中以 64.9% 的成功率超越竞品。其核心能力涵盖从 BOM 选型、PCB 布线到 CAD 建模的硬件工程闭环，并能零样本泛化至解魔方、拧瓶盖等真机操作。通过强视觉-空间绑定和长时序规划，它显著降低了新机器人任务的数据成本，尽管在移动具身和极端视觉环境下仍存局限。

**重点**：通用模型首次实现硬件工程闭环与真机零样本操作

**来源**：[Dev.to](https://dev.to/cognitalk/claude-fable-52-embodied-intelligence-overview-e0h)

### 31. Google 发布 Gemini Decisions API，毫秒级多模态决策

![Google 发布 Gemini Decisions API，毫秒级多模态决策](https://storage.googleapis.com/gweb-uniblog-publish-prod/images/decisions-architecture_f0NFXU9.width-1200.format-webp.webp)

Google 推出 Gemini Decisions API 及 Gemini Decision 1 模型，专为快速、校准的多模态封闭集决策设计。该 API 支持文本、图像、音频、视频及 PDF 输入，单次前向传播即可对多达 1,000 个独立问题进行评分，端到端延迟仅 150-250 毫秒。其定价极具竞争力，输入成本约为每百万 token 0.10 美元，输出免费，比 Gemini 3.5 Flash-Lite 便宜近 5 倍。Google 内部已将其应用于 Notebook 动态模型路由、Stitch 快速设计迭代及 Search 安全层等场景，旨在作为低延迟控制平面，无需训练自定义分类器即可实现高效决策。

**重点**：150ms 延迟处理 1000 个选项，成本仅为 Flash-Lite 的 1/5

**来源**：[Google AI Blog](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) · [Hacker News 首页](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) · [Dev.to](https://dev.to/delimitter/google-introduces-gemini-decisions-api-that-scores-1000-closed-set-choices-in-a-single-pass-56om)

### 32. 字节跳动计划推 AI 智能体，对标 Meta Muse 追赶顶尖实验室

![字节跳动计划推 AI 智能体，对标 Meta Muse 追赶顶尖实验室](https://img.ithome.com/newsuploadfiles/2026/11/be30686f-8c6d-4c9c-b78c-074bdc4701e1.png)

据彭博社报道，字节跳动计划在未来几周内推出一款类似 Meta Muse 的 AI 智能体助手，旨在巩固其在 AI 视频生成领域的优势并追赶美国顶尖 AI 实验室。联合创始人张一鸣在内部会议指出，字节 Seed 系列模型的预训练数据规模远小于竞争对手，预计需到 2029-2030 年才能完全对标 OpenAI 和 Anthropic。公司正投入最高 700 亿美元重点发展 Seedance 视频模型，强调不应过度依赖模型蒸馏技术，同时积极招聘 AI 人才以维持长期竞争力。

**重点**：投入 700 亿美元发展 Seedance，预计 2029 年对标 OpenAI

**来源**：[IT之家](https://www.ithome.com/1/025/726.htm)

### 33. 百度文心发布 ERNIE 5.5 Flash Preview，11 月 25 日开源权重

![百度文心发布 ERNIE 5.5 Flash Preview，11 月 25 日开源权重](https://img.ithome.com/newsuploadfiles/2026/11/585e9b07-2a27-438f-8faf-a7d9fe8c2f2d.jpg?x-bce-process=image/format,f_auto)

百度文心发布 ERNIE 5.5 Flash Preview 模型，这是基于 Base 模型的首个后训练版本。该模型总参数 280B，激活参数 14B，支持 1M 上下文，在编程、3D 建模等领域表现优异且解码速度快。API 已在千帆平台上线，权重将于 11 月 25 日前开源。官方称该版本为中间阶段，后续将继续优化，旨在为开发者提供高性能、低成本的开源大模型选择。

**重点**：280B 总参数支持 1M 上下文，即将开源权重

**来源**：[IT之家](https://www.ithome.com/1/025/451.htm)

### 34. 苹果 CarPlay 接入 Gemini，车内支持免提自然对话

![苹果 CarPlay 接入 Gemini，车内支持免提自然对话](https://img.ithome.com/newsuploadfiles/2026/11/076a223c-e97b-4ea5-b095-ce83cc18f603.png)

谷歌宣布苹果 CarPlay 正式接入 Gemini AI 应用，即日起向全球 iOS 用户逐步推送。用户可在车机屏幕通过 Gemini Live 进行免提自然对话，支持随时打断、切换话题及暂停。该功能可连接 Gmail 和 Google 日历，提供日程简报、邮件总结、周边查询及演讲练习等服务。车内对话记录将自动同步至 iPhone 上的 Gemini 应用，方便停车后回看摘要与笔记，极大提升了驾驶场景下的 AI 交互体验。

**重点**：CarPlay 接入 Gemini Live，支持日程简报与邮件总结

**来源**：[IT之家](https://www.ithome.com/1/025/831.htm)

## AI 基础设施与芯片算力

### 35. AMD EPYC 9006 SP7 正式发货，支持 16 通道 DDR5

![AMD EPYC 9006 SP7 正式发货，支持 16 通道 DDR5](https://img.ithome.com/newsuploadfiles/2026/11/db8736bc-7023-4678-8c5f-deba79c22c2e.jpg)

AMD 宣布基于 Zen6/Zen6c 架构的 EPYC 9006 SP7 处理器正式发货。该芯片最高支持 256 核心，默认功耗 600W，配备 16 通道 DDR5 内存（最高 12800MT/s）及 PCIe Gen6 接口。单插槽最大内存容量达 8TB，旨在为数据中心提供高性能、高能效的通用计算能力，进一步巩固其在服务器市场的竞争力。

**重点**：Zen6 架构首发，单插槽 8TB 内存容量

**来源**：[IT之家](https://www.ithome.com/1/025/621.htm)

### 36. 台积电批准 10 亿美元 AI 投资，入股 OpenAI 与 Anthropic

台积电董事会批准高达 10 亿美元的 AI 投资计划，其中分别向 OpenAI 和 Anthropic 各投资不超过 5 亿美元，另授权 5 亿美元成立半导体投资公司。此举不仅加深了台积电与苹果在先进制造产能及 AI 领域的竞争关系，也反映了其对 AI 芯片市场的前瞻性布局，旨在通过资本纽带锁定未来高端芯片需求。

**重点**：直接投资头部 AI 实验室，锁定先进制程产能

**来源**：[Hacker News AI](https://www.macrumors.com/2026/11/11/tsmc-approves-ai-investment/)

### 37. 三星启动 46 万亿韩元 HBM 新产线，2028 年投产

![三星启动 46 万亿韩元 HBM 新产线，2028 年投产](https://img.ithome.com/newsuploadfiles/2026/11/a98a94d3-9cda-4d80-b4c6-e006efd6efa7.jpg)

三星电子在忠清南道牙山市温阳产区启动 HBM 后端先进封装新产线建设，总投资 46 万亿韩元（约 2295 亿元人民币）。项目包含 5 条生产线，计划 2028 年投产，旨在大幅扩大 HBM 产能以支持 AI 芯片需求。韩国总统李在明出席动工仪式，显示政府对半导体产业的高度重视，三星此举意在巩固其在高带宽内存市场的领先地位。

**重点**：巨额投资扩产 HBM，应对 AI 芯片内存瓶颈

**来源**：[IT之家](https://www.ithome.com/1/026/045.htm)

### 38. SpaceX 开发 Kessel 机架，探索服务器“去英伟达化”

![SpaceX 开发 Kessel 机架，探索服务器“去英伟达化”](https://img.ithome.com/newsuploadfiles/2026/11/473bce9b-8233-4154-a82e-289bb350a7e6.png?x-bce-process=image/format,f_auto)

SemiAnalysis 披露 SpaceX 正在开发名为 Kessel 的定制 AI 服务器机架，旨在实现“去英伟达化”的采购模式。该机架保留英伟达芯片但自行采购配套硬件，取消铜缆模块改用 M10 材料的中板。Kessel 将用于地面及太空轨道计算，配合 SpaceX 上调至 13GW 的 2027 年算力目标，但供电仍是主要挑战，体现了巨头对供应链自主权的追求。

**重点**：自研机架硬件，降低对英伟达整体方案依赖

**来源**：[IT之家](https://www.ithome.com/1/025/597.htm)

### 39. IDC：中国液冷服务器收入同比增 153%，转向按柜交付

![IDC：中国液冷服务器收入同比增 153%，转向按柜交付](https://img.ithome.com/newsuploadfiles/2026/11/018c69a8-7b71-44e1-9bc2-005045fb4b76.png?x-bce-process=image/format,f_auto)

IDC 报告显示，2026 年上半年中国液冷服务器收入同比增长 153.1%，未来五年出货量年均复合增长率预计接近 49%。采购模式正从按“台”转向按“柜”交付，机柜成为算力采购单元。互联网企业占采购量 65.6%，冷板式液冷占比 90.2%。受 AI 推理负载增加影响，整柜交付在中国占比目前为 5.0%，远低于北美的 47.4%，但正成为锁定算力的重要路径。

**重点**：液冷市场爆发，整柜交付成为算力锁定新趋势

**来源**：[IT之家](https://www.ithome.com/1/025/599.htm)

### 40. Diraq 全球首台硅自旋量子计算机落地商业数据中心

![Diraq 全球首台硅自旋量子计算机落地商业数据中心](https://img.ithome.com/newsuploadfiles/2026/11/7a57294f-aea8-4a9d-be1f-8ed7886cb777.jpg)

量子计算企业 Diraq 宣布在 Equinix 悉尼数据中心投运全球首台硅自旋量子计算机。该技术采用半导体工艺，无需大幅改造基础设施即可升级 QPU。当前系统功耗低于 20kW，占地约 16 平方米，预计一年内从 8 量子比特扩展至 64 量子比特。未来公用事业级系统功耗约 300kW，占地可降至 5 平方米，部署密度更高，标志着量子计算向商业化部署迈出关键一步。

**重点**：半导体工艺量子计算机，低功耗高密度部署

**来源**：[IT之家](https://www.ithome.com/1/025/608.htm)

### 41. IBM 发布 Nighthawk r3，计划 2027 年超千比特系统

![IBM 发布 Nighthawk r3，计划 2027 年超千比特系统](https://img.ithome.com/newsuploadfiles/2026/11/9afeaa4d-f88f-4c2d-83b8-39300edf2cbe.jpg)

IBM 发布下一代量子处理器 Nighthawk r3，支持 520 个可编程量子比特执行 1 万次量子操作。该处理器采用 l-couplers 耦合技术，计划于 2027 年连接两颗芯片组成超 1000 量子比特系统。IBM 还验证了模块化量子计算关键技术，量子态传输保真度达 99.3%，并成功整合低温模块，为扩大量子计算规模奠定基础，展示了其在量子霸权路径上的持续进展。

**重点**：模块化设计验证成功，迈向千比特量子系统

**来源**：[IT之家](https://www.ithome.com/1/025/787.htm)

### 42. 英特尔 256 核 Diamond Rapids 曝光，定位智能体 AI 基础设施

![英特尔 256 核 Diamond Rapids 曝光，定位智能体 AI 基础设施](https://img.ithome.com/newsuploadfiles/2026/11/3342baa3-5f0e-4090-9923-29b039ef0e55.png)

英特尔下一代至强 7 处理器 Diamond Rapids 实物样品首次曝光。该芯片采用 18A-P 工艺和 Panther Cove-X 架构，最高配备 256 个性能核、1.28GB 末级缓存，支持 16 通道 MRDIMM 内存及 128 条 PCIe 6.0 通道。英特尔将其定位为面向智能体 AI 基础设施的 CPU，预计 2027 年推出，适配 LGA 9324 插槽，旨在通过高核心数和先进内存支持复杂 AI 工作负载。

**重点**：18A 工艺首发，专为智能体 AI 工作负载优化

**来源**：[IT之家](https://www.ithome.com/1/025/878.htm)

### 43. 百度发布天池 1024 卡超节点，支撑 5 万亿参数模型训练

![百度发布天池 1024 卡超节点，支撑 5 万亿参数模型训练](https://img.ithome.com/newsuploadfiles/2026/11/9fc2b7bd-3c14-49ca-827b-bb5e4986fde8.jpg)

百度在 2026 世界大会发布天池 1024 卡超节点，明年上市。该集群采用光引擎技术，互联带宽提升 3 倍，训练性能提升 2.5 倍，推理性能提升 3 倍。配套 G3.5 KV Cache 加速柜，长上下文推理性能提升 2 倍，TTFT 降低 90%。单套可支撑 5 万亿参数模型训练，并具备扩展至万卡规模的能力。相比去年计划，上市节奏提前一年，显示百度在 AI 基础设施领域的加速布局。

**重点**：光引擎提升互联带宽，提前一年上市节奏

**来源**：[IT之家](https://www.ithome.com/1/026/026.htm)

## AI 安全与漏洞披露

### 44. Apache HTTP/2 曝出严重 RCE 漏洞

Wiz 披露 Apache HTTP Server 存在严重远程代码执行漏洞（CVE-2026-119618），源于 HTTP/2 模块中的竞态条件。未认证攻击者可利用该漏洞破坏堆内存并执行任意代码。数据显示 64% 的云环境受影响，建议升级至 2.4.71 或禁用 HTTP/2 作为临时缓解措施。

**重点**：影响广泛，需立即升级或禁用 HTTP/2

**来源**：[Hacker News 首页](https://www.wiz.io/blog/cve-2026-119618-rce-apache-http-server-vulnerability) · [极客洞察](https://newshacker.me/story?id=50462177) · [The Hacker News](https://thehackernews.com/2026/11/critical-apache-http2-flaw-could-let.html)

### 45. 超 3.5 万个 Grok 生成应用在线暴露

![超 3.5 万个 Grok 生成应用在线暴露](https://image.3001.net/images/20261111/1794406319055706_b017e4a1c3f24f4db1a4ee93160407e4.jpg!small)

安全公司 Claroc 发现超 3.5 万个由 Grok 生成的应用默认公开暴露，其中包含 X 及 SpaceXSI 员工搭建的应用，泄露了机密销售数据、员工名单甚至明文密码。研究指出 Grok 应用默认权限为“知道链接的任何人”，且存在代码逻辑缺陷导致未授权用户可篡改数据。

**重点**：AI 生成应用默认权限设置存在重大安全隐患

**来源**：[FreeBuf](https://www.freebuf.com/articles/ai-security/512031.html)

### 46. 微软借助 AI 发现 59 个 Linux 内核漏洞

![微软借助 AI 发现 59 个 Linux 内核漏洞](https://image.3001.net/images/20200701/1593550745.png!small)

微软 FORGE 实验室利用 AI 工具 MDASH 在 Linux 内核中发现 59 个安全漏洞，其中部分潜伏超 20 年。已分配 33 个 CVE，8 个证实存在本地 root 提权路径。扫描产出 2.6 万条原始结果，经多轮 AI 与人工校验后保留 59 个有效报告，修复补丁合入主线中位周期 41 天。

**重点**：AI 显著提升漏洞挖掘效率，但人工确认成本高

**来源**：[FreeBuf](https://www.freebuf.com/articles/system/512145.html)

### 47. 新型 GhostFrame 恶意软件劫持 VMware ESXi

![新型 GhostFrame 恶意软件劫持 VMware ESXi](https://image.3001.net/images/20261111/1794374009596904_c601024e7584428a8c7d1dc156966e74.webp!small)

Insikt Group 发现新型 GhostFrame 恶意软件，可劫持 VMware ESXi 服务器。该工具无需在虚拟机内部运行程序，即可通过修改底层配置和内存扫描窃取 Windows 凭证。其部署需 ESXi root 权限，具备无文件驻留、伪装进程及多端口 C2 连接特征，常利用 VPN 设备漏洞作为初始入口。

**重点**：虚拟化环境面临新型无文件驻留威胁

**来源**：[FreeBuf](https://www.freebuf.com/articles/system/511912.html)

### 48. 微软发布补丁修复 1259 个漏洞

![微软发布补丁修复 1259 个漏洞](https://image.3001.net/images/20261111/1794388866330391_6f96a8d20fc647acb4d63cc6f6732479.jpg!small)

微软发布月度安全补丁，修复 1259 个漏洞，其中包含一个已遭在野利用的 Outlook 中等严重度漏洞（CVE-2026-124194）。该漏洞允许攻击者通过特制邮件文件诱导用户点击，从而泄露 NTLMv2 哈希并冒充用户身份。CISA 已将其列入 KEV 目录，要求联邦机构在 2026 年 11 月 24 日前完成修复。

**重点**：Outlook 漏洞已遭利用，需优先修补

**来源**：[FreeBuf](https://www.freebuf.com/news/511981.html)

## 趋势观察

AI 行业正从单纯的技术竞赛转向**资本化与治理化**的深水区。Anthropic 的高估值与安全警报并存，英伟达的管理层动荡，预示着**智能体**时代的竞争将更多取决于供应链自主权、模型安全审计及组织稳定性，而非单一性能指标。

---

*本报告由 RSS-Claw 岛屿日报 AI 自动生成*


---

## 📎 产品机会雷达 · 2026-11-12

### 📈 已有机会的新进展

- **Agent Skills 生态爆发：从编码到安全审计的标准化**
  📈 **进展**：新增 OpenAI Codex Security 官方技能包、营销技能包及中文小说创作技能包，显示 Skills 正成为 AI 智能体能力扩展的标准接口，且应用场景从工程向内容创作和安全合规延伸。
  🗓️ **首次/上次记录**：2026-11-11
  > 通过标准化技能包（Skills）将垂直领域最佳实践注入 AI 智能体，实现从通用编码到专业审计的跨越。
  **目标用户**：使用 AI 编码智能体进行特定领域开发（如安全、金融、设计）的专业人士
  **痛点**：通用 AI 编码智能体在特定垂直领域缺乏领域知识和最佳实践，导致输出质量不稳定或需要大量人工修正，且缺乏标准化的技能分发和验证机制。
  **为什么现在**：OpenAI 官方发布 Codex Security 技能包，且社区涌现出营销、中文小说等垂直技能，表明标准化接口已获大厂认可，生态进入爆发期。
  **1周验证**：发布一个针对特定垂直领域（如 SEO 或 财务审计）的 Skill 包，观察 GitHub Star 增长及开发者下载量。
  **MVP 功能**：技能包标准格式定义；垂直领域技能市场（安全、营销、创作）；技能包版本管理与分发
  **变现**：技能包订阅或按次付费，企业版提供私有技能库托管
  **证据**：github-trending-js:PenglongHuang_chinese-novelist-skill, github-trending-js:addyosmani_agent-skills, github-trending-js:coreyhaines31_marketingskills, github-trending:openai_codex-security, v2ex:create:1256542
  *分类：AI 开发工具*

- **Astryx: Agent-Ready 设计系统**
  📈 **进展**：Meta 开源 Astryx 设计系统，强调其“fully customizable and agent ready”，为 AI 智能体提供了官方级别的设计规范接口，进一步验证了设计系统与 Agent 集成的趋势。
  🗓️ **首次/上次记录**：2026-11-11
  > 通过标准化的组件定义和元数据，让 AI 智能体能够直接调用并生成符合设计规范的 UI 代码。
  **目标用户**：使用 Claude Code、Cursor 等 AI 编码智能体进行前端开发的工程师及设计师
  **痛点**：现有 AI 编码工具缺乏对设计系统底层规范的直接感知能力，导致生成的 UI 在视觉一致性和可交付性上存在“最后一公里”差距。
  **为什么现在**：Meta 官方发布 Astryx，标志着大厂开始将“Agent-Ready”作为设计系统的核心属性，而非仅仅是人类开发者使用的组件库。
  **1周验证**：基于 Astryx 构建一个 Demo，展示 AI 智能体如何直接读取其元数据生成符合规范的 React 组件。
  **MVP 功能**：Agent-Ready 组件元数据标准；设计 Token 自动同步；AI 生成 UI 的视觉一致性校验
  **变现**：开源核心 + 企业版设计系统托管与合规检查服务
  **证据**：github-trending:meta_astryx
  *分类：AI 开发工具*

- **AI 智能体远程操控：从“跨设备共享”到“iPhone 远程 Mac”与“本地优先工作台”**
  📈 **进展**：CopilotKit 推出 OpenBot，允许 AI 智能体拥有独立的浏览器和文件环境，并记录所有操作；Orkas 推出本地优先的 AI 团队管理器，支持 16 个内置专家智能体。这些进展表明智能体正从“代码助手”向“拥有独立工作空间的数字员工”演进。
  🗓️ **首次/上次记录**：2026-10-31
  > 提供移动端（iPhone）和本地优先（OpenBot）的 AI 智能体远程监控与控制工具，实现“随时随地”管理 Agent。
  **目标用户**：需要在不同设备间切换或远程监控 AI 智能体执行过程的开发者
  **痛点**：AI 智能体通常在本地终端或 IDE 中运行，当用户离开电脑或想在另一台设备上查看/控制智能体状态时，缺乏一种轻量级、低延迟的“智能体专用”远程桌面方案。
  **为什么现在**：CopilotKit 发布 OpenBot，提供开源的 AI 同事（拥有独立浏览器、文件、工具）；Orkas 提供本地优先的桌面 AI 团队管理。两者都强化了“智能体拥有独立计算环境”的概念。
  **1周验证**：开发一个 iOS 客户端，连接 OpenBot 或 Orkas，实现远程查看 Agent 正在执行的网页操作。
  **MVP 功能**：移动端 Agent 状态监控；独立浏览器/文件沙箱环境；操作日志回放与审计
  **变现**：SaaS 订阅，按 Agent 数量或并发连接数计费
  **证据**：github-trending-js:Orkas-AI_Orkas, github-trending:CopilotKit_OpenBot
  *分类：AI 基础设施*

- **LLM 价格战下的“本地优先”与“免费模型”路由策略**
  📈 **进展**：GitHub 趋势榜出现 free-claude-code 项目，聚合多个免费/低成本 AI 编码工具；V2EX 社区热议 Google AI Pro 小号被封及 Claude 防封策略，显示开发者对 AI 订阅成本和账号稳定性的焦虑加剧，催生了新的工具和服务需求。
  🗓️ **首次/上次记录**：2026-11-06
  > 通过动态路由和缓存优化，在模型价格战中自动选择性价比最高的 LLM 组合。
  **目标用户**：对 AI 编码订阅费用敏感的个人开发者、初创团队
  **痛点**：主流 AI 编码工具默认绑定昂贵的高性能模型，导致 Token 成本居高不下。
  **为什么现在**：出现专门聚合免费/低成本模型（如 Claude Code, Codex, Antigravity 等）的工具，以及针对 Google AI Pro 封号问题的“物理防封”策略讨论，显示成本优化已从“路由”扩展到“账号生存”。
  **1周验证**：构建一个 CLI 工具，自动检测当前可用的免费模型额度，并在额度耗尽时自动切换至下一个可用模型。
  **MVP 功能**：多模型免费额度聚合器；账号健康度监控与防封策略；基于任务复杂度的动态模型路由
  **变现**：免费开源 + 高级路由策略订阅，或按节省成本比例抽成
  **证据**：github-trending:Alishahryar1_free-claude-code, v2ex:share:1256483, v2ex:share:1256508
  *分类：AI 开发工具*

- **Agent 长期记忆层：从开源 SDK 到云厂商标准化服务**
  📈 **进展**：V2EX 分享 continue-with-x.skill，允许在不同 AI 工具间传递上下文和开发任务；即刻讨论组分享有道开源办公 Agent 的团队版 Token 管理功能。这些进展表明记忆基础设施正从个人助手向团队协作和跨平台互操作方向扩展。
  🗓️ **首次/上次记录**：2026-11-11
  > 提供独立的 Memory 层，自动提取对话关键信息构建用户画像，并支持跨工具的状态交接。
  **目标用户**：构建 Personal Agent 或企业级 AI 应用的开发者
  **痛点**：AI 智能体在跨会话交互中缺乏持久化记忆，导致重复询问或无法个性化，现有 RAG 方案难以解决“记忆”与“学习”问题。
  **为什么现在**：记忆层从“存储”向“跨工具状态交接”和“团队 Token 管理”演进，出现专门解决多 Agent 协作中上下文断裂问题的开源项目。
  **1周验证**：开发一个 Skill，允许用户在 Claude Code 中保存当前任务状态，并在 Cursor 中一键恢复，验证跨工具记忆迁移的可行性。
  **MVP 功能**：跨工具上下文迁移协议；团队级 Token 与记忆共享；用户画像自动提取与更新
  **变现**：开源核心 + 企业版团队记忆托管服务
  **证据**：jike-ai-discuss:PVSPffN6KC49hC8-PSb1QA, v2ex:programmer:1256444
  *分类：AI 基础设施*


### 📡 待验证信号

- **VS Code 扩展 Berth: 多 Agent 会话侧栏管理**

- **Apple Harbor: Mac 私有 AI 推理服务器**

- **GPT 模型质量争议与 Token 消耗焦虑**

- **Pipeline Lens: 本地模拟 GitLab CI**


### 🔨 本周建议动手

- **构建“跨工具 Agent 记忆” Skill**

- **开发“免费模型额度聚合器” CLI**

- **基于 Astryx 构建 Agent-Ready UI 生成 Demo**



---

## 📎 arXiv Artificial Intelligence · 2026-11-12

### 📄 论文列表

- **医学图像分割：基础模型适配与任务特定训练的比较**
  *Medical Image Segmentation: Foundation Model Adaptation versus Task-Specific Training*

  📄 `arXiv:2611.14519` · cs.CV, cs.AI
  👥 **作者**：Emre Kutlusan, Yongmin Li
  🏛️ **单位**：Department of Computer Science, Brunel University of London, Uxbridge, UB8 3PH, United Kingdom
  📝 **摘要**：本研究探讨了在医学图像分割中，基于大规模自然图像预训练的基础模型（DINOv2）与从头训练的任务特定模型（U-Net, ResU-Net）之间的性能差异。实验涵盖结肠镜、乳腺超声和皮肤镜检查，并在训练源保留数据及来自其他机构的独立数据集上进行测试。结果显示，适配后的基础模型在所有外部数据集上均表现出更好的泛化能力。在训练分布内，当数据充足时，任务特定模型在边界描绘上更精确，而基础模型更容易遗漏小病灶。研究发现，仅需适配基础模型的一小部分参数即可达到良好效果，且所需容量由成像领域决定而非适配方法。此外，还发现一个广泛使用的息肉测试集存在与其他基准重复图像的问题。结论表明，在需要跨站点部署的场景中，基础模型适配是合理的，应根据目标领域选择模型容量。
  🔗 [PDF](https://arxiv.org/pdf/2611.14519v1)

- **通过EM-DETR中的基于示例的定位迈向基础检测模型**
  *Toward Foundation Detection Models via Example-Based Grounding in EM-DETR*

  📄 `arXiv:2611.14518` · cs.CV, cs.AI
  👥 **作者**：Sheethal Bhat, Bogdan Georgescu, Awais Mansoor, Florin C. Ghesu, Sasa Grbic, Andreas Maier
  🏛️ **单位**：Friedrich-Alexander-Universität, 91058, Erlangen-Nürnberg, Germany, Siemens Healthineers, 91052, Erlangen, Germany, Siemens Medical Solutions, 08540, Princeton, USA
  📝 **摘要**：针对医学病灶检测中高质量标注数据稀缺及数据集异质性限制基础模型发展的问题，本文提出了一种构建多领域医学图像检测基础模型的新方法。该方法整合了包含解剖结构和异常标注的多样化医学图像数据集。首先，提出了一种学生-教师训练策略，有效结合具有异构标签空间的数据集，缓解灾难性遗忘并改善特征学习。其次，基于先前提出的基于示例的EM-DETR框架，将其扩展为能从多个领域特定数据集中联合学习，实现跨模态的细粒度、示例驱动的检测。实验结果表明，该模型在胸片（CXR）的四个关键发现上，图像级AUC得分超过此前最先进（SOTA）水平1个百分点；在胸片和乳腺摄影中取得了领先的mAP50，比单数据集训练的EM-DETR高出2-3个百分点。该研究为利用异构数据构建可扩展、鲁棒且具泛化能力的医学影像基础模型铺平了道路。
  🔗 [PDF](https://arxiv.org/pdf/2611.14518v1)

- **对比发现：基于竞争性解释的开放式科学发现**
  *Contrastive Discovery: Open-Ended Scientific Discovery over Competing Explanations*

  📄 `arXiv:2611.14514` · cs.AI, cs.CL, cs.LG
  👥 **作者**：Ziang Liu, James J. Kim, Yijia Dai, Jennifer J. Sun
  🏛️ **单位**：Department of Computer Science, Cornell University
  📝 **摘要**：大语言模型（LLM）智能体在开放式数据驱动的科学发现中应用日益广泛，但现有方法通常仅针对单一假设及其补集进行点式评估，导致当证据拒绝假设时，智能体无法确定证据支持的具体替代解释。为此，本文提出“对比发现”（Contrastive Discovery）框架，用“对比集”替代单一假设，即由一个科学问题和一组互斥且穷尽的竞争性解释组成。每个实验通过证据在对比集内重新分配信念来评分，当信念集中于某一解释时问题即被解决。由于对比集仅改变智能体提出和评分的单位，现有智能体可利用其重新评估已收集的证据或引导搜索。在六个领域的实验中，89%的点式最大信念变化候选项为拒绝；在相同证据下，对比集将其中73%的候选项解决为特定替代解释。当对比集引导搜索时，智能体在相同实验预算下比点式惊讶度多解决67%的问题。盲测显示，38名人类专家在78%的已解决问题上选择了相同解释。
  🔗 [PDF](https://arxiv.org/pdf/2611.14514v1)

- **智能体评估框架的比较分析：企业分析智能体中的稳定性、检测与发现**
  *Comparative Analysis of Agent Evaluation Frameworks: Stability, Detection, and Discovery in Enterprise Analytics Agents*

  📄 `arXiv:2611.14493` · cs.AI, cs.CL, cs.LG, cs.SE
  👥 **作者**：Howard Zhang, Chuck Arvin, Logan Brown, Mihir Bhatia, Neelu Choudhary, Lily Miao
  🏛️ **单位**：Amazon, New York, NY, USA, Amazon, Washington, DC, USA, Amazon, Austin, TX, USA
  📝 **摘要**：在企业环境中部署基于LLM的分析智能体需要能够可靠检测复杂多工具工作流中故障的评估框架。本文对三种代表不同评估范式的框架进行了三阶段比较研究：基于轨迹的LLM评判、仅文本的LLM评判（含红队测试）以及确定性启发式方法，应用于两个分析智能体并使用冻结的执行轨迹。第一阶段量化评估框架的稳定性，发现97%的配置满足稳定性阈值，且稳定性模式与智能体无关。第二阶段测量已知风险检测能力，在72个真值测试用例中，基于轨迹的框架取得了最佳精确率-召回率平衡（F1=0.90），而仅文本评估虽召回率相当，但误报率高出5倍。第三阶段评估未知风险发现，发现了24个新型故障，且功能测试与安全红队测试之间零重叠。结果表明，评估框架可用的信息决定评估质量，功能与安全评估互补，且LLM评估框架能发现人类审查者遗漏的细微错误。建议采用双框架策略：基于轨迹的评估用于功能评估，对抗性红队测试用于安全验证。
  🔗 [PDF](https://arxiv.org/pdf/2611.14493v1)

- **ReTrace：将工具使用智能体蒸馏为无规划器工作流**
  *ReTrace: Distilling Tool-Using Agents into Planner-Free Workflows*

  📄 `arXiv:2611.14492` · cs.AI, cs.LG, cs.MA
  👥 **作者**：Kaiyuan Hou, Yang Ping Kuo, Indranil Bhattacharya, Rohith Nama, Arushi Gupta, Carlos D. Castillo, Prathap Ramachandra, Xiaofan Jiang, Francesco Carbone
  🏛️ **单位**：Columbia University, Amazon
  📝 **摘要**：业务流程自动化通常对相同的标准操作程序（SOP）重复执行。虽然LLM智能体可以遵循自然语言编写的SOP，但每次运行都需调用LLM选择步骤，增加了延迟和成本。本文提出ReTrace，将SOP和少量记录的智能体运行转化为可复用的工作流，其中由代码而非LLM选择下一步。ReTrace提取智能体推理中每个步骤背后的条件，将这些条件合并为紧凑的规则文档，并生成可执行工作流。仅最后阶段依赖平台，因此规则文档可编译为不同编排平台。在79个生产平台流程中，ReTrace工作流达到93.8%的完成率（智能体为96.8%），每任务成本低24%。在τ²-Bench上，ReTrace达到75.8%的任务成功率（智能体为80.6%），运行时间从170秒缩短至1.3秒；通过三轮修复，k=2工作流成功率从66.7%提升至81.2%。在SOP-Bench的8个流程中，ReTrace经修复后达到87.8%的成功率，每任务耗时0.40秒，优于智能体的85.5%和46.6秒。
  🔗 [PDF](https://arxiv.org/pdf/2611.14492v1)



---

## 📎 arXiv Machine Learning · 2026-11-12

### 📄 论文列表

- **TorchCurves：可微参数曲线**
  *TorchCurves: Differentiable Parametric Curves*

  📄 `arXiv:2611.14516` · cs.LG, stat.ML
  👥 **作者**：Alex Shtoff
  📝 **摘要**：本文提出了 TorchCurves，一个将向量值参数曲线视为可学习原语的 PyTorch 库。其核心操作是将标量输入批次映射到以 B 样条或勒让德多项式基表示的曲线点，并支持对输入和系数进行反向传播。曲线系数可与周围模型联合优化，或由另一个网络生成。该库提供了可训练模块、可复用基模块和函数式接口，支持从连续特征嵌入到 Kolmogorov-Arnold 网络（KAN）及函数回归等多种应用。实现上结合了经典评估算法与向量化 PyTorch 操作，强调可读性和可维护性，无需自定义硬件内核。计时实验对比了曲线评估与 NumPy/SciPy 的性能，以及 KAN 训练与 EfficientKAN 的效率，展示了该通用性在计算上的实际可行性及开销情况。
  🔗 [PDF](https://arxiv.org/pdf/2611.14516v1)

- **AutoScaffold：用于语言模型强化学习的 AI 引导支架**
  *AutoScaffold: AI-Guided Scaffolding for Reinforcement Learning of Language Models*

  📄 `arXiv:2611.14515` · cs.LG, cs.CL
  👥 **作者**：Zijian Zhang, Rizhen Hu, Jiangweizhi Peng, Shiyang Li, Sujay Bhatt, Sihan Zeng, Mingyi Hong
  🏛️ **单位**：University of Minnesota, Twin Cities, JPMorgan AI Research
  📝 **摘要**：针对可验证奖励强化学习（RLVR）中结果奖励信息利用率低的问题，本文提出了 AutoScaffold，一个统一的 AI-for-AI 框架，将学生的训练经验转化为自适应支架，无需人工干预。冻结的教师模型定期诊断瓶颈，设计两类支架：跨任务共享的策略和针对困难任务的提示，并随学生进步动态调整。在 ALFWorld、搜索问答、数学推理和 GPU 内核生成四个领域，移除支架后的评估显示 AutoScaffold 训练的学生均优于对应 RL 基线。具体而言，ALFWorld 成功率提升 7.2 点，QA 精确匹配率提升 4.0 点，GPU 内核生成中正确且快于 PyTorch 参考的内核比例提升最多 5.0 点。分析表明，教师能识别不同任务类的失败原因，并从逐步工作流转向针对性修复，显著提升了学习效率。
  🔗 [PDF](https://arxiv.org/pdf/2611.14515v1)

- **Pyrite：构建与基准测试蛋白-配体构象排序智能体**
  *Pyrite: Building and Benchmarking Protein-Ligand Pose Ranking Agents*

  📄 `arXiv:2611.14511` · cs.LG, q-bio.QM
  👥 **作者**：Megha Srivastava, Michael H. Lim, Allison M. Keys, Pranav Murugan, Nate Gruver
  🏛️ **单位**：Stanford University, Genesis Molecular AI
  📝 **摘要**：本文介绍了 Pyrite，一个包含 1,500 个蛋白-配体复合物构象对的成对排序基准，旨在解决共折叠模型生成多样候选构象后难以可靠排序的问题。实验显示，配备 3D 可视化和物理评分工具的专家化学家表现接近随机，凸显了解释化学信号的难度。为此，作者提出了 PyriteRep 结构化表示，并开发了两个基于 LLM 的智能体：PyriteReasoner 通过文本推理直接比较构象，PyriteFeaturizer 生成可执行代码构建逻辑回归特征。结果显示，PyriteFeaturizer 达到 74% 的准确率，PyriteReasoner 达到 67%，均超过专家表现。LLM 引导的特征发现通常优于直接推理，且通过组相对策略优化（GRPO）改进的开源模型可匹敌或超越闭源前沿模型。
  🔗 [PDF](https://arxiv.org/pdf/2611.14511v1)

- **真实连接组何时胜出？针对未测量生理学的连接组结构-功能主张测试**
  *When Does the Real Wiring Win? Testing connectome structure-function claims against unmeasured physiology*

  📄 `arXiv:2611.14508` · cs.LG, q-bio.NC
  👥 **作者**：Yeyuan Liu
  🏛️ **单位**：University of Virginia
  📝 **摘要**：本文探讨了连接组约束模型中结构决定功能的主张，指出此类比较常混淆连接组结构与模型调优（如兴奋性、增益、可塑性率）。作者分离了三种估计量：P1（在真实连接组上调优后迁移到空模型）、P2（每种连接组独立调优）和 P3（限制于与独立数据一致的生理学的 P2）。利用合成真值、安慰剂空模型和三个果蝇电路模型，研究发现部分主张（如分离的奖励/惩罚多巴胺改善学习）在所有协议下均成立，但其他主张则不然。例如，在蘑菇体中，真实 Kenyon 细胞输出连接组在 P1 和 P2 下优于跨亚型身份洗牌，但在 P3 下表现更差，这暴露了模型的不充分性而非果蝇连接组的缺陷。可信的结构主张需要匹配的优化、数据约束的生理学以及在该条件下仍有效的模型。
  🔗 [PDF](https://arxiv.org/pdf/2611.14508v1)

- **Continual-ARC：衡量工作生涯中的技能获取**
  *Continual-ARC: Measuring Skill Acquisition over a Working Lifetime*

  📄 `arXiv:2611.14505` · cs.LG
  👥 **作者**：Daniel Lenton
  🏛️ **单位**：unify
  📝 **摘要**：针对现有持续学习基准局限于单一领域、单次实例服务及单一学习者类型的缺陷，本文提出了 Continual-ARC，一个基于 ARC-AGI 三个版本构建的终身任务流。该基准无需领域知识，同一任务在休眠间隙后以新实例返回，同时新任务不断到达。学习者可在每个实例中支付演示费用、提交答案或在框架内行动，错误提交允许重试但需付费，评分基于消耗的反馈预算比例。由于学习者可在实例间保留任何内容，基于记忆和基于权重的系统在同一尺度上比较。实验在 Qwen3.5-9B 和 GLM-5.3 Flash 上运行冻结权重的智能体框架，结果显示：除非提供显式专家指导，框架中的持久性通常不会改善记忆；大多数基于框架的方法学习到的内容少于仅缓存演示的基线；基于框架的方法在未见任务上无增益，而基于权重的学习显示出显著增益，为未来基于权重的持续学习开辟了新途径。
  🔗 [PDF](https://arxiv.org/pdf/2611.14505v1)



---

## 📎 arXiv Computation and Language · 2026-11-12

### 📄 论文列表

- **机制可解释性需要推理逻辑**
  *Mechanistic Interpretability Needs a Logic of Inference*

  📄 `arXiv:2611.14483` · cs.CL, cs.CV
  👥 **作者**：Zhimin Hu, Chen Jiang, Hanbo Xie, N. Apurva Ratan Murty, Sashank Varma
  🏛️ **单位**：Georgia Tech, McGill University
  📝 **摘要**：本文探讨了机制可解释性（MI）研究从观察模型内部组件到构建机制解释的推理瓶颈。作者对比了神经科学与MI在理解复杂神经网络时的平行努力，指出当前缺乏从可解释性结果到形式化机制主张的通用逻辑。为此，论文提出了五项原则，并将其组织为一种递归推理逻辑，旨在建立更严谨的机制推断程序。该框架有助于将局部的可解释性发现转化为模型内部机制的累积知识，并使这些机制足够精确以生成关于模型外部领域的可测试假设。文章强调，最终需要MI之外的证据来确立模型机制对现实世界的揭示。
  🔗 [PDF](https://arxiv.org/pdf/2611.14483v1)

- **Pterodactyl：推动高效自动翻译评估的极限**
  *Pterodactyl: Pushing the Limits of Efficient Automated Translation Evaluation*

  📄 `arXiv:2611.14480` · cs.CL
  👥 **作者**：Evelyn Y. Garland, Carola F. Berger
  🏛️ **单位**：1020 Group, Acta Language Services, LLC, CFB Scientific Translations LLC
  📝 **摘要**：本文介绍了1020 Group在WMT26自动质量评估共享任务中的提交系统Pterodactyl。该系统专为子任务2（片段级质量分数预测）和子任务3（无错误片段检测）设计，是一个高度可定制、超低成本的系统，优化用于翻译分诊和数据策展中的二元分类。Pterodactyl基于“LLM作为评委”的方法，其提示工程和模型选择由ROC分析指导。作者还开发了针对子任务3特别调整的Pterodactyl变体。该研究旨在通过更快的模型和提示配置，在保持任务特定性能的同时，推动自动翻译评估的成本-性能前沿，实现高效的生产导向策略。
  🔗 [PDF](https://arxiv.org/pdf/2611.14480v1)

- **FERN：基于冻结检索器和学习排序的跨基准Text-to-SQL表格检索**
  *FERN: Cross-Benchmark Table Retrieval for Text-to-SQL with Frozen Retrievers and Learned Ranking*

  📄 `arXiv:2611.14477` · cs.IR, cs.CL
  👥 **作者**：Arjun Rao, Nishant Gopinath
  🏛️ **单位**：SAP
  📝 **摘要**：针对大型合并目录中的Text-to-SQL系统，本文提出FERN（无生成式LLM的特征工程排序）方法，用于检索问题所需的表格。FERN融合三个冻结检索器生成100个候选项，利用最多120个特征描述每个候选项，并使用仅在BIRD训练集上拟合一次的LightGBM排序器进行重排。实验显示，在未拟合的Spider基准上，FERN的候选池召回率达到了RASL在15个表格时的水平，且排序器将complete@5从83.9%提升至95.6%。在BIRD和Fiben基准上，FERN在低延迟（单A100上中位208ms）且无需托管模型调用的情况下，展现了与基于生成式LLM的方法相当或更优的检索性能，特别是在非检索特征对complete@5的提升方面。
  🔗 [PDF](https://arxiv.org/pdf/2611.14477v1)

- **文本编码何时对语言建模重要？**
  *When does text encoding matter for language modeling?*

  📄 `arXiv:2611.14459` · cs.CL
  👥 **作者**：Eugene Jang, Catherine Arnett, Terra Blevins
  🏛️ **单位**：Khoury College of Computer Sciences, Northeastern University, EleutherAI
  📝 **摘要**：本文调查了文本编码对字节级语言模型性能的影响，比较了UTF-8与其他Unicode策略、语言特定编码及自定义编码。作者提出了Aether混合编码方案，针对目标设置使用脚本特定编码，同时通过UTF-8回退保持完整的Unicode覆盖，并用于建模四种正字法多样的语言。研究发现，信息密度高的语言（如中文、韩文）从压缩编码中显著受益，而单个字符信息量较低的语言（如格鲁吉亚文、泰米尔文）对编码选择 largely 不敏感。基于此，论文论证文本编码应作为语言特定的设计决策，而非通用默认标准，以解决UTF-8可变长度设计带来的跨语言不平等。
  🔗 [PDF](https://arxiv.org/pdf/2611.14459v1)

- **Earlybird：29M参数下的预测式流式语音识别**
  *Earlybird: Predictive Streaming Speech Recognition in 29M Parameters*

  📄 `arXiv:2611.14421` · cs.SD, cs.CL, eess.AS
  👥 **作者**：Sahil Mahendrakar
  📝 **摘要**：本文提出Earlybird，一个仅含29M参数（4位量化后16.8 MB）的流式语音识别器，旨在解决传统流式模型在说话人结束单词后90-400ms才输出结果的延迟问题。Earlybird通过从随机截断的音频（包括单词中间）学习，预测截至该时刻应输出的所有完整单词，并猜测接下来的两个单词。其原始token概率为每个单词（包括正在说话的）提供置信度。在LibriSpeech test-clean上，其中位单词在说话人结束前90ms即被正确预测，而现有模型则在结束后90-400ms才输出。在六个测试集上，Earlybird均实现了最早的预测时间，69%的单词在结束前被正确预测，且置信度校准良好（ECE 3.7-5.5）。在Open ASR Leaderboard上，其准确率优于Moonshine Tiny，并与同规模的Whistle相当。
  🔗 [PDF](https://arxiv.org/pdf/2611.14421v1)



---

## 📎 arXiv Computer Vision and Pattern Recognition · 2026-11-12

### 📄 论文列表

- **在连接组约束的果蝇视觉系统模型中测量鲁棒性与效率：关联对抗性扰动与感知错觉**
  *Measuring Robustness and Efficiency in a Connectome-Constrained Fly Visual System Model: Linking an Adversarial and a Perceptual Illusion*

  📄 `arXiv:2611.14498` · cs.CV, q-bio.NC
  👥 **作者**：Alexandre Garcia-Duran, Alejandro Rodriguez-Garcia, Manuel Molano-Mazón, Alexandre Hyafil, Srikanth Ramaswamy, Janne K. Lappalainen
  📝 **摘要**：本研究通过基准测试受突触连接组约束的果蝇视觉系统连续时间循环神经网络（FlyNet），探讨了生物视觉系统在代谢和布线约束下的鲁棒性与效率。FlyNet 在碰撞检测任务中表现出极高的计算效率，其 FLOPs 比 RAFT 低多达五个数量级，且对常见视频损坏的鲁棒性优于 RAFT，但对对抗性扰动较为脆弱。相比之下，无详细连接组约束的 CTRNN 在几乎所有扰动下都比 FlyNet 更鲁棒，表明连接组约束主要提升了效率而非鲁棒性。研究进一步发现，FlyNet 的位置和速度表示在对抗性纹理下退化，但在恢复正确分类的反事实纹理下恢复，排除了陌生纹理作为失败原因。反向 phi 错觉同样破坏了这些表示，并反转了与对抗性纹理相同的低级运动统计量。仅优化该输入统计量即可诱导分类失败，将两种扰动归因于同一电路脆弱性，为生物感知脆弱性提供了可测试的假设。
  🔗 [PDF](https://arxiv.org/pdf/2611.14498v1)

- **RS-JEPA：用于跨传感器图像检索的遥感联合嵌入预测架构与扫描路径视图**
  *RS-JEPA: Remote Sensing Joint-Embedding Predictive Architecture with Scan-Path Views for Cross-Sensor Image Retrieval*

  📄 `arXiv:2611.14496` · cs.CV
  👥 **作者**：Tanishq Rachamalla, Srishti Kaushik, Muhammad Attique Khan, Gustau Camps-Valls, Swalpa Kumar Roy
  🏛️ **单位**：Prince Mohammad Bin Fahd University, Al Khobar, Saudi Arabia, Universitat de València, Valencia, Spain, Tezpur University, Assam, India
  📝 **摘要**：针对跨传感器遥感图像检索中现有自监督方法参数量大或仅对齐共注册图像的问题，本文提出了 RS-JEPA，一种基于共享 Vision Mamba 编码器的紧凑联合嵌入预测架构。由于状态空间编码器将图像读取为有序补丁序列，作者提出了“扫描路径视图”，将同一图像的两种读取顺序视为像素相同但顺序不同的两个视图，并预测一种顺序中的隐藏补丁。为保持预测挑战性，引入了对抗性视图耦合（AVC）以学习可见补丁的最难分割，以及邻域共识损失以对齐两种传感器的场景相似度。在 SAR-光学（BEN-14K, CBRSIR-VS）和 PAN-MS（DSRSID）基准测试中，RS-JEPA 以仅 3.88M 参数的检索网络（训练时 14.57M，比先前 JEPA 检索器少 8-16 倍）实现了最高的 F1@5 分数（分别为 72.92, 80.35 和 94.43），证明了读取顺序作为自监督视图来源的有效性。
  🔗 [PDF](https://arxiv.org/pdf/2611.14496v1)

- **BoviShift：跨越动物与时间的六年多属性视觉牛表型审计**
  *BoviShift: A Six-Year Multi-Attribute Audit of Visual Cattle Phenotyping Across Animals and Time*

  📄 `arXiv:2611.14476` · cs.CV
  👥 **作者**：Mobasshir Bhuiya Shagor, Nilambar Halder Tonmoy, Md Saef Ullah Miah
  🏛️ **单位**：Graaho Technologies LLC, Dhaka, Bangladesh, Indiana University Bloomington, Bloomington, IN, USA, American International University Bangladesh, Dhaka, Bangladesh
  📝 **摘要**：计算机视觉为估算牲畜性状提供了可扩展的非接触手段，但相关图像和视频帧使得可靠评估变得困难。本文介绍了 BoviShift，一个从 2021 到 2026 年连续六个年度队列重建的语料库，包含 2,657 头牛、10,610 张静态图像和 2,566 段环绕视频，涵盖九个记录品种。通过四种配置评估了三种分割策略：在相同开发队列上的图像随机分割和池化牛不相交分割，以及独立的未来 2025 和锁定未来 2026 评估。使用固定的 ResNet-50 多任务基线，评估了体重、年龄、身高、品种和毛色。研究发现，图像随机与牛不相交分割的差异是任务依赖的，而非普遍的泄漏惩罚；未来队列的行为也是属性和队列特定的，例如品种性能下降，而毛色在 2025 年迁移良好但在 2026 年退化。多任务训练改善了所有五个点估计，零样本视频帧聚合揭示了静态到视频的领域差距。BoviShift 是已知跨度最长的结合连续年度队列与物理和视觉属性的牛视觉资源。
  🔗 [PDF](https://arxiv.org/pdf/2611.14476v1)

- **TanCRAFT：用于组装任务的上下文推理预期反馈**
  *TanCRAFT: Context-Reasoned Anticipatory Feedback for Assembly Tasks*

  📄 `arXiv:2611.14470` · cs.RO, cs.CV
  👥 **作者**：Sassan Mokhtar, Lars Doorenbos, Marius Bock, Sina Mokhtar, Katharina Beckh, Dominik Bach, Juergen Gall
  🏛️ **单位**：University of Bonn, Germany, Lamarr Institute, Germany, University of New Mexico, USA, Fraunhofer IAIS, Germany
  📝 **摘要**：在物理组装任务中防止人为错误需要能在错误发生前进行干预的辅助系统，这在用户自由选择构建顺序且正确性取决于不断演变的组装状态时尤为具有挑战性。本文提出了 TanCRAFT，一个四阶段实时预测辅助系统，它跟踪场景状态，推理当前部分组装，预测被操纵部件的近未来运动，并在预测放置与目标不兼容时进行干预。该框架在受控的七巧板组装任务中通过离线基准测试和组内用户研究得到验证。结果显示，预测性反馈显著减少了相对于无引导和反应式会话的错误，同时产生了最低的平均感知工作负荷和最短的平均完成时间。这些结果证明了预测性反馈在错误预防中的价值，并为自动化和人机工作单元中的成本感知辅助迈出了一步。
  🔗 [PDF](https://arxiv.org/pdf/2611.14470v1)

- **C$^2$-Routing：用于高效视觉语言推理的互补裁剪与压缩**
  *C$^2$-Routing: Complementary Cropping and Compression for Efficient Vision-Language Inference*

  📄 `arXiv:2611.14469` · cs.CV, cs.LG
  👥 **作者**：Guorui Lu, Qinyu Chen
  🏛️ **单位**：Leiden University
  📝 **摘要**：视觉问答（VQA）给视觉语言模型（VLMs）带来了巨大的计算开销，促使人们寻求模型无关的输入减少方法。简单强制视觉令牌上限可减少计算，但可能丢弃回答问题所需的信息，且单一减少策略难以适应不同场景。本文的关键观察是裁剪和压缩是互补的：裁剪突出小目标和局部细节，而全图压缩更好地保留大目标或分布证据的上下文。基于此，提出了 C$^2$-Routing，它根据输入图像和问题自适应地选择裁剪或压缩。由于两种策略仍可能丢弃关键信息，进一步设计了一个安全门，利用原始和减少输入下预测的联合正确性分布来指导回退并保护准确性。所有训练和评估实验均在 RTX 3090 GPU 上运行。在三个 VLMs 和 18 个数据集上的广泛评估表明，在视觉预算已封顶的情况下，C$^2$-Routing 平均进一步将端到端 FLOPs 减少 36.53%，视觉令牌减少 42.36%，而平均相对任务分数仅下降 0.77%。
  🔗 [PDF](https://arxiv.org/pdf/2611.14469v1)



---
