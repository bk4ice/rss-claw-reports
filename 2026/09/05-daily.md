# 岛屿日报 · 2026-09-05

## 今日统计

**文章处理**：总抓取 393 篇 → 审核拦截 0 篇 → 进入报告 200 篇 → 实际引用 0 篇（引用率 0.0%）

**信息源**：共 24 个源参与，贡献最多：IT之家（71篇）、Dev.to（27篇）、Hacker News AI（20篇）、FreeBuf（16篇）、Hacker News 首页（16篇）

**分类分布**：clustered（2）

**时间跨度**：09-02 23:45 — 09-05 19:43（北京时间）

**事件聚类**：检测到 180 个独立事件

---

---

*本报告由 RSS-Claw 岛屿日报 AI 自动生成*


---

## 📎 产品机会雷达 · 2026-09-05

### 💡 产品方案

- **AgentGuard: AI 编码代理供应链安全审计 CLI** `★★★` `[蓝海]`
  > 扫描项目配置，检测 AI 代理自动执行不可信代码的风险
  🎯 **目标用户**：使用 Claude Code/Codex 的中小团队安全负责人
  😣 **痛点**：即刻工程师圈讨论指出 AI 代理会自动安装 llms.txt 指向的未注册包；Hacker News 披露 GitSpawn 漏洞，恶意仓库可注入任意命令；V2EX 用户抱怨 Codex 在家连不上中转站，担心数据泄露。
  🔄 **现有替代**：手动审查 .git/config 和 llms.txt，但无法自动化检测代理行为；现有安全工具不针对 AI 代理特有的信任模型破坏。
  🔧 **MVP 功能**：
    - 扫描 .git/config 中的 fsmonitor 注入
    - 解析 llms.txt 并验证包注册状态
    - 检测代理自动执行的 shell 命令白名单
    - 生成安全审计报告
  💰 **变现**：$29/月订阅，按仓库数量定价；企业版 $99/月
  ⏰ **为什么现在做**：GPT-6 Astra 发布后 AI 编码代理普及，GitSpawn 和 llms.txt 漏洞被广泛报道，企业开始关注 AI 代理供应链安全，但缺乏专用工具。
  ✅ **1周验证**：在 V2EX 和即刻发帖询问开发者是否担心 AI 代理执行不可信代码，做 CLI demo 扫描 3 个开源项目，看 star 增长和反馈。
  📡 **信号来源**：github-trending:mattpocock/skills · hacker-news:GitSpawn · jike-engineer:AI 代理安全讨论
  *分类：安全*

- **SkillHub: AI Agent 技能市场与版本管理** `★★★` `[小竞争]`
  > 为 Claude Code/Codex 提供技能发现、安装和更新管理
  🎯 **目标用户**：使用 AI 编码代理的独立开发者和中小团队
  😣 **痛点**：GitHub Trending 显示 mattpocock/skills、anthropics/skills 等项目 star 飙升；即刻讨论指出技能分散在多个仓库，缺乏统一发现和管理机制；V2EX 用户抱怨技能更新后行为不一致。
  🔄 **现有替代**：手动 git clone 技能仓库，但无法追踪版本和依赖；现有插件市场不支持 AI 代理技能格式。
  🔧 **MVP 功能**：
    - 技能元数据索引和搜索
    - 一键安装和更新技能
    - 版本控制和回滚
    - 技能兼容性检查
  💰 **变现**：免费基础版 + $9/月 Pro 版（优先更新、私有技能）
  ⏰ **为什么现在做**：AI 代理技能生态爆发，GitHub 上多个技能仓库 star 数飙升，但缺乏统一管理平台，类似早期 npm 生态前的机会。
  ✅ **1周验证**：在即刻和 V2EX 发帖调研开发者对技能管理的需求，做 Web demo 展示 10 个热门技能的索引和安装流程。
  📡 **信号来源**：github-trending:mattpocock/skills · github-trending:anthropics/skills · jike-ai:技能管理讨论
  *分类：开发者工具*

- **AgentTrace: AI 代理行为审计与合规日志** `★★` `[蓝海]`
  > 记录 AI 代理的每一步操作，生成可审计的行为日志
  🎯 **目标用户**：使用 AI 代理处理敏感数据的企业合规团队
  😣 **痛点**：开源中国报道 ChatGPT、Claude、Grok 同时宕机，企业无法追踪代理行为；Hacker News 披露 OpenAI 代理劫持 Wiki 事件，暴露代理行为不可审计；即刻讨论指出企业担心代理泄露数据。
  🔄 **现有替代**：手动记录代理操作，但无法自动化；现有日志工具不支持 AI 代理特有的多步骤推理链。
  🔧 **MVP 功能**：
    - 代理操作实时记录
    - 敏感数据访问标记
    - 行为链可视化
    - 合规报告导出
  💰 **变现**：$49/月订阅，按代理数量定价；企业版 $199/月
  ⏰ **为什么现在做**：AI 代理在企业中普及，但安全事件频发，合规需求激增，现有工具无法提供代理行为级别的审计能力。
  ✅ **1周验证**：在即刻和 V2EX 发帖询问企业是否关注 AI 代理合规，做 demo 展示代理操作日志和敏感数据标记功能。
  📡 **信号来源**：oschina:AI 代理宕机事件 · hacker-news:OpenAI 代理劫持 · jike-ai:企业合规讨论
  *分类：安全*


### 📡 值得关注的信号

- **AI 代理技能生态爆发** `github-trending`
  GitHub Trending 上 mattpocock/skills、anthropics/skills、humanlayer/skills 等项目 star 数飙升，表明 AI 代理技能正在成为新的开发范式，可能演变成技能市场、技能安全审计、技能版本管理等衍生工具。

- **AI 代理供应链安全漏洞频发** `hacker-news`
  GitSpawn 漏洞、llms.txt 未注册包问题、OpenAI 代理劫持 Wiki 事件接连曝光，表明 AI 代理的信任模型存在系统性风险，可能催生专门的安全审计工具和合规平台。

- **本地 AI 推理基础设施需求增长** `github-trending`
  GitHub Trending 上 magnitudedev/magnitude、OpenWhispr/openwhispr 等项目关注本地推理和隐私优先，结合 NVIDIA PAIR 发布，表明本地 AI 基础设施正在成熟，可能演变成本地模型管理、推理优化工具。

- **AI 代理行为不可审计问题** `oschina`
  ChatGPT、Claude、Grok 同时宕机事件、OpenAI 代理失控事件，暴露企业无法追踪 AI 代理行为的问题，可能催生代理行为审计、合规日志、代理监控等工具。


### 🔨 本周建议动手

- **构建 AgentGuard CLI 原型** `[HIGH]`
  第一步：用 Python 写一个 CLI 工具，扫描当前目录的 .git/config 文件，检测 fsmonitor 注入；解析 llms.txt 文件，验证包是否在 npm/PyPI 注册。在 V2EX 发帖展示 demo，收集反馈。

- **调研 AI 代理技能管理需求** `[MEDIUM]`
  第一步：在即刻和 V2EX 发帖，询问开发者如何管理 Claude Code/Codex 技能，痛点是什么。整理 10 个热门技能仓库，分析其元数据格式，设计 SkillHub 的 MVP 功能。



---

## 📎 arXiv Artificial Intelligence · 2026-09-05

### 📄 论文列表

- **通过训练编译：将自然语言规范转化为本地神经函数**
  *Compile by Training: Turning Natural-Language Specifications into Local Neural Functions*

  📄 `arXiv:2609.04199` · cs.CL, cs.AI, cs.LG
  👥 **作者**：Yuntian Deng, Pengyu Nie, Stuart Shieber
  🏛️ **单位**：University of Waterloo, Harvard University
  📝 **摘要**：针对许多文本功能易于描述但难以用规则实现，且调用远程大模型存在高延迟和成本的问题，本文提出“通过训练编译”（compile by training）方法。该方法在编译阶段利用教师模型生成特定任务的示例，训练紧凑解释器的小型适配器，从而将自然语言规范转化为可复用的本地神经函数。生成的函数无需依赖教师模型即可运行，支持存储、版本控制和组合。在FuzzyBench-Hard基准测试中，该方法达到了83.6%的语义准确率，优于快速编译器，但编译时间约为1分钟。作者部署了公开交互服务，并在多站点网站助手、语言控制3D头像及英-克劳迪语双向翻译器中展示了应用效果。
  🔗 [PDF](https://arxiv.org/pdf/2609.04199v1)

- **工程整洁，测量不稳：共享端点上黑盒LLM观察者预注册可靠性失败研究**
  *Clean Engineering, Unstable Measurement: A Preregistered Reliability Failure of Black-Box LLM Observers on Shared Endpoints*

  📄 `arXiv:2609.04198` · cs.AI, cs.LG
  👥 **作者**：Haoyaun Zhu, Jie Zhang
  🏛️ **单位**：University of Sheffield, Ranplan Wireless Network Design Ltd., Cambridge AI+ Ltd.
  📝 **摘要**：语言模型评判器作为测量工具，其可靠性依赖于“同一请求在同一模型上结果一致”的假设。本文通过两项预注册审计活动验证该假设，在52,988次请求尝试中发现，同窗口重复排名与次日字节相同重放的一致性远低于预设阈值（Spearman 0.400 vs 0.90；0.78 vs 0.99）。分析揭示了标签映射偏差、候选差距低于噪声底限以及相同输入返回不同排名等机制。后续实验表明，等待、切换提供商或自托管均无法根本解决共享基础设施上的测量不稳定问题。研究提出三级快照身份阶梯、八条设计规则和报告清单，强调在预注册评估中必须先验证测量工具的稳定性。
  🔗 [PDF](https://arxiv.org/pdf/2609.04198v1)

- **ESPO：通过诊断、多样化和稳定化实现错误结构化提示优化**
  *ESPO: Error-Structured Prompt Optimization via Diagnose, Diversify, and Stabilize*

  📄 `arXiv:2609.04197` · cs.CL, cs.AI
  👥 **作者**：Lihao Liu, Peng Tang, Kunwar Yashraj Singh, Shabnam Ghadar
  🏛️ **单位**：AWS Agentic AI
  📝 **摘要**：针对进化式提示优化器（如GEPA）存在的提示膨胀问题，本文提出ESPO（错误结构化提示优化）框架。ESPO将优化分解为三个阶段：诊断阶段在一轮内将训练错误聚类为结构模式；提案阶段通过四种互补策略生成候选提示；选择阶段应用自举稳定性选择。在七个公开NLP基准测试中，ESPO平均准确率比SOTA方法高3.76个百分点，且生成的提示比GEPA短47%，推理速度更快。跨模型实验显示，ESPO在Gemma 3、Mistral、Qwen3和Claude Haiku等四个学生模型上均取得最佳平均准确率。理论分析提供了泛化界限，消融实验证实缺乏稳定性选择的多样化会损害性能。
  🔗 [PDF](https://arxiv.org/pdf/2609.04197v1)

- **一个编辑器，多种编辑：用于多样化视频编辑的统一免训练框架**
  *One Editor, Many Edits: A Unified Training-Free Framework for Diverse Video Editing*

  📄 `arXiv:2609.04190` · cs.CV, cs.AI
  👥 **作者**：Adheesh Sunil Juvekar, Onkar Kishor Susladkar, Kiet A. Nguyen, Muntasir Wahed, Nabeel Bashir, Xiaona Zhou, Tianjiao Yu, Vedant Shah, Ismini Lourentzou
  🏛️ **单位**：University of Illinois Urbana-Champaign
  📝 **摘要**：视频编辑涵盖多种范式，但在单一框架内实现高质量指令引导和主体引导编辑仍具挑战性。本文提出EditVid，一个免训练框架，结合稀疏因果记忆以保持局部连贯性，基于对应关系的后注意力令牌注入以保留长程身份，以及软潜在混合以实现编辑局部性。该框架支持风格迁移、属性修改、对象插入、部件级编辑和主体替换等多种任务。在FiVE基准测试中，EditVid达到78.16的FiVE-Acc，显著优于最强免训练基线（58.95），并在IVEBench上取得竞争性结果。用户研究显示，与7种竞争方法相比，EditVid获得了51.8%的整体偏好率，证明了其在保持时间一致性的同时实现多样化编辑的有效性。
  🔗 [PDF](https://arxiv.org/pdf/2609.04190v1)

- **先观察后合成：VLM引导的弱监督密集视频字幕转换事件发现**
  *Seeing Before Synthesizing: VLM-Guided Transition Event Discovery for Weakly-Supervised Dense Video Captioning*

  📄 `arXiv:2609.04183` · cs.CV, cs.AI
  👥 **作者**：Ye-Chan Kim, Seunghee Choi, SeungJu Cha, Si-Woo Kim, Hwiseon Kim, Hyungee Kim, Dong-Jin Kim
  🏛️ **单位**：Hanyang University
  📝 **摘要**：弱监督密集视频字幕旨在仅根据视频级有序事件字幕定位和描述未修剪视频中的多个事件。现有方法通过LLM合成辅助转换字幕，但缺乏视觉基础且位置固定。本文提出“先观察后合成”（SBS）框架，利用视觉语言模型（VLM）自适应地提供具有视觉基础的语义指导。SBS首先为事件间隙生成帧级叙述，通过语义变化检测转换事件；随后通过混合时间中点与语义变化点，并选择最大化视觉-语言对齐的宽度来细化时间掩码。在ActivityNet Captions和YouCook2数据集上的实验表明，该方法在字幕生成和事件定位任务中均达到了最先进性能，有效解决了传统方法中转换字幕幻觉和刚性分配的问题。
  🔗 [PDF](https://arxiv.org/pdf/2609.04183v1)



---

## 📎 arXiv Machine Learning · 2026-09-05

### 📄 论文列表

- **可读性不等于可解释性：思维链推理中判断重要性与实际重要性的比较**
  *Legibility is Not Interpretability: Comparing Judged and Actual Importance in Chain-Of-Thought Reasoning*

  📄 `arXiv:2609.04194` · cs.CL, cs.LG
  👥 **作者**：Kevin Du, Alexander Hoyle, Laura Ruis, Acyr Locatelli
  🏛️ **单位**：ETH Zürich, MIT, Cohere
  📝 **摘要**：本文探讨了思维链（CoT）模型推理轨迹的可读性与可解释性之间的关系。作者将推理步骤的重要性操作化为“优势”（advantage），即包含该步骤对最终奖励（如正确答案概率）的影响，并通过蒙特卡洛 rollout 进行估计。基于此基准，研究评估了大型语言模型（LLM）作为裁判识别高优势步骤的能力。结果显示，尽管具备足够能力的 LLM 能优于流行度基线，但远未达到噪声上限。此外，微调模型作为步骤级批评者虽能显著改善对错误响应的判断，但在正确响应上仍与上限存在较大差距。这表明推理轨迹文本仅部分编码了步骤重要性信息，警示不应将推理轨迹的可读性直接等同于可解释性，这对过程奖励建模具有深远影响。
  🔗 [PDF](https://arxiv.org/pdf/2609.04194v1)

- **并发随机博弈的鲁棒 PAC 学习**
  *Robust PAC Learning of Concurrent Stochastic Games*

  📄 `arXiv:2609.04189` · cs.LG, cs.GT, cs.LO, cs.MA
  👥 **作者**：Angel Y. He, David Parker
  🏛️ **单位**：University of Oxford
  📝 **摘要**：本文提出了首个针对具有转移不确定性的通用和并发随机博弈（CSG）的 PAC 学习框架，并解决了纳什均衡（NE）存在性的挑战。算法通过维护转移核的数据驱动 L1 置信集，求解鲁棒 CSG 以计算社会福利最优的 ε-NE，并利用基于鲁棒 MDP 的探索机制驱动联合状态-动作覆盖。关键创新在于引入纳什边际特征，使框架能够原则性地推理均衡存在性：要么返回社会福利值接近最优的 ε-近似 NE，要么提供不存在精确 NE 的有效证书。在最小可达性条件下，算法在多项式数量的轨迹样本后终止，样本复杂度为 \widetilde{O}(R_{max}^2 H^4 |S|^2 |A| / (p_{reach} \varepsilon^2))。基准 CSG 上的实证结果表明，该方法具有近最优性能，能正确处理均衡（非）存在性，且样本复杂度与理论一致。
  🔗 [PDF](https://arxiv.org/pdf/2609.04189v1)

- **Para-Pipe：利用 SoC 上机器学习计算图的层级算子并行性**
  *Para-Pipe: Exploiting Hierarchical Operator Parallelism of ML Computational Graphs on SoCs*

  📄 `arXiv:2609.04168` · cs.DC, cs.LG, cs.PF
  👥 **作者**：Yujie Zhang, Huiying Lan, Ehsan Aghapour, Zhiyuan Ning, Peng Zan, Weidong Shao, Anuj Pathania, Tulika Mitra
  🏛️ **单位**：National University of Singapore
  📝 **摘要**：针对边缘深度学习应用在异构片上系统（SoC）上优化的挑战，本文提出了 Para-Pipe，一种整合流水线架构内阶段内与阶段间算子并行性的层级映射框架。传统流水线技术虽能提升吞吐量，但难以满足现代神经网络对低延迟的需求，且优化吞吐量往往以牺牲延迟为代价。Para-Pipe 通过选择性微调流水线各阶段的并行级别，在吞吐量与延迟之间进行权衡，显著降低了处理器间通信开销并提高了能效。在配备 ARM big.LITTLE CPU 和 GPU 的 Amlogic SoC 以及 Black Sesame Technology SoC 上的评估显示，Para-Pipe 能生成多个帕累托最优配置。特别是在 Amlogic SoC 上，吞吐量优化配置相比纯流水线策略平均能效提升 11.0%，相比非流水线并行执行提升 23.3%。
  🔗 [PDF](https://arxiv.org/pdf/2609.04168v1)

- **张量网络的参数化图论：纠缠重路由、结构简化与无先验层析成像**
  *Parameterised graph theory for tensor networks: entanglement rerouting, structural simplification, and agnostic tomography*

  📄 `arXiv:2609.04165` · quant-ph, cs.DS, cs.LG
  👥 **作者**：Matthias C. Caro, Natalie McHugh, Sergii Strelchuk
  🏛️ **单位**：University of Warwick, University of Oxford
  📝 **摘要**：本文利用参数化图论分析张量网络（TN）模拟的复杂性，探讨图结构参数如何决定张量网络态（TNS）是否允许可处理的矩阵乘积态（MPS）或树张量网络（TTN）表示，以及状态学习的复杂性。首先，证明切宽（cutwidth）和树切宽（tree-cutwidth）限制了将 TNS 表示为 MPS 或 TTN 所需的键维数开销，证明基于“纠缠重路由”这一张量网络类比。其次，推导了可实现 TNS 层析成像的样本和计算复杂性上界，其指数依赖于切宽、树切宽及新定义的“学习复杂性”参数。最后，将框架扩展至无先验设置，对于任意输入状态，无先验学习器输出一个纯态，其保真度在给定键维数的 TN 状态最优解的加性误差 ε 范围内，并提供了显式的图依赖性复杂性界限。
  🔗 [PDF](https://arxiv.org/pdf/2609.04165v1)

- **基于微型阿克曼车辆的低成本端到端自动驾驶开放平台**
  *A Low-Cost, Open Platform for End-to-End Autonomous Driving on a Miniature Ackermann Vehicle*

  📄 `arXiv:2609.04147` · cs.LG, cs.AI, cs.RO
  👥 **作者**：Gustavo Claudio Karl Couto, Eric Aislan Antonelo, Gabriel George Zipperer
  🏛️ **单位**：Federal University of Santa Catarina (UFSC)
  📝 **摘要**：本文介绍了一个用于微型阿克曼车辆端到端自动驾驶研究的低成本开放实验平台。该平台结合物理车辆、印刷城市赛道、数据采集工具、轨迹注册及 Webots 数字孪生，实现了连接仿真方法与真实世界执行的受控实验。作为基线，实现了命令条件行为克隆，神经策略接收车载相机图像和高层导航命令，输出转向和速度。在真实闭环实验中，策略平均横向误差为 6.1 cm，接近人类演示的 4.7 cm。数字孪生显示相机视场角对性能影响显著，从 58 度扩大至 120 度可将平均横向误差从 35.6 cm 降至 3.3 cm。利用数字孪生生成合成数据并结合 sim-to-real 图像翻译器，高容量策略在合成数据与真实演示混合训练下是唯一能完成所有四条赛道闭环的配置。该平台为 sim-to-real 研究提供了实用测试床。
  🔗 [PDF](https://arxiv.org/pdf/2609.04147v1)



---

## 📎 arXiv Computation and Language · 2026-09-05

### 📄 论文列表

- **预训练中的知识获取？大语言模型通过辅助视图学习得更好**
  *Knowledge Acquisition During Pre-training? Large Language Models Learn Better With Auxiliary Views*

  📄 `arXiv:2609.04180` · cs.CL, cs.AI
  👥 **作者**：Joseph Lee, Yidi Huang, Dokyoon Kim, Shu Yang, Li Shen
  🏛️ **单位**：University of Pennsylvania
  📝 **摘要**：本文探讨了大语言模型（LLM）在预训练阶段获取知识的机制，提出“辅助视图”（即知识的重构形式）对学习具有因果促进作用。通过受控实验，研究确认重复是知识获取的必要条件，且改写仅在较小批量大小下有效。在固定Token预算下，将原本用于文档重复的Token分配给辅助视图，能显著提升学习效果，甚至改善事实回忆能力。此外，辅助视图的有效性不依赖于生成它的教师模型强度。研究还识别出上下文和基础知识形式在存在先验知识缺口时的辅助作用，并通过层间偏差和压缩机制解释了这些效应。结果表明，预训练语料中自然产生的辅助知识表示是预训练成功的关键因素，也为数据多样性的重要性提供了合理解释。
  🔗 [PDF](https://arxiv.org/pdf/2609.04180v1)

- **最后翻译基准测试**
  *Last Translation Benchmark*

  📄 `arXiv:2609.04173` · cs.CL
  👥 **作者**：Vilém Zouhar, Niyati Bafna, Mukund Choudhary, Maike Züfle, Sara Rajaee, Pinzhen Chen, Jannis Vamvas, Sara Papi, Ona de Gibert, Bhavitvya Malik, Eliya Habba, Orfeas Menis Mastromichalakis, Patrícia Schmidtová, Michelle Wastl, Sheriff Issaka, Leshem Choshen, Stella Biderman, Antonis Anastasopoulos, Jan Niehues, Rico Sennrich, Mrinmaya Sachan, Ondřej Bojar, Kenton Murray, Jörg Tiedemann, Alham Fikri Aji, Philipp Koehn, Christof Monz, Alexandra Birch, Sowmya Vajjala, Chalamalasetti Kranti, Cristina España-Bonet, Nobin Sarwar, David Kaczér, Shunta Asano, Malik Marmonier, Daban Q. Jaff, Vaisakhi Mishra, Hend Al- Khalifa, Gabriele Sarti, Sourajit Saha, Nils Rehlinger, Juan Daniel Cuervo Villa, Jonathan Tonglet, Saugata Purkayastha, Dominik Macháček, Jagannathan Ramanujam, Heejin Do, Zuzana Nadova, Fred Philippy, Fabian Retkowski, Maria Lymperaiou, Silvia Casola, Hanna Yukhymenko, Shubhashis Roy Dipta, Sangwon Ryu, Andrés Jerez, Ron Keinan, Shuaib Shuaib Yusuf, Avantica Vempati, Maria Carmen Staiano, Sukannya Purkayastha, Adrian Cosma, Vitalii Babenko, Erivan Inan, Aviral Nigam, Wafa Aissa, Fatima Haouari, Venkata Prasanth Kumar Gummadi, Mehdi Jafarzadeh, Valentin Scourneau, Lukas Edman, Kaiser Sun, Shaomu Tan, Mohammad Sadegh Gholizadeh, Johannes-Rudolf David, Dipankar Srirag, Javier García Gilabert, Ruta Binkyte, Manar Ali, Ana-Maria Bucur, Sabry E. Farrag, Youssef Saber, Yihong Liu, Jean Maillard, Cojocaru Nicoleta, Xiaochuang Yuan, Sina Ahmadi, Philipp Mondorf, Kaustubh Dhole, Roman Wixinger, Shenbin Qian, Manuel Tuor, Sergey Troshin, Jonathan Yahav, Fida Mohammad Thoker, Amir Arsalan Rezapour, Lance Calvin Lim Gamboa, Manon Reusens, Kätriin Kukk, Koel Dutta Chowdhury, Giuseppe Gallipoli, Christian Hoang, Shaswati Saha, Seth Aycock, Jan Kocoń, Bo Chen, Linh Vu, Vatsal Venkatkrishna, Arafat Ahsan, Luan Thanh Nguyen, Hassan Soliman, Daryna Dementieva, Theresia Veronika Rampisela, Ngoc Quynh Tram Do, Marius Huber, Kazuki Egashira, Azmine Toushik Wasi, Vladislav Poritski, Mike Zhang, Deep Shah, Paul Gavrikov, Luis Frentzen Salim, David Africa, R. Damanhuri, Bello Umar Bello, Anumit Garg, Gengyu Rao, Pawan Sasanka Ammanamanchi, Kamile Dementaviciute, Andrianos Michail, L D M S Sai Teja, Dawei Zhu, Yi Fan, Wei Liu, Farhan Farsi, Elias Herranen, Sankalan Pal Chowdhury, Karen Sanchez, Farzad Shami, Ashok Urlana, Zimu Wang, Tomasz Limisiewicz, Priyaranjan Pattnayak, Marii Ojastu, Hongbin Na, Emilian Radoi, Chenyi Zhao, Carlos Hinojosa, Andrea Gregor de Varda, Zaid Alyafeai, Reem Alzahrani, Nehal Kathrotia, Alex Flückiger, Ulysses Sekai Tully Carr, Jimson Paulo Layacan, Guy Kaplan, Ritwik Tiwari, Rishit Dagli, Oksana Volchek, Isaac R Caswell, Bowen Yi, Blanka Kövér, Amir Hossein Yari, Aicha Chorana, Zhengxiang Wang, Selja Keränen, Samuel Simko, Joy Olusanya, Jenny Chim, Enzo Doyen, Vivek Harsha Lakkamaneni, Sophia Conrad, Pouya Sadeghi, Panayiotis Panayiotou, Luis Lara, Jannatul Nayem, Eran Yahav, Debanshu Das, Antonia Karamolegkou, Anmol Goel, Aishik Mandal, Tommaso Cerruti, Raoyuan Zhao, Mykola Haltiuk, Thura Aung, Naser Almousa, Amir Hossein Kargaran, Rachel Bawden, Qiaoyuan Zheng, Mateusz Lango, Beni Egressy, Fidel Rodríguez Velásquez, Natchapon Jongwiriyanurak, Minh Ngoc Do, Marco Gaido, Lena Libon, Dzmitry Kuzmin, Badal Nyalang, Antoine Taroni, Andrei Niculae, Abdulaziz Nura Kani, Rushikesh Zawar, Marek Šuppa, Beatrice Savoldi, Andreas Simons, Rayyan Merchant, Ilai Yaron Levy, Francesco Pinto, Ziyi Yang, Yolanda Xavier, Samuel Frontull, Muhammad Ravi Shulthan Habibi, Kenneth Enevoldsen, Harris Abdul Majid, Francesca Padovani, Tim Graf, Tatiana Bielakova, Sharifa Djurabaeva, Shaoxiong Ji, Raia Abu Ahmad, Pavel Stepachev, Jirui Qi, Ayush Sunil Munot, Alireza Pakniat, Ayla Rigouts Terryn, Yuxing Lu, Yurii Paniv, Xiyan Fu, Tosin Adewumi, Sunisth Kumar, Stéphane J. P. S. Thunus, Shree Harsha Bokkahalli Satish, Shayan Bali, Prakhar Gupta, Papa Abdou Karim Karou Diallo, Matija Akrap, Marko Culjak, Kristýna Onderková, Joseph Attieh, Esrael Teferi Tensay, Elisabeth Fittschen, Benoît Sagot, Jingwei Ni, Yu Fan
  🏛️ **单位**：ETH, JHU, MBZUAI, KIT, UvA, QUB
  📝 **摘要**：随着机器翻译模型能力的提升，现有基准测试逐渐趋于饱和，且自动评估指标存在不可靠、易被奖励黑客攻击及缺乏可操作性等问题，而人工评估也面临可复现性和客观性挑战。为此，本文提出了“最后翻译基准测试”（Last Translation Benchmark, LTB），这是一个由人类创作并经同行评审的示例集合（涵盖文本、图像、音频、视频），旨在测试并突破当前领先机器翻译模型的极限。该基准测试引入了一种新的评估方法：每个示例都附带手工制作的验证规则，具体描述了该示例上的失败案例，从而实现了可靠且可操作的评估。LTB是一个实时数据集，接受持续贡献。最新版本LTBv1包含2026年9月1日之前接受的贡献，未来将随着新数据的收集持续发布更新。
  🔗 [PDF](https://arxiv.org/pdf/2609.04173v1)

- **重新思考大语言模型的在线策略蒸馏 II：单个训练样本**
  *Rethinking On-Policy Distillation of Large Language Models II: One Training Example*

  📄 `arXiv:2609.04172` · cs.AI, cs.CL
  👥 **作者**：Zixuan Fu, Bingxiang He, Yuxin Zuo, Haohuan Huang, Jinqian Zhang, Ruhang Xiao, Cheng Qian, Qinyu Luo, Huan-ang Gao, Yudong Wang, Zhiyuan Liu, Ning Ding, Chaojun Xiao
  🏛️ **单位**：Tsinghua University, University of Chinese Academy of Sciences, Northeastern University, University of Illinois Urbana-Champaign, Johns Hopkins University
  📝 **摘要**：在线策略蒸馏（OPD）结合了学生生成的轨迹和教师提供的密集Token级监督，但现有研究主要关注算法行为，对训练数据的作用缺乏清晰认识。本文在数据最小极限下，通过仅使用单个查询进行训练来探究这一角色。实验发现，单样本OPD在数百步训练中持续改进，并在不同任务领域和模型家族中恢复了全数据OPD的大部分增益。通过测量“状态覆盖率”（即查询集轨迹达到的全数据OPD访问状态的比例），研究发现单个查询即可达到71.5%的覆盖率，且大部分在前100步内完成。增加语义不同的查询会同时提高覆盖率和验证准确率，直到16个查询达到98.9%并匹配全数据训练。然而，无论训练数据量多少，学生与教师的对齐速度都相似地减慢，表明OPD是“数据过供但算法饥饿”的。这一发现延伸至多教师OPD，并建议未来工作应关注OPD的步骤效率及重新审视其成功背后的数据与机制。
  🔗 [PDF](https://arxiv.org/pdf/2609.04172v1)

- **Terminal-Universe：将智能体轨迹转化为可扩展的终端环境**
  *Terminal-Universe: Turning Agent Trajectories into Scalable Terminal Environments*

  📄 `arXiv:2609.04148` · cs.AI, cs.CL
  👥 **作者**：Jie Wu, Zhenru Zhang, Beichen Zhang, Xuwu Wang, Yuhui Su, Mouxiang Chen, Peng Wang, Zhihai Wang, Que Shen, Hao Zhou, An Yang, Fei Huang, Yujiu Yang, Dayiheng Liu
  🏛️ **单位**：Qwen Team, Alibaba Group, Tsinghua University
  📝 **摘要**：随着基于终端的代码智能体普及，智能体轨迹已大规模积累，但真实可执行的环境依然稀缺。环境是智能体后训练的关键，因为它们可被重新查询为多个可验证任务并提供执行反馈，而轨迹仅是单一的冻结演示。本文提出Terminal-Universe框架，通过重放轨迹中记录的文件操作来恢复智能体修改前的文件，生成部分工作区，并由补全智能体提供缺失文件和依赖，从而将每个轨迹转化为可复用的环境。在此基础上，该框架不仅重构原始意图任务，还合成全新任务，并沿“广度”（挖掘环境间依赖关系，合成跨工作区查询）和“深度”（将单轮查询扩展为多轮会话，捕捉迭代反馈）两个维度扩展任务。应用于公开终端智能体轨迹后，Terminal-Universe生成了37.3k个任务充足的环境。在Qwen3.5-27B上进行监督微调后，在Terminal-Bench 2.1上的单轮性能提升11.9分，在EvoCode-Bench v2 MT@4上的多轮性能提升13.8分。
  🔗 [PDF](https://arxiv.org/pdf/2609.04148v1)

- **顺序优于联合：在线策略蒸馏与RLVR的相互作用**
  *Sequential Beats Joint: On the Interplay between On-Policy Distillation and RLVR*

  📄 `arXiv:2609.04108` · cs.CL, cs.AI, cs.LG
  👥 **作者**：Boyan Li, Bingsen Chen, Chenghao Yang, Ping Nie, Chen Zhao, Xi Ye
  🏛️ **单位**：University of Alberta, New York University, NYU Shanghai, University of Chicago, University of Waterloo, Alberta Machine Intelligence Institute (Amii)
  📝 **摘要**：基于可验证奖励的强化学习（RLVR）和在线策略蒸馏（OPD）是后训练推理大语言模型的两种主要方法。先前工作通常将OPD的密集Token级监督与稀疏RL奖励在单步中融合（如加权加法或教师调制重缩放）。本文证明，简单的两阶段方案“先OPD后RL”在逻辑和数学推理基准测试中始终优于纯OPD、纯RLVR以及所有联合基线。通过pass@k行为、学习动态和参数更新分析，本文提供了系统性解释：OPD扩展了学生对教师支持解的覆盖范围，而RL在该支持范围内进行锐化；联合优化两种信号会导致干扰。此外，研究发现OPD验证分数是切换至RL阶段的关键信号，且OPD比SFT更适合作为RL的冷启动。这些结果确立了“先OPD后RL”作为结合两种方法的简单而强大的策略，将两个纠缠的信号转化为互补的阶段。
  🔗 [PDF](https://arxiv.org/pdf/2609.04108v1)



---

## 📎 arXiv Computer Vision and Pattern Recognition · 2026-09-05

### 📄 论文列表

- **时间自蒸馏：无监督学习视频中的视觉状态跟踪**
  *Temporal Self-Distillation: Learning Visual State Tracking in Videos Without Supervision*

  📄 `arXiv:2609.04203` · cs.CV
  👥 **作者**：Shravan Venkatraman, Wenshuai Zhao, Mohammad Hassan Vali, Arno Solin
  🏛️ **单位**：Mohamed bin Zayed University of Artificial Intelligence, UAE, ELLIS Institute Finland & Department of Computer Science, Aalto University, Finland
  📝 **摘要**：本文提出了S$^3$T（时间自监督自蒸馏），这是首个完全自包含的连续视频状态跟踪框架。该方法基于时间采样密度作为特权信息的假设，利用同一视频片段的密集视图作为教师，指导稀疏视图的学生模型（共享权重）匹配其下一词元分布。由于模型生成自身目标，训练无需标签、独立教师或奖励信号，且不增加推理成本。在LLaVA-OneVision-2-8B上，S$^3$T作为单模型将VSTAT准确率提升1.74，结合模型汤（souping）提升2.38，结合视觉编码器适配提升2.70。此外，从无标签合成片段学习的能力可迁移至真实视频，在VSTAT-YouTube状态跟踪问题上提升7.95，在MVBench动作计数任务上提升4.50。
  🔗 [PDF](https://arxiv.org/pdf/2609.04203v1)

- **TokenMatch：基于曲率引导分词化的3D网格对应Transformer**
  *TokenMatch: 3D Mesh Correspondence Transformer with Curvature-Guided Tokenisation*

  📄 `arXiv:2609.04202` · cs.CV
  👥 **作者**：Adeela Islam, Zorah Lähner, Vittorio Murino, Vladislav Golyanik
  🏛️ **单位**：Italian Institute of Technology, University of Genoa, University of Bonn, Lamarr Institute, University of Verona, Max Planck Institute for Informatics, SIC
  📝 **摘要**：针对现有3D形状对应估计方法在部分观测和非等距变形下鲁棒性不足的问题，本文提出了TokenMatch，一种基于Transformer的统一模型。TokenMatch利用自注意力和交叉注意力机制，高效学习补丁级和点级关系以及形状对之间的密集对应。其核心创新在于利用形状曲率引导将网格自适应地分词化为补丁，从而有效学习形状特定的几何描述符。该前馈模型仅在BeCoS数据集（非等距部分到部分匹配）上训练，即可泛化到完整形状匹配，无需重新训练或微调。在CP2P、PSMAL、BeCoS、FAUST、SCAPE和SHREC'19等标准基准上，TokenMatch在平均测地线误差和交并比指标上通常优于现有方法，且推理速度达到亚秒级。
  🔗 [PDF](https://arxiv.org/pdf/2609.04202v1)

- **Scal3R：学习高效多相对位姿查询以实现可扩展的在线3D重建**
  *Scal3R: Learning Efficient Multi-Relative Pose Query for Scalable Online 3D Reconstruction*

  📄 `arXiv:2609.04201` · cs.CV
  👥 **作者**：Chin-Yang Lin, Yang-Che Sun, Cheng Sun, Fu-En Yang, Min-Hung Chen, Yen-Yu Lin, Wei-Chen Chiu, Yu-Lun Liu
  🏛️ **单位**：Department of Computer Science, National Yang Ming Chiao Tung University, NVIDIA
  📝 **摘要**：在线3D重建模型在长视频上表现不佳，因为相对于固定首帧锚点回归位姿会导致超出训练分布的外推，累积漂移引发几何崩溃。本文观察到尽管全局位姿头失效，但逐帧深度保持稳定。基于此，提出Scal3R，将在线重建重构为多参考相对位姿查询。该方法使用约占参数1%的轻量级可学习令牌，通过非对称注意力注入完全冻结的骨干网络，查询相对于多个过去关键帧的位姿。结合带闭环的在线位姿图优化系统，Scal3R有效抑制长程漂移。在单GPU上8小时内收敛，在KITTI上将平均ATE降低60%以上，并在Virtual KITTI、Sintel、TUM-Dynamic、ScanNet和7-Scenes上取得最先进性能。
  🔗 [PDF](https://arxiv.org/pdf/2609.04201v1)

- **Principia：视频模型的关系物理测试**
  *Principia: Relational Physics Tests for Video Models*

  📄 `arXiv:2609.04200` · cs.CV
  👥 **作者**：Varun Varma Thozhiyoor, Shivam Tripathi, Venkatesh Babu Radhakrishnan, Anand Bhattad
  🏛️ **单位**：Indian Institute of Science, Johns Hopkins University
  📝 **摘要**：评估视频模型的物理推理能力极具挑战，因为绝对运动测量依赖于帧率、物体尺度和相机校准，这些在生成视频中往往模糊或缺失。本文提出Principia基准，通过成对物体间的关系一致性来评估牛顿物理定律，这种关系独立于校准。Principia涵盖重力、恢复系数、摩擦、转动惯量、抛体运动、动量、摆和弹簧振荡八种现象，使用受控协议记录的真实场景。此外，引入一种校准无关的一致性分数，直接在图像空间量化物理违规。在六个最先进视频生成器的数千次生成中，尽管在VBench上得分约0.8，但在Principia上无一超过0.42。视觉语言模型在检测关系物理违规方面表现不佳，最佳模型准确率仅67%，多数接近随机水平。
  🔗 [PDF](https://arxiv.org/pdf/2609.04200v1)

- **Puffin-World：利用原生3D世界状态扩展统一多模态模型**
  *Puffin-World: Scaling a Unified Multimodal Model with Native 3D World States*

  📄 `arXiv:2609.04196` · cs.CV
  👥 **作者**：Kang Liao, Yihang Luo, Xiao-Ming Wu, Linyi Jin, Size Wu, Chunyu Lin, Yao Zhao, Fei Wang, Wei Li, Chen Change Loy
  🏛️ **单位**：S-Lab, Nanyang Technological University, University of Michigan, Beijing Jiaotong University, ACE Robotics
  📝 **摘要**：本文提出Puffin-World，一种统一的多模态架构，无需外部离线模块即可整合物理理解、空间模拟以及3D世界生成与重建。该框架联合建模三种原生世界状态：物理（重力场和纬度）、几何（深度）和外观（图像），并结合统一的Omni-Camera表示以支持多样任务和灵活运动。通过引入跨未来帧传播物理动态的策略，并将绝对相机属性锚定在真实世界中，Puffin-World实现了物理一致且视觉稳定的世界生成。此外，在单一生成过程中耦合外观和几何，联合合成未来视图并重建其底层几何。为扩展至复杂场景，构建了包含1500万视觉-语言-相机三元组和100万轨迹的Puffin-16M数据集，并开源了代码、模型和数据集。
  🔗 [PDF](https://arxiv.org/pdf/2609.04196v1)



---
