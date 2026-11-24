# 岛屿日报 · 2026-11-24｜AI黎曼猜想获证，黄仁勋复职，CrowdStrike并购

## 今日概览

本周科技界迎来**AI数学**与**芯片治理**的双重震动。Anthropic利用AI证明**黎曼猜想**引发学界反思，而**黄仁勋**在特朗普支持下复职，股价单日大涨近**30%**。安全领域，**CrowdStrike**宣布**439亿美元**收购Zscaler，同时OpenRouter泄露事件凸显供应链风险。*在AI能力爆发与地缘政治博弈交织下，行业正加速重构信任与治理边界。*

**值得关注的要点：**

- **Anthropic**确认AI证明黎曼猜想正确，引发数学界震动
- **黄仁勋**正式复职英伟达CEO，股价单日涨幅近30%
- **CrowdStrike**以439亿美元全股票收购Zscaler，整合安全平台
- **OpenRouter**泄露200万条提示词，回退机制成最大风险
- **亚马逊**75亿美元收购Decart，强化Trainium芯片竞争力
- **腾讯**开源HyMT3模型，支持102种语言且性能超越旗舰

## 今日统计

**文章处理**：总抓取 555 篇 → 审核拦截 0 篇 → 进入报告 200 篇 → 实际引用 52 篇（引用率 26.0%）

**信息源**：共 24 个源参与，贡献最多：IT之家（81篇）、Hacker News AI（21篇）、FreeBuf（17篇）、Dev.to（16篇）、TechCrunch（14篇）

**分类分布**：clustered（1）

**时间跨度**：11-18 02:42 — 11-24 19:20（北京时间）

**事件聚类**：检测到 143 个独立事件

---

## AI 安全与可信运行时

### 1. OpenRouter 泄露事件：回退机制成最大风险

OpenRouter 因三家推理提供商数据泄露，撤销了 125 个端点的零数据保留状态。Dragos 研究显示约 200 万条提示词可能包含泄露凭证。文章指出，开发者应固定提供商、禁用回退机制并避免在提示词中直接包含密钥，同时建议进行独立的金丝雀测试以审计数据流向，从而降低供应链安全风险。

**重点**：回退提供商是 LLM 应用数据泄露的主要隐患

**来源**：[Dev.to](https://dev.to/shivaysinghrajput/i-ran-the-numbers-on-the-openrouter-prompt-leak-your-fallback-provider-is-your-biggest-risk-2h07)

### 2. Agent 参数投毒：93% 成功率下的防御盲区

![Agent 参数投毒：93% 成功率下的防御盲区](https://image.3001.net/images/20261123/1795426988_6b040aaca2d2a7ba77780.png!small)

中科大团队实测发现，现有 AI Agent 防御机制因聚焦动作完整性而忽视参数来源，导致“参数投毒”攻击成功率高达 93%。文章介绍了基于任务感知授权框架 AuthorityFlow 的防御方案，通过冻结授权基线和追踪参数来源，将攻击成功率降至 9% 左右，并提出了蓝队落地的检测思路，为 Agent 安全提供了新视角。

**重点**：参数来源追踪可将 Agent 攻击成功率降至 9%

**来源**：[FreeBuf](https://www.freebuf.com/articles/ai-security/514134.html)

### 3. OpenAI 与 Cisco 发布 AI 辅助 Linux 安全工具

OpenAI 与 Cisco 联合发布开源 Linux 运行时工具 Shirudo。该工具允许 AI 代理通过编写动态 eBPF 控制来防御系统漏洞，无需停机即可在补丁部署前拦截利用。这一创新为防御者争取了测试和发布补丁的时间，显著提升了 Linux 系统在面临零日漏洞时的响应速度和安全性。

**重点**：AI 代理动态生成 eBPF 控制实现漏洞即时拦截

**来源**：[The Hacker News](https://thehackernews.com/2026/11/openai-and-cisco-unveil-ai-assisted.html)

### 4. Linux 基金会接纳 TRACE 规范验证 AI 运行时

![Linux 基金会接纳 TRACE 规范验证 AI 运行时](https://www.linuxfoundation.org/hs-fs/hubfs/Press%20Release%20Images%20-%20GL%20(19).png?width=600&height=314&name=Press%20Release%20Images%20-%20GL%20(19).png)

Linux 基金会宣布接纳 OPAQUE 贡献的 TRACE 开放规范。该规范由 AMD、Intel、Microsoft 等共同开发，旨在为 AI 智能体和机密工作负载提供可验证的硬件证明运行时证据。TRACE 基于 RATS、SLSA 等现有标准，构建跨云、跨平台的合规与安全证据层，确保 AI 系统在处理敏感数据时的操作完整性可被独立验证。

**重点**：TRACE 规范为 AI 工作负载提供跨平台硬件证明

**来源**：[Hacker News AI](https://www.linuxfoundation.org/press/linux-foundation-welcomes-trace-to-advance-verifiable-runtime-evidence-for-ai-workloads)

## AI 数学突破：黎曼猜想证明与学科反思

### 5. 独立数学家确认 AI 黎曼猜想证明正确

![独立数学家确认 AI 黎曼猜想证明正确](https://static.scientificamerican.com/dam/asset/64e45f50-d1c5-4a9f-ad48-60b52541abcc/riemann-proven.jpg?m=1795211310.647&w=600)

Anthropic 数学家 Levent Alpöge 声称利用 Claude AI 模型证明了黎曼猜想。独立数学家及 Lean/Mathlib 社区已确认该证明正确，代码编译无误且通过独立内核复核，排除了逻辑漏洞或符号重定义等潜在问题。

**重点**：AI 证明获独立复核，确立数学新范式

**来源**：[Hacker News AI](https://www.scientificamerican.com/article/the-ai-riemann-hypothesis-proof-is-almost-certainly-true-independent-mathematicians-attest/) · [Hacker News AI](https://www.nature.com/articles/d41586-026-03812-7)

### 6. AI 数学爆发引发学界震动与担忧

![AI 数学爆发引发学界震动与担忧](https://images.theconversation.com/files/768642/original/file-20261027-62-aev245.jpg?ixlib=rb-4.1.1&rect=0%2C0%2C4447%2C2964&q=45&auto=format&w=1050&h=700&fit=crop)

2026 年，OpenAI 和 Anthropic 等前沿 AI 模型解决了包括纳维-斯托克斯方程和黎曼猜想在内的多个长期未解难题。OpenAI 通过部署大规模 AI 智能体集群，发布了 700 多篇论文，声称解决了 372 个开放问题。这一“AI 数学爆发”引发了数学界的震动与担忧，菲尔兹奖得主陶哲轩等学者指出 AI 公司目标与数学社区存在严重错位，并发起宣言呼吁关注数学研究的本质。尽管 AI 能高效产出结果，但其高昂的计算成本（如纳维-斯托克斯方程解法耗资 1500 万美元）也引发了对商业可持续性的讨论。

**重点**：AI 高效解题但成本高昂，学界反思研究本质

**来源**：[The Conversation](https://theconversation.com/ai-has-solved-a-host-of-big-maths-problems-heres-why-this-threatens-the-whole-field-of-mathematics-293982)

### 7. Anthropic 发布 AI 编写的复杂度下界论文

Anthropic 发布论文《VP ≠ VNP over Every Field》，证明在任意域上，哈密顿回路多项式电路及特征不为 2 时的永久多项式电路复杂度下界。该结果由内部研究模型 Claude 发现，论文及 Lean 4 形式化证明均由 AI 编写，尚未经过人类数学家检查。

**重点**：AI 自主发现并形式化证明复杂度下界

**来源**：[Hacker News 首页](https://github.com/anthropics/formal-math/tree/main/vp-vnp)

## AI前沿模型与架构创新

### 8. 智谱发布GLM-5.4：首个Loop Transformer架构落地

智谱AI发布GLM-5.4，首次采用Looped Transformer架构，通过固定循环中间层提升有效深度并降低显存需求。该模型支持视觉输入、100万token上下文窗口，并将订阅用户每周配额提升50%。尽管未公开完整跑分及开源权重，但其架构创新在Hacker News引发广泛讨论，被视为通用编码能力的重要探索。

**重点**：Loop架构降低显存，支持1M上下文

**来源**：[极客洞察](https://newshacker.me/story?id=50609685) · [Dev.to](https://dev.to/paullovelace/glm-54-can-see-now-vision-1m-context-50-more-quota-2ofj) · [Hacker News 首页](https://z.ai/blog/glm-5.4)

### 9. 腾讯开源HyMT3：102种语言翻译性能超越旗舰

![腾讯开源HyMT3：102种语言翻译性能超越旗舰](https://img.ithome.com/newsuploadfiles/2026/11/30f46923-081d-4fae-8b81-dfc39b86f5f5.png)

腾讯发布并开源第三代翻译模型HyMT3，提供1.8B、7B及30B-A3B三种尺寸，支持102种语言。该模型在误译、漏译及指令遵循方面显著优化，性能超越Qwen3.8-Max等旗舰模型。HyMT3重点优化游戏本地化与图片翻译场景，并联合AMD实现NPU加速，支持在PC及手机端侧本地部署，数据本地处理。

**重点**：开源多尺寸，端侧NPU加速，性能领先

**来源**：[IT之家](https://www.ithome.com/1/031/681.htm)

### 10. 蚂蚁集团开源医疗AI：宣称超越OpenAI与Google

蚂蚁集团免费开源两款医疗AI模型：5600亿参数的LingSante-3.1-flash擅长复杂医疗推理，1240亿参数的LingSante-3.1-air-VL可读取X光片、皮肤照片及操作健康App预约。官方称其在多项测试中超越OpenAI、Google和Anthropic的最新模型，但强调其仅为研究工具，不能替代专业医疗诊断。

**重点**：双模型开源，多模态医疗推理能力突出

**来源**：[Dev.to](https://dev.to/fathomnews/ant-group-gives-away-free-medical-ai-it-says-beats-openai-and-google-1gd2)

### 11. TML发布Inkling 2 Mini：小参数循环架构编程领先

![TML发布Inkling 2 Mini：小参数循环架构编程领先](https://img.ithome.com/newsuploadfiles/2026/11/2bc8e745-634a-49c3-9837-2afa71d53eb4.png)

Thinking Machines Lab发布Inkling 2 Mini模型，采用循环Transformer架构，总参数26.4B，激活参数仅5.4B。该模型在智能体编程等推理任务上表现优异，在DeepSWE和SWE-bench Pro测试中领先于100B以内模型。支持通过Ollama在32GB内存Mac及NVIDIA DGX Spark上运行，展现了小模型在特定垂直领域的高效能。

**重点**：26B参数激活5.4B，编程基准测试领先

**来源**：[IT之家](https://www.ithome.com/1/030/907.htm)

### 12. 大模型周榜：Gemini 4 Neon空降第3，国产模型智能体稳定

Arena发布第47周大模型周榜，谷歌Gemini 4 Neon空降综合榜第3，Anthropic Claude Fable 5.2入榜第7。国产模型中，阿里Qwen4-Max在智能体榜首秀第18，腾讯Hy4进入前端开发与智能体榜单。整体来看，新模型主导本周变化，国产模型在综合榜处中游，但在智能体与前端开发维度表现稳定。

**重点**：Gemini 4 Neon登顶前三，国产智能体表现亮眼

**来源**：[IT之家](https://www.ithome.com/1/030/935.htm)

## AI安全、治理与隐私风险

### 13. 前沿AI公司进入“Handoff”阶段，失控风险上升

![前沿AI公司进入“Handoff”阶段，失控风险上升](https://cdn.prod.website-files.com/6a2bd279c59d9c01b2a20237/6b039751aaac8cdc4541aaa5_1189bd86.png)

Apollo Research报告指出，Anthropic和OpenAI等前沿公司正将研发执行与决策权移交给内部AI智能体。数据显示Claude已主导26%的研发工作，人类审查大幅减少。报告警告，若2027-2028年实现递归自我改进，对齐难度增加将导致失控风险急剧放大，建议政府尽快获取可见性并制定应对策略。

**重点**：人类监督减弱，递归自我改进临近，需政府介入

**来源**：[Hacker News AI](https://apolloresearch.ai/governance/handoff-at-frontier-ai-companies)

### 14. 开源AI黑客框架ARTEX引发全球安全警报

![开源AI黑客框架ARTEX引发全球安全警报](https://storage.ghost.io/c/0f/76/0f76b548-bc58-4f25-abc3-3f5ebca07da4/content/images/2023/08/404-joseph-01-1.jpg)

FBI警告称，开源AI黑客框架ARTEX被用于政府、医疗等多行业的间谍及金融攻击。该工具利用代理AI以“机器速度”自动化侦察至数据窃取，数小时内即可完成。尽管原作者已转为闭源，但代码已被广泛克隆。维护者强调其对小团队自测仍有价值，呼吁关注FBI发布的失陷指标。

**重点**：AI加速攻击流程，开源代码扩散加剧安全挑战

**来源**：[Hacker News AI](https://www.404media.co/the-code-is-already-copied-everywhere-the-ai-hacking-tool-causing-havoc-around-the-world-artex-github/)

### 15. 前沿模型仅需一段文本即可识别作者身份

新研究表明，Claude Fable 5.2等前沿模型通过零样本提示，能准确判断文本作者是AI还是人类，甚至能识别98%的AI生成文本所属实验室及特定人群的人类作者ID。研究指出，模型对作者写作风格的预训练数据暴露程度是关键，这对在线发布大量文本者的匿名性构成重大威胁，现有防御手段有限。

**重点**：AI指纹识别能力增强，在线匿名性面临挑战

**来源**：[Hacker News AI](https://arxiv.org/abs/2611.26216) · [Hacker News AI](https://arxiv.org/abs/2611.26216)

### 16. Google Cloud CISO：自主AI攻击迫使SOC架构演进

![Google Cloud CISO：自主AI攻击迫使SOC架构演进](https://image.3001.net/images/20261124/1795508979671058_81fc4585440841698af4661cfb071ee7.webp!small)

Google Cloud CISO Chris Betz指出，自主AI攻击使传统人工防御失效，攻击者可在数分钟内完成横向移动。企业需构建可审计、可回滚的Agent安全管控体系，转向“Moving Beyond Zero”架构。未来SOC分析师将聚焦高阶策略，董事会需重点审查Agent操作的追踪与审计能力，以应对2027年的安全风险。

**重点**：传统防御基线失效，需建立可审计的Agent管控体系

**来源**：[FreeBuf](https://www.freebuf.com/articles/ai-security/514280.html)

### 17. OpenAI提议基于“困惑度”为AI能力设定速度限制

OpenAI首席科学家Jakub Pachocki提议利用“困惑度”指标为AI模型能力设定行业通用的“速度限制”。当模型预测准确率突破特定阈值时，强制暂停训练并进行安全评估。该策略直接针对模型智能水平，旨在解决算法效率提升带来的监管滞后问题，引发了关于自我监管与行业壁垒的讨论。

**重点**：以智能水平而非算力为监管基准，应对算法效率提升

**来源**：[Dev.to](https://dev.to/gp-ia-blog/openai-wants-to-cap-ai-power-using-perplexity-1io9)

### 18. Meta AI首席警告超级智能风险，引发政界争议

![Meta AI首席警告超级智能风险，引发政界争议](https://data.ibtimes.sg/en/full/99314/democrats-are-preparing-tougher-ai-regulations-congressional-investigations-ceo-hearings-and-subpoenas-as-they-take-control-of-the-us-house-and-senate-in-2027.jpg?w=736)

Meta首席AI官Alexandr Wang警告，若缺乏约束的递归自我改进，人类可能失去对AI的控制权，超级智能即将到来。前奥巴马演讲撰稿人Jon Favreau批评其为“疯狂”，呼吁政治领导人干预。Wang随后澄清该路径并非不可避免，强调领导层重要性，并提及Meta在安全方面的投入及参与SI Accords协议。

**重点**：超级智能控制权之争，科技领袖与政界观点碰撞

**来源**：[Hacker News AI](https://www.ibtimes.sg/meta-ai-chief-warns-superintelligence-risks-obamas-former-speechwriter-calls-it-fing-madness-96538)

### 19. Vercel推出经审计的零数据保留功能提升透明度

![Vercel推出经审计的零数据保留功能提升透明度](https://vercel.com/vc-ap-vercel-marketing/_next/image?url=https%3A%2F%2Fassets.vercel.com%2Fimage%2Fupload%2Fcontentful%2Fimage%2Fe5382hct74si%2F7911SzATc1NYfyRnFQN5Ud%2F3f2014ceadf901735edeab4107376f2f%2Faudited-zdr-flow-desktop-light.png&w=1200&q=95)

Vercel在AI Gateway推出Audited ZDR功能，要求推理提供商通过独立安全公司的代码、基础设施及实时流量审计来证明零数据保留承诺，审计报告将公开。Baseten、Modal和Wafer为首批合作伙伴。此举旨在解决传统合同自证缺乏保障的问题，配合Canary监控机制，提升AI数据处理的透明度与安全性。

**重点**：独立审计替代合同自证，增强AI数据处理信任

**来源**：[Vercel Blog](https://vercel.com/blog/introducing-audited-zdr-on-ai-gateway)

### 20. OpenAI Codex Desktop审计发现多处隐私与数据残留问题

对OpenAI Codex Desktop的取证审计发现，高推理模式下存在516 token量化截断，且客户端在用户未授权训练时捕获1 MiB原始git diff数据。此外，默认读取Windows注册表获取应用记录，本地SQLite数据库未执行安全删除导致数据残留，GDPR导出档案缺失会话记录。作者提供了离线只读审计工具供用户验证。

**重点**：桌面端AI工具存在数据残留与未授权采集，需用户自查

**来源**：[Dev.to](https://dev.to/nehumorist/auditing-openai-codex-desktop-516-token-cutoffs-live-1-mib-git-diffs-and-unzeroed-sqlite-c48)

## Nvidia CEO 黄仁勋复职风波与地缘政治博弈

### 21. 黄仁勋正式复职，股价单日大涨近30%

![黄仁勋正式复职，股价单日大涨近30%](https://img.ithome.com/newsuploadfiles/2026/11/c29e331e-6f53-48e9-8038-d90d350ff11c.jpg)

英伟达董事会在经历多轮讨论后，于11月23日投票恢复黄仁勋的CEO职务。此前他因涉及与中国情报机构有关联女性的恋情及性不当行为指控离职。复职消息公布后，市场反应强烈，股价单日涨幅接近30%。马斯克、奥尔特曼等科技界领袖及特朗普均公开支持其回归，认为此举符合股东及合作伙伴利益。

**重点**：复职引发股价剧烈波动，显示市场对其领导力的信心

**来源**：[IT之家](https://www.ithome.com/1/031/251.htm) · [V2EX 最热主题](https://www.v2ex.com/t/1259265#reply48) · [IT之家](https://www.ithome.com/1/031/389.htm) · [IT之家](https://www.ithome.com/1/031/207.htm)

### 22. 特朗普宣称促成黄仁勋回归，引发政治争议

![特朗普宣称促成黄仁勋回归，引发政治争议](https://daringfireball.net/misc/2026/11/trump-huang-truth-social.jpeg)

美国总统特朗普在博客及CNBC采访中声称，黄仁勋的复职是他达成的“交易”成果，并向董事会保证黄仁勋不构成国家安全风险。这一直接干预行为被评论人士认为精准捕捉了当下政治与商业交织的氛围。然而，随着民主党重掌国会，预计将对特朗普的干预动机及英伟达的出口管制违规情况展开深入调查，政治压力持续存在。

**重点**：总统直接干预企业人事，加剧地缘政治与商业的纠缠

**来源**：[daringfireball.net](https://truthsocial.com/@realDonaldTrump/posts/117666713950631493) · [TechCrunch](https://techcrunch.com/2026/11/23/jensen-huang-isnt-out-of-the-woods-yet/) · [TechCrunch](https://techcrunch.com/2026/11/23/nvidia-reverses-course-and-brings-jensen-huang-back-as-ceo/)

### 23. 公司治理专家质疑复职先例，担忧长期影响

![公司治理专家质疑复职先例，担忧长期影响](https://images.theconversation.com/files/773685/original/file-20261123-62-2aaryt.jpg?ixlib=rb-4.1.1&rect=0%2C0%2C3799%2C2532&q=45&auto=format&w=1050&h=700&fit=crop)

The Conversation 指出，黄仁勋在被罢免仅11天后重返职位，虽获行业支持，但为英伟达公司治理树立了不良先例。研究数据显示，当董事会严肃对待高管不当行为时，公司长期表现往往更好。此次快速复职可能削弱董事会的独立性，引发投资者对英伟达内部监督机制有效性的担忧，影响其长期治理信誉。

**重点**：快速复职可能削弱董事会独立性，引发治理信誉担忧

**来源**：[The Conversation](https://theconversation.com/nvidias-jensen-huang-is-getting-his-ceo-job-back-but-history-shows-companies-perform-better-when-corporate-boards-take-executive-misbehavior-seriously-281689)

### 24. 黄仁勋将出席国会听证，聚焦AI优势保护

![黄仁勋将出席国会听证，聚焦AI优势保护](https://foreignpolicy.com/wp-content/uploads/2022/01/Palmer-James-foreign-policy-columnist20.jpg?quality=90)

复职后，黄仁勋面临更密集的政治审视。他将于12月1日和3日分别出席美国众议院和参议院听证会。其中，12月3日由参议院银行委员会主持的公开听证会主题为“保护美国的人工智能优势”。此次听证不仅涉及其个人背景，更将深入探讨英伟达芯片出口管制合规性及美国AI战略地位，是复职后首个重大政治考验。

**重点**：国会听证将检验其个人背景及美国AI战略合规性

**来源**：[IT之家](https://www.ithome.com/1/031/456.htm) · [Hacker News 首页](https://foreignpolicy.com/2026/11/23/jensen-huang-nvidia-return-ceo-national-security-scandal/) · [TechCrunch](https://techcrunch.com/2026/11/23/jensen-huang-scheduled-to-testify-next-week-in-senate-following-reinstatement-as-nvidia-ceo/)

## 科技巨头并购与融资动态

### 25. CrowdStrike 439亿美元全股票收购 Zscaler

![CrowdStrike 439亿美元全股票收购 Zscaler](https://img.ithome.com/newsuploadfiles/2026/11/3de90e17-6212-4e89-ab0f-ed7726be0b41.jpg)

CrowdStrike 宣布以 439 亿美元全股票交易收购网络安全同行 Zscaler，每股 Zscaler 股票兑换 1.135 股 CrowdStrike 股票，隐含溢价 34%。合并后企业预计年度经常性收入超 100 亿美元，旨在整合端点保护与零信任平台，构建“网络安全操作系统”以应对 AI 驱动威胁，并挑战 Palo Alto Networks 的市场地位。交易预计于 2027 年底至 2028 年初完成，需获监管批准。

**重点**：网络安全行业最大规模整合，重塑 AI 时代安全格局

**来源**：[IT之家](https://www.ithome.com/1/031/188.htm) · [TechCrunch](https://techcrunch.com/2026/11/23/crowdstrike-to-acquire-zscaler-for-44-billion/) · [Hacker News AI](https://www.cnbc.com/2026/11/23/crowdstrike-zscaler-aquisition-ai-cyberattacks.html) · [FreeBuf](https://www.freebuf.com/news/514198.html)

### 26. 亚马逊 75 亿美元收购 Decart 强化 Trainium 芯片

![亚马逊 75 亿美元收购 Decart 强化 Trainium 芯片](https://techcrunch.com/wp-content/uploads/2024/12/Decart-Founders-Dean-Leitersdorf-CEO-and-Moshe-Shalev-CPO.jpg)

亚马逊宣布以 75 亿美元收购以色列 AI 初创公司 Decart，获取其核心产品 Decart Optimization Stack (DOS) 及研发团队。此举旨在通过软硬件协同优化提升 AI 模型在自研 Trainium 芯片上的运行效率，降低训练与推理成本，从而增强与英伟达竞争的实力。Decart 此前曾与 Anthropic 和 Nvidia 进行谈判，最终选择加入亚马逊，其技术自 2025 年起已协助优化 Trainium 性能。

**重点**：亚马逊加码自研芯片生态，正面挑战英伟达主导地位

**来源**：[Hacker News AI](https://www.calcalistech.com/ctechnews/article/g0mtcg4mi) · [TechCrunch](https://techcrunch.com/2026/11/23/amazon-snaps-up-decarts-ai-optimization-tech-for-7-5b-as-it-prepares-to-sell-trainium-chips/) · [IT之家](https://www.ithome.com/1/031/262.htm)

### 27. Sierra 估值半年翻倍至 300 亿美元

前 Salesforce 联席 CEO Bret Taylor 联合创办的企业客户体验公司 Sierra 完成 17.5 亿美元 F 轮融资，估值在六个月内翻倍至 300 亿美元。本轮由 Greenoaks 和 Lightspeed 领投，Benchmark、红杉等跟投。Sierra 目前服务近 50% 的财富 500 强企业，其基于结果的定价模式使年化收入在 5 个月内翻倍至 4 亿美元。公司计划利用新资金加强技术栈并扩大销售团队，以在 AI 驱动的 CX 领域保持竞争优势。

**重点**：AI 客户体验赛道爆发，Sierra 成为独角兽标杆

**来源**：[TechCrunch](https://techcrunch.com/2026/11/23/sierra-doubles-valuation-to-30b-within-six-months-as-demand-for-ai-in-cx-takes-off/)

### 28. SpaceX 与特斯拉成立特别委员会推进合并

据英国金融时报报道，马斯克旗下的 SpaceX 和特斯拉已任命五名董事成立特别委员会，负责推进两家公司合并谈判。委员会成员包括来自 SpaceX 的 Roelof Botha 和 Randy Glein，以及来自特斯拉的 Robyn Denholm 等三人。目前顾问正在微调财务模型，双方有望于 12 月宣布合并协议。若达成，这将成为全球规模最大的企业合并交易之一，标志着马斯克商业版图的进一步整合。

**重点**：马斯克两大巨头有望合并，或成全球最大企业交易

**来源**：[IT之家](https://www.ithome.com/1/031/485.htm)

### 29. 知乎间接投资 DeepSeek 股价大涨

![知乎间接投资 DeepSeek 股价大涨](https://img.ithome.com/newsuploadfiles/2026/11/5e8b77cb-02fe-4784-90f9-2e92a56331aa.png)

知乎宣布通过基金间接投资 DeepSeek，取得低个位数股权，消息公布后其港股股价大涨 10%，美股涨约 15.76%。工商变更显示 DeepSeek 运营主体新增股东杭州程砚，注册资本增加约 21.1%。据知情人士透露，DeepSeek 本轮融资规模达 1000 亿至 1055 亿元，投后估值约 6155 亿元，叠加此前融资累计超 1500 亿元。创始人梁文锋持股比例约 67.42%，控制权未变。

**重点**：DeepSeek 巨额融资落地，知乎借势股价飙升

**来源**：[IT之家](https://www.ithome.com/1/031/339.htm)

## 英伟达变局：黄仁勋回归与地缘政治博弈

### 30. 黄仁勋重返总部获员工英雄式欢迎，承诺成为更好CEO

![黄仁勋重返总部获员工英雄式欢迎，承诺成为更好CEO](https://i.insider.com/6b048e2673f126f9eccb99e9?width=400&format=jpeg&auto=webp)

在辞职约两周后，黄仁勋重返英伟达总部，受到数百名员工的夹道欢迎。此前支持者发起的“Stand with Jensen”请愿获得超20万人联署。黄仁勋在回归仪式上向员工道歉，感谢董事会及团队在过渡期间的支持，并表示迫不及待投入工作，承诺将努力成为更优秀的CEO，带领公司迎接新一轮工业革命。这一场景被视为公司凝聚力恢复的重要信号。

**重点**：20万员工联署支持，回归即获“英雄”待遇

**来源**：[daringfireball.net](https://www.businessinsider.com/jensen-huang-returns-to-nvidia-hq-im-terribly-sorry-2026-11) · [TechCrunch](https://techcrunch.com/2026/11/23/nvidia-employees-greet-jensen-huang-like-a-hero-as-he-returns-to-companys-hq/)

### 31. 新加坡Megaspeed被美列入实体清单，芯片走私调查升级

![新加坡Megaspeed被美列入实体清单，芯片走私调查升级](https://techcrunch.com/wp-content/uploads/2026/11/GettyImages-2303986898.jpg)

美国商务部宣布将新加坡云与AI基础设施提供商Megaspeed及其子公司Speedmatrix列入“实体清单”，限制其获取美国制造的半导体。此举源于Megaspeed前CEO Alice Huang被指控为中国间谍，且该公司被怀疑通过新加坡实体将英伟达芯片非法走私至中国。这一行动标志着围绕黄仁勋丑闻的地缘政治博弈进一步升级，旨在防止敏感技术流向威胁美国国家安全的一方。

**重点**：针对芯片走私嫌疑，美新两国展开联合调查

**来源**：[TechCrunch](https://techcrunch.com/2026/11/23/megaspeed-the-company-at-the-center-of-the-jensen-huang-scandal-appears-headed-for-a-u-s-blacklist/) · [Hacker News AI](https://www.bbc.co.uk/news/articles/cv98xpg5dg5zo)

## 英伟达治理风波与芯片产业动态

### 32. 美财长贝森特软化对黄仁勋回归立场

![美财长贝森特软化对黄仁勋回归立场](https://img.ithome.com/newsuploadfiles/2026/11/6ac133b0-408c-4a82-a73e-b98d2cd9f6b8.jpg)

美国财长贝森特在采访中改口称已辞职的黄仁勋属于英伟达“外部人士”，不反对其重返公司，此前他曾批评英伟达存在“不合规文化”。尽管特朗普公开支持黄仁勋回归，但英伟达董事会主席表示董事会无意恢复其职位，目前由CFO Colette Kress担任临时CEO，合规调查仍在进行中。

**重点**：政治阻力降低，董事会仍持保留态度

**来源**：[IT之家](https://www.ithome.com/1/030/811.htm) · [Dev.to](https://dev.to/jimclydegm/bessent-softens-on-huang-return-as-nvidia-board-resists-1jaj)

### 33. Arm CEO哈斯续约至2033年并兼任软银副董事长

![Arm CEO哈斯续约至2033年并兼任软银副董事长](https://img.ithome.com/newsuploadfiles/2026/11/304993d0-b6e8-4667-bbb7-15fe115c9dd5.png)

Arm 宣布 CEO Rene Haas 续约至 2033 年，并将自 2026 年 12 月 1 日起兼任最大股东软银集团副董事长。此举旨在稳定领导层并深化与软银的合作，同时也回应了此前关于其可能接替英伟达 CEO 黄仁勋的市场传闻，显示 Arm 在芯片架构领域的长期战略定力。

**重点**：稳定领导层，回应接任英伟达传闻

**来源**：[IT之家](https://www.ithome.com/1/031/200.htm)

## 趋势观察

AI从工具演变为**科研主体**与**治理变量**，黎曼猜想的突破预示数学研究范式转移，而黄仁勋复职则折射出科技巨头在**地缘政治**与**公司治理**间的微妙平衡。未来，**可验证性**将成为AI安全与信任的核心，企业需在效率与合规间寻找新锚点。

---

*本报告由 RSS-Claw 岛屿日报 AI 自动生成*


---

## 📎 产品机会雷达 · 2026-11-24

### 💡 今日新机会

- **Firecrawl: 智能体知识基础设施**
  > 通过单一 API 聚合搜索、抓取及 550+ 数据提供商，为 AI 智能体提供标准化的数据接入能力。
  **目标用户**：构建需要实时、多源数据支持的 AI 智能体应用的开发者
  **痛点**：现有 AI 智能体获取外部知识主要依赖通用搜索引擎或单一 API，缺乏对结构化数据、垂直领域数据源（如 550+ 提供商）的统一接入和标准化处理，导致数据获取成本高且覆盖面有限。
  **现有替代**：通用搜索引擎 API, 单一数据源 API, 自建爬虫集群
  **为什么现在**：GitHub Trending 显示 Firecrawl 项目热度极高（990 points），表明市场对智能体数据基础设施的需求正在爆发，且现有解决方案碎片化严重。
  **1周验证**：在 GitHub 或 V2EX 发起讨论，收集开发者对“统一数据接入”的需求反馈；尝试接入 3-5 个主流数据源，测试 API 延迟和稳定性。
  **MVP 功能**：统一数据接入 API；550+ 数据提供商聚合；标准化数据格式输出
  **变现**：按 API 调用量或数据源数量订阅收费
  **证据**：github-trending:firecrawl_firecrawl
  *分类：AI 基础设施*

- **Diagram Design: AI 编码智能体的“编辑级”图表生成技能包**
  > 提供包含 52 种图表类型的 Agent Skill，支持生成自包含的 HTML+SVG 图表，具备“编辑级”设计美学，可直接嵌入代码库或文档。
  **目标用户**：使用 Claude Code、Cursor 等 AI 编码工具进行前端开发或文档编写的工程师
  **痛点**：AI 生成的图表（如架构图、流程图）往往风格单一、缺乏设计感，难以直接用于专业文档或演示，且现有工具多依赖外部 SaaS 或复杂的 SVG 代码手写，缺乏针对 AI Agent 的标准化、高审美图表生成能力。
  **现有替代**：Mermaid.js, Draw.io, 手写 SVG
  **为什么现在**：GitHub Trending 显示 diagram-design 项目热度高（794 points），且 AI 编码工具普及使得“代码即设计”的需求激增，现有图表工具与 AI Agent 的集成度不足。
  **1周验证**：在 V2EX 或即刻分享 3-5 个由该 Skill 生成的精美图表案例，观察开发者反馈；测试其在 Claude Code 中的调用成功率。
  **MVP 功能**：52 种图表类型支持；自包含 HTML+SVG 输出；编辑级设计美学模板
  **变现**：开源免费 + 高级模板/插件订阅
  **证据**：github-trending:cathrynlavery_diagram-design
  *分类：AI 开发工具*

- **MiniMind: “两小时从零训练”微型 LLM 体验工具**
  > 提供开源工具，支持在消费级硬件上快速训练 64M 参数的小型 LLM，通过可视化界面展示训练过程，降低“从零训练”的认知和工程门槛。
  **目标用户**：希望深入理解 LLM 训练原理、但受限于算力或时间的开发者及学生
  **痛点**：现有 LLM 训练工具要么过于复杂（需配置分布式集群），要么过于抽象（仅展示结果），缺乏一种“轻量级、可交互、快速反馈”的工具，让开发者能在短时间内（如 2 小时）体验从数据预处理到模型收敛的完整训练流程。
  **现有替代**：Hugging Face Transformers, PyTorch 原生训练脚本
  **为什么现在**：GitHub Trending 显示 MiniMind 项目热度高（727 points），AI 教育市场存在“重推理、轻训练”的空白，开发者对“动手理解原理”的需求强烈。
  **1周验证**：在技术社区（如 V2EX, 即刻）发布“2 小时训练一个小模型”的体验帖，收集用户反馈；测试其在不同硬件上的运行稳定性。
  **MVP 功能**：64M 参数小模型训练；消费级硬件支持；训练过程可视化
  **变现**：开源免费 + 云托管训练服务收费
  **证据**：github-trending:jingyaogong_minimind
  *分类：AI 教育*

- **OpenSRE: CI/CD 可靠性智能体**
  > 提供开源的 CI/CD 可靠性智能体，能够实时监控流水线状态，自动分析失败原因，并执行修复操作（如重试、回滚、通知），实现“无人值守”的发布可靠性保障。
  **目标用户**：DevOps 工程师及 SRE 团队
  **痛点**：传统 CI/CD 监控依赖静态规则和人工响应，缺乏对构建失败、部署异常等复杂场景的自动化诊断和自愈能力，导致发布流程中断时恢复时间长，影响交付效率。
  **现有替代**：Jenkins 插件, GitLab CI 内置监控, Datadog
  **为什么现在**：GitHub Trending 显示 OpenSRE 项目热度上升（408 points），DevOps 领域对“智能运维”的需求从监控转向自愈，AI Agent 在故障诊断中的能力得到验证。
  **1周验证**：在 DevOps 社区（如 V2EX, 即刻）分享 OpenSRE 的故障自愈案例；测试其在典型 CI/CD 平台（如 GitHub Actions, GitLab）中的集成难度。
  **MVP 功能**：流水线状态实时监控；失败原因自动分析；自动化修复操作（重试/回滚）
  **变现**：开源免费 + 企业版 SaaS 服务
  **证据**：github-trending:Tracer-Cloud_opensre
  *分类：AI 基础设施*

- **Viewport-Compiled Browser MCP: 解决 AI 智能体网页交互的 Token 爆炸问题**
  > 提供“视口编译”技术的浏览器 MCP，通过只提取用户当前可见区域的精简 DOM 结构，将 Token 消耗降低 90% 以上，实现高效、低成本的网页交互。
  **目标用户**：构建需要与网页深度交互（如自动化测试、数据抓取）的 AI 智能体应用的开发者
  **痛点**：现有浏览器 MCP（如 Playwright MCP）在将网页 DOM 传递给 LLM 时，往往包含大量冗余信息，导致 Token 消耗巨大且上下文窗口易满，影响智能体执行效率和成本。
  **现有替代**：Playwright MCP, browser-use, Selenium
  **为什么现在**：V2EX 上关于“视口编译浏览器 MCP”的讨论热度高，开发者普遍反映现有浏览器 MCP 的 Token 成本过高，且“视口编译”技术能有效解决这一痛点。
  **1周验证**：在 V2EX 或即刻分享“视口编译”技术的原理和效果数据；测试其在典型网页交互任务（如表单填写、数据抓取）中的 Token 消耗对比。
  **MVP 功能**：视口编译技术；精简 DOM 结构提取；Token 消耗降低 90%
  **变现**：开源免费 + 商业授权
  **证据**：v2ex:create:1259480
  *分类：AI 基础设施*


### 📡 待验证信号

- **Claude BugHunter: AI 编码智能体的“红队测试”技能包**

- **Last30Days Skill: AI 智能体的“多源信息综合”技能**

- **Ponytail: AI 智能体的“懒惰高级开发者”思维模式**

- **Stitch Skills: Google Labs 的 AI 智能体技能库**

- **Cursor Plugins: Cursor 官方插件规范**


### 🔨 本周建议动手

- **验证 Firecrawl 的“知识基础设施”定位**

- **测试 Diagram Design 的“编辑级”图表生成能力**

- **体验 MiniMind 的“两小时从零训练”流程**

- **评估 OpenSRE 的 CI/CD 可靠性智能体**

- **验证 Viewport-Compiled Browser MCP 的 Token 优化效果**



---

## 📎 arXiv Artificial Intelligence · 2026-11-24

### 📄 论文列表

- **语言模型能响应注入的不确定性标记，但无法进行原位自我监控**
  *Language Models Steer on Injected Uncertainty Tokens, but Fail to Self-Monitor In Situ*

  📄 `arXiv:2611.31228` · cs.AI
  👥 **作者**：Daniel Theron
  📝 **摘要**：本文探讨了语言模型在代理推理中通过口头化置信度触发回溯和纠错的能力。研究评估了Qwen2.5-7B、Llama-3.1-8B、Mistral-7B和Phi-4四个开源模型在15,200次数学基准测试中的表现，并针对2,017个推理错误点应用了27,568次反事实延续。结果显示，模型在“监控”与“控制”之间存在显著解耦：所有模型均无法有效检测自身错误，口头化置信度在错误步骤与正确推理间几乎无区分度（AUROC接近0.5），且轨迹置信度通常饱和在95%以上。然而，模型对“外部不确定性”响应良好，在错误步骤注入低置信度标记能显著提升下游纠错率。结论指出，推理时自我修正的瓶颈在于原位错误检测能力，而非下游修复能力。
  🔗 [PDF](https://arxiv.org/pdf/2611.31228v1)

- **CTLink：一种将放射学报告发现与3D胸部CT扫描关联的文本提示分割模型**
  *CTLink: A Text-Prompted Segmentation Model for Linking Radiology Report Findings to 3D Chest CT Scans*

  📄 `arXiv:2611.31222` · cs.CV, cs.AI
  👥 **作者**：Mohammed Baharoon, Sung Eun Kim, Mahmoud Hussain Alabbad, Lucas Bijnens, Ali Piracha, Reem Alwasiah, Talal Yahyan, Abdulrahman Alamoudi, Mashael Alshehri, Rayan Alsager, Hannah Hancock, Anna M. Hunkemöller, Peter Youssef, Mona A. Alhammad, Afnan Aljumayan, Brecht Van Berkel, Eric Bijnens, Saud Alhussain, Maarten Steyvers, Rolf Symons, Bryan Eelen, Ayed Alaklubi, Maha Buraykan Alshammari, Amirah Fahad Alshammeri, Tomas Gilvydis, Ibrahim AlTurki, Monerah Almohideb, Ali Alburkani, Shahad Alhomaiani, Fatima Jabali, Abdulrhman Aljouie, Daesung Kim, Junha Im, Michael Moritz, Hassan R. Alomaish, Pranav Rajpurkar
  🏛️ **单位**：Department of Biomedical Informatics, Harvard Medical School, Boston, MA, USA; King Fahad Hospital, Al-Ahsa Health Cluster, Al Hofuf, Saudi Arabia; KU Leuven, Leuven, Belgium; Saint Louis University, St Louis, MO, USA; Medical Imaging Department, King Abdulaziz Medical City, Ministry of National Guard Health Affairs, Riyadh, Saudi Arabia; Naval Medical Center Portsmouth, Portsmouth, VA, USA; Institute of Diagnostic and Interventional Radiology, Hannover Medical School, Hannover, Germany; Biomedical Research in Endstage and Obstructive Lung Disease Hannover (BREATH), German Center for Lung Research (DZL), Hannover, Germany; Justus Liebig University Giessen, Giessen, Germany; Ras Tanura General Hospital, Ministry of Health, Ras Tanura, Saudi Arabia; Jessa Hospital, Hasselt, Belgium; King Fahad Specialist Hospital, Buraydah, Saudi Arabia; University Hospitals Leuven, Leuven, Belgium; Imelda Hospital, Bonheiden, Belgium; Prince Sultan Military Medical City, Riyadh, Saudi Arabia; University of Hail, Hail, Saudi Arabia; King Saud University Medical City, Riyadh, Saudi Arabia; King Abdulaziz Specialist Hospital, Taif Health Cluster, Taif, Saudi Arabia; King Abdulaziz University Hospital, Jeddah, Saudi Arabia; Research and Innovation Institute, Ministry of Defense Health Services, Riyadh, Saudi Arabia; Yonsei University, Seoul, South Korea; Yonsei University College of Medicine, Seoul, South Korea; SSM Health, St Louis, MO, USA
  📝 **摘要**：针对放射学报告仅以文本描述发现而无法在扫描图像上直观标记的问题，本文提出了CTLink，一种基于文本提示的3D分割模型，用于分割胸部CT报告中描述的发现。CTLink在4123例非对比胸部CT扫描和9547个分割报告发现上进行训练，包括新标注的ReXGroundingCTv2数据集。在验证集上，CTLink的命中率（0.816）、实例F1分数（0.456）和平均Dice分数（0.400）均显著优于现有公开模型VoxTell。在MICCAI 2026 ReXGrounding挑战赛中，CTLink集成模型取得了最高的命中率和实例F1分数。此外，在独立放射科医生双重分割的测试中，CTLink的表现达到或超过了医生间一致性。弥漫性非局灶性发现仍是主要局限，模型权重和数据集已公开。
  🔗 [PDF](https://arxiv.org/pdf/2611.31222v1)

- **空间探索：评估视觉-语言模型空间推理中有目的主动探索的基准**
  *Seeking in Space: Benchmarking Purposeful Active Exploration of Vision-Language Models for Spatial Reasoning*

  📄 `arXiv:2611.31215` · cs.AI
  👥 **作者**：Xiwei Liu, Yulong Li, Xuhui Li, Xinlin Zhuang, Zhixiang Lu, Haolin Yang, Jianxu Chen, Yifan Lu, Zhiran Zhang, Yutong Xie
  🏛️ **单位**：Mohamed bin Zayed University of Artificial Intelligence, The Chinese University of Hong Kong, University of Liverpool
  📝 **摘要**：本文提出了ActSpace-Bench，一个包含994个问题和234个探索片段的基准，旨在评估视觉-语言模型（VLMs）在真实室内场景中主动寻找证据以回答空间问题的能力。该基准要求模型从单一视角出发，导航真实捕获的帧，并在回答前收集证据。为了评估探索是否有目的性，研究引入了一种受控评估协议，将模型自身的探索与相同预算的随机游走及神谕路线进行比较，从而分离证据寻找与空间推理能力。对23个专有、开源及空间专用VLMs的评估显示，最强模型虽能进行有目的的探索，但因记忆有限而丢失大量证据；而较弱或专用模型的表现往往不优于随机游走。研究指出，记忆能力和基于证据的推理是主动空间智能的下一个关键目标。
  🔗 [PDF](https://arxiv.org/pdf/2611.31215v1)

- **ToolSmith：面向多模态搜索智能体的自动工具生成框架**
  *ToolSmith: An Automatic Tool-Generation Framework for Multimodal Search Agents*

  📄 `arXiv:2611.31198` · cs.CL, cs.AI, cs.CV
  👥 **作者**：Rui Sun, Junhua Huang, Luca Zancato, Md Mofijul Islam, Kai-Wei Chang
  🏛️ **单位**：University of California, Los Angeles, AWS GenAI
  📝 **摘要**：现有多模态搜索智能体依赖手工构建的小型工具库来回答超出参数化知识的问题，但维护成本高且难以适应新的查询类型和失败模式。受人类从熟悉部件中创造新工具并跨任务复用的启发，本文提出了ToolSmith，一个自动工具生成框架，能够在精简的基础工具库之上生长和复用模块。该框架通过自动扩展工具库，使智能体能够处理更复杂的证据格式。在三个领域内多模态搜索基准和十个领域外基准的评估中，采用VLM-as-a-Judge协议，ToolSmith在不同规模的部署智能体上均一致优于基础库，且更大的骨干模型获益更多，证明了该方法的可扩展性。代码和数据已公开。
  🔗 [PDF](https://arxiv.org/pdf/2611.31198v1)

- **学习神经血管代码用于EEG到fMRI的合成**
  *Learning Neurovascular Codes for EEG-to-fMRI Synthesis*

  📄 `arXiv:2611.31194` · cs.LG, cs.AI
  👥 **作者**：Yiming Sun, Yifan Wang, Aosong Feng, Yijia Ma, Ben Cheng, Xurui Wang, Yufan He, Yucheng Tang, Qing Lyu, Daguang Xu, Pei-Fen Kuan, Mingzhou Ding, Wen Li, Chenyu You
  🏛️ **单位**：Stony Brook University, University of Toronto, Yale University, UTHouston, NVIDIA, University of Florida
  📝 **摘要**：本文引入了“神经血管代码”（Neurovascular Codes）作为fMRI生成的共享EEG表示。首先训练独立的EEG编码器预测每个fMRI信号，从相同的EEG窗口中学习目标特定的时频特征。随后冻结编码器，将其拼接的隐藏特征投影到共享的神经血管代码中。基于该代码，随机插值器将高斯噪声转换为fMRI信号向量，允许对同一EEG窗口采样不同的响应。在八个公开的同时EEG-fMRI数据集（包括静息态和任务态，共61,646个体素级对）上评估，该模型在受试者内和保留受试者评估中，平均Pearson相关系数分别比最强编码器基线提高19.1%和19.8%，比最强生成器基线提高18.8%和47.9%。此外，在基于真实fMRI训练的主体识别分类器中，该方法取得了最高平均准确率，为跨模态大脑建模提供了新机会。
  🔗 [PDF](https://arxiv.org/pdf/2611.31194v1)



---

## 📎 arXiv Machine Learning · 2026-11-24

### 📄 论文列表

- **自动驾驶VLA模型剪枝：推理与动作中应保留什么**
  *Pruning Autonomous Driving VLAs: What to Preserve for Reasoning and Action*

  📄 `arXiv:2611.31240` · cs.CV, cs.LG, cs.RO
  👥 **作者**：Seongchan Kim, Soowon Son, Sangoh Kim, Hyunah Ko, Eunbeen Hong, Hyunkoo Lee, Sanghyun Lee, WonJun Moon, Kihong Kim, Dongyeon Son, Woongchan Nam, Seungryong Kim
  🏛️ **单位**：KAIST, LG Innotek
  📝 **摘要**：本文研究了用于自动驾驶的推理视觉-语言-动作（VLA）模型的结构化剪枝方法，旨在平衡场景理解与轨迹预测的性能。通过分析Alpamayo-1.5-10B模型的泰勒重要性，发现推理目标和轨迹目标对同一视觉-语言模型（VLM）结构赋予的重要性不同。在动作专家模块中，MLP通道在不同去噪步骤中的重要性排名比查询头更稳定，且少数通道占据了大部分重要性。基于此，作者提出了MoOP方法，结合两个目标的重要性排名进行VLM剪枝，并聚合逐步重要性以选择固定的专家MLP通道子集。实验表明，在24.0%的参数缩减下，MoOP在驾驶任务中表现优于或持平于最强基线，同时保留了94.0%的LingoQA分数。在30.0%的高缩减率下，MoOP是唯一推理能力未崩溃的方法。进一步移除93.75%的专家MLP通道后，总参数缩减达39.4%，模型实现了1.37倍的端到端推理加速和36.6%的峰值内存降低，且无需剪枝后微调。
  🔗 [PDF](https://arxiv.org/pdf/2611.31240v1)

- **让视觉-语言模型通过其表征生成图像**
  *Let Vision-Language Models Generate Images through Their Representations*

  📄 `arXiv:2611.31237` · cs.CV, cs.LG
  👥 **作者**：JB Kim, Byungwoo Jeon, Kyungmin Lee, Hyeonmo Kang, Cheonbok Park, Shinyoung Joo, Jinwoo Shin, Jeonghoon Kim
  🏛️ **单位**：NAVER Cloud, Korea Advanced Institute of Science and Technology
  📝 **摘要**：本文提出了一种名为Integral的方法，旨在将预训练的视觉-语言模型（VLM）转化为统一的多模态模型，以解决视觉理解与生成中表征异构性的挑战。Integral通过构建共享的视觉表征空间来整合这两种能力，包含两个互补组件：抽象融合（Abstraction Fusion）通过聚合冻结视觉编码器的层级表征来构建共享视觉标记；块级混合专家（Block-wise MoT）引入轻量级生成流，仅在块边界处与VLM交互。该方法有效保留了预训练的理解能力，同时扩展了强大的视觉生成能力。受控对比实验表明，尽管重建保真度相当，但在理解与生成之间共享视觉表征能显著改善生成学习。这些结果证明，预训练VLM学到的表征已为视觉生成提供了有效基础。
  🔗 [PDF](https://arxiv.org/pdf/2611.31237v1)

- **TowerBridge：通过权重空间编程弥合双编码器模态间隙**
  *TowerBridge: Bridging the Dual-Encoder Modality Gap via Weight-Space Programming*

  📄 `arXiv:2611.31233` · cs.CV, cs.LG
  👥 **作者**：Hani Alomari, Md Atabuzzaman, Chris Thomas
  🏛️ **单位**：Department of Computer Science, Virginia Tech
  📝 **摘要**：本文针对CLIP风格双编码器中图像和文本映射到共享嵌入空间时存在的模态间隙问题，提出了TowerBridge方法。研究发现，事后移除模态间隙会降低检索性能，而轻微衰减特定方向则能改善检索。作者引入了一种配对统计量，用于识别双塔在难负样本上比匹配对更一致的方向。通过权重空间编程，由LLM代理指导，无需反向传播即可编写闭式权重编辑。TowerBridge是一种基于难负样本边际一阶分析的闭式配方，仅需从25,000个标记对计算数秒，无需模型特定调优，且不改变架构和推理成本。实验显示，TowerBridge在21个CLIP检查点上平均将COCO测试检索RSUM提高16.8，Flickr30k测试检索提高6.6，同时将ImageNet零样本准确率下降限制在0.5点以内，并减少了hubness现象。
  🔗 [PDF](https://arxiv.org/pdf/2611.31233v1)

- **线性模型能走多远？BiPert：单细胞扰动建模的统一框架**
  *How Far Can Linear Go? BiPert, a Unified Framework for Single-Cell Perturbation Modelling*

  📄 `arXiv:2611.31227` · cs.LG, q-bio.CB, q-bio.GN, q-bio.QM
  👥 **作者**：Abhishek Sharma, Aleksej Zelezniak
  🏛️ **单位**：Randall Centre for Cell & Molecular Biophysics, King’s College London, Department of Life Sciences, Chalmers University of Technology, Institute of Biotechnology, Life Sciences Centre, Vilnius University
  📝 **摘要**：本文提出了BiPert，一个用于单细胞扰动建模的简单线性框架，旨在解决预测未见细胞类型中的扰动响应和从转录效应中识别扰动基因这两个挑战。BiPert基于将转录响应分解为共享和扰动特定组件的线性原理，同时支持前向预测和反向识别。在前向预测中，BiPert在预测未见细胞系的基因表达变化时优于不使用外部生物知识的现有方法；其少样本扩展BiPert-FS仅需十个测量扰动即可适应新细胞系。在反向识别中，BiPert-ID从单细胞表达谱中识别扰动基因，在未见细胞系和供体中优于深度学习模型。研究还发现，跨细胞背景转移更一致的扰动也更容易被识别。这些结果建立了扰动转移与识别之间的联系，证明简单线性模型可为这两项任务提供强大且可解释的基线。
  🔗 [PDF](https://arxiv.org/pdf/2611.31227v1)

- **通过互信息最大化实现自监督数据集蒸馏**
  *Self-Supervised Dataset Distillation via Mutual Information Maximization*

  📄 `arXiv:2611.31225` · cs.CV, cs.LG
  👥 **作者**：Mohammad Hossein Moslemi, Mahdi Beitollahi, Zhimin Mei, Jiale Cai, Bissan Ghaddar, Boyu Wang
  🏛️ **单位**：Western University, Queen’s University, Ivey Business School, Vector Institute
  📝 **摘要**：本文介绍了MIPA（互信息原型对齐），一种高效的自监督学习（SSL）数据集蒸馏方法，旨在优化合成图像以保留增强不变信息。尽管数据集蒸馏在监督学习中取得成功，但在SSL中仍探索不足，因为蒸馏数据必须保留学习跨增强一致表征所需的信息。MIPA将合成图像视为可学习原型，并使用冻结编码器基于特征相似度将真实样本分配给它们。为了鼓励这种增强不变性，MIPA最大化跨视图分配之间的互信息，同时避免所有真实样本仅分配到少数合成原型的平凡解。在图像分类基准上的评估表明，MIPA生成的合成数据比现有蒸馏方法产生更高质量的表征，同时减少了蒸馏过程中的时间和存储需求。
  🔗 [PDF](https://arxiv.org/pdf/2611.31225v1)



---

## 📎 arXiv Computation and Language · 2026-11-24

### 📄 论文列表

- **CO-GRAFT：通过角色级策略嫁接归因搜索智能体中的强化学习增益**
  *CO-GRAFT: Attributing Reinforcement Learning Gains in Search Agents via Role-Level Policy Grafting*

  📄 `arXiv:2611.31185` · cs.IR, cs.AI, cs.CL
  👥 **作者**：Ramraj Chandradevan, Sayontan Ghosh, Vinoth Selvendran
  📝 **摘要**：本文提出CO-GRAFT，一种奖励无关的干预式归因框架，用于解析强化学习（RL）在大型语言模型搜索智能体中带来的性能增益。该方法让RL训练后的智能体与其预RL初始化版本在闭环执行中共同生成轨迹，每个策略控制四个互斥功能角色（中间推理、搜索/回答决策、查询生成、答案提取）的子集。通过评估所有16种角色分配组合，利用Shapley值分解总增益，并用Möbius交互项区分独立角色改进与多角色耦合。在Qwen2.5和Llama-3.2模型上的实验表明，查询生成贡献不超过15%的总增益；增益主要受预RL答案有效性、搜索保留率、模型规模及任务级搜索预算控制。大模型或格式良好的检查点将信用从推理转向答案提取，而小型基础模型则依赖推理与决策的耦合。
  🔗 [PDF](https://arxiv.org/pdf/2611.31185v1)

- **LLM后训练中跨块数的精度感知学习率迁移**
  *Precision-Aware Learning Rate Transfer Across Block Count in LLM Post-Training*

  📄 `arXiv:2611.31166` · cs.LG, cs.CL
  👥 **作者**：Nan Chen, Soledad Villar, Soufiane Hayou
  🏛️ **单位**：Department of Applied Mathematics and Statistics, Johns Hopkins University
  📝 **摘要**：针对预训练大语言模型后训练（如SFT、DPO、RLVR）对学习率敏感且网格搜索成本高昂的问题，本文提出TipSweep方法，实现跨可训练Transformer块数的学习率迁移。该方法仅训练最后k0个块（通常k0=1）来搜索最佳学习率，并提供缩放规则预测训练任意k个块（包括全模型）时的最优学习率。在1B至7B参数模型的实验中，发现最优学习率遵循精度依赖的缩放规则：使用FP32主权重时近似为k^-1，直接更新BF16权重时近似为k^-1/2。作者通过考虑更新舍入误差的分析模型解释了这些规则。此外，开发了两个原型：一个可在16GiB内存的消费级GPU上运行，另一个通过单次数据遍历评估所有候选学习率，使五候选搜索的GPU耗时仅为全深度运行的一半。
  🔗 [PDF](https://arxiv.org/pdf/2611.31166v1)

- **Deneb-Vritra：通过恢复令牌表示和注意力阻断来考察描述、边和名称**
  *Deneb-Vritra: Descriptions, Edges and Names Examined by Blocking Via Restoring Token Representations and Attention*

  📄 `arXiv:2611.31139` · cs.CL, cs.AI
  👥 **作者**：Mohammed Nayeem Khan, Akhil P, Shahina Shaik
  🏛️ **单位**：Intel Corporation
  📝 **摘要**：本文研究421M参数编码器Laya如何在单次前向传播中处理选项名称与描述冲突的问题。通过951个合成问题实验，发现模型存在“名称捷径”，即倾向于选择名称正确的选项。定位分析表明，阻断第14至17层中每个标记到其自身名称令牌的注意力，可将v1微调模型的捷径率从67%降至16%，同时保持原始名称准确率在90%。相比之下，阻断标记到问题、其他选项或文本的注意力无显著影响。在5个检查点（包括发布版、微调版、名称随机化版）上重复实验发现，名称随机化模型中阻断描述边可使捷径率回升至56-58%，表明读取机制持续存在但被投票否决。此外，标记状态从第0层即可解码名称，层间移植实验进一步验证了特定层对捷径形成的贡献。
  🔗 [PDF](https://arxiv.org/pdf/2611.31139v1)

- **连载与角色系统：衡量法国小说（1800–1940）中的叙事集中度**
  *Serialization and the Character-System: Measuring Narrative Concentration in French Fiction (1800–1940)*

  📄 `arXiv:2611.31133` · cs.CL
  👥 **作者**：Jean Barré, Antoine Bourgois, Thierry Poibeau
  🏛️ **单位**：Max Planck Institute for Empirical Aesthetics, Frankfurt am Main, Germany, LaTTiCe Laboratory, CNRS & ENS-PSL, Paris, France
  📝 **摘要**：本文将Woloch的“角色系统”概念操作化为角色网络PageRank分布的不等度（基尼系数），以衡量小说中叙事注意力的结构性集中度。基于Gallica语料库中1800至1940年间出版的12,011部法国小说，研究发现长期十九世纪中集中度呈U型轨迹：在1850-1860年代降至低谷，随后在世纪之交回升。这一变化虽小（相当于双主角与单主角小说的差异），但对角色截断、语料密度、演员规模及作者效应具有鲁棒性。侦探和冒险小说比同期平均小说集中度更低。在连载小说时代（1840-1914），以报纸连载为职业结构的作者比文学对照组更均匀地分配中心性。研究支持将连载小说解读为情节增殖形式而非超级英雄叙事的观点，并评估了提取管道在角色和身份层面的准确性。
  🔗 [PDF](https://arxiv.org/pdf/2611.31133v1)

- **注意力温度混淆零样本上下文扩展**
  *Attention Temperature Confounds Zero-Shot Context Extension*

  📄 `arXiv:2611.31113` · cs.LG, cs.AI, cs.CL
  👥 **作者**：Ruben Navasardyan
  🏛️ **单位**：Machine Learning and Optimization Laboratory, EPFL, Department of Applied Mathematics, University of Waterloo
  📝 **摘要**：本文指出，在默认温度τ=1下评估零样本上下文扩展时，基线模型在超出训练长度处的校准偏差会混淆结果。在标准FP32主权重配方下，8k训练的基线在30k长度处存在8-15%的校准偏差，这可能导致块稀疏训练模型看似提升7%的性能，但校准后该优势消失。在纯BF16训练（无主权重）中，校准偏差更大（37-58%），因为AdamW更新步长小于BF16精度间隔，导致归一化增益无法移动，使得块稀疏预训练、注意力Dropout和ALiBi看似有6-35%的优势。对每个模型和长度校准单一温度可消除这些虚假优势，使ALiBi落后RoPE 5%，并保留NTK感知缩放的部分增益。解冻增益可逆转365M模型的块稀疏优势，并在1.2B模型中消除71-89%的优势。作者建议在校准温度下报告扩展结果，并检查归一化增益是否移动。
  🔗 [PDF](https://arxiv.org/pdf/2611.31113v1)



---

## 📎 arXiv Computer Vision and Pattern Recognition · 2026-11-24

### 📄 论文列表

- **Lyris：基于布局引导与持久3D记忆的长视频生成**
  *Lyris: Layout-Guided Long Video Generation with Persistent 3D Memory*

  📄 `arXiv:2611.31239` · cs.CV
  👥 **作者**：Chen Wang, Jiahui Huang, Riccardo de Lutio, Alex Trevithick, Bryan Chu, Jiawei Ren, Laura Leal-Taixé, Shengyu Huang, Lingjie Liu, Haithem Turki
  🏛️ **单位**：NVIDIA, University of Pennsylvania
  📝 **摘要**：本文提出Lyris，一种解决长视频生成中相机漂移和场景不一致问题的框架。针对现有记忆方法缺乏锚点、布局方法依赖人工标注的局限，Lyris结合持久点云记忆与视觉语言模型生成的3D布局。其核心洞察是，每个对象仅需一个带标签的3D框即可作为视频模型的锚点，既简单可编辑又具备足够表达力。实验表明，从单张照片出发，Lyris能生成超过3分钟、50米长的相机控制漫游视频，并穿过门廊进入未展示的房间。在四个数据集的分钟级往返测试中，Lyris大幅超越最先进方法，相机误差降低3.8倍，返回时的一致性平均提升22%。
  🔗 [PDF](https://arxiv.org/pdf/2611.31239v1)

- **现代自监督视觉Transformer具有“空想性”**
  *Modern Self-Supervised Vision Transformers Are Pareidolic*

  📄 `arXiv:2611.31238` · cs.CV
  👥 **作者**：Zihang Lin, Huaiyuan Qin, Liangli Zhen, Qing Guo, Jun Liu, Yew-Soon Ong, Hongyuan Zhu
  🏛️ **单位**：Institute of Advanced Intelligence and Computing (IAIC), A*STAR, Singapore, Nanyang Technological University, Nankai University, Lancaster University
  📝 **摘要**：本文发现现代自监督视觉Transformer（ViTs）存在类似人类“空想性”（Pareidolia）的现象：在纯白噪声中，其特征的少数方向仍形成空间连贯模式。这种“空想子空间”在DINOv2和DINOv3中占据大部分特征方差，导致尽管密集特征更强，但在物体涌现能力上远落后于DINO。实验表明，缩小该子空间可恢复物体发现能力。据此，作者提出免训练校准方法PSC，仅在噪声输入上测量空想子空间并校准自然图像特征。PSC在物体发现、显著性检测和视频物体分割任务上分别将DINOv2/DINOv3的性能提升最高31.7 CorLoc、30.2 maxF和59.9 J。研究还追溯发现，空想性源于中间层，且仅在使用patch级损失训练时持续至最后层。
  🔗 [PDF](https://arxiv.org/pdf/2611.31238v1)

- **LeJEPA特征并非各向同性，且不应是**
  *LeJEPA Features Are Not Isotropic, and Should Not Be*

  📄 `arXiv:2611.31216` · cs.CV, cs.LG
  👥 **作者**：Richeek Das, Pratik Chaudhari
  🏛️ **单位**：GRASP Laboratory, University of Pennsylvania
  📝 **摘要**：本文指出LeJEPA中的SIGReg正则项旨在使特征呈各向同性高斯分布，但实践中无法达成。首先，作者设计改进的正则项以更好地实现目标，在ImageNet-100上以1.3倍更少的epoch达到SIGReg的最终精度。其次，论证自监督编码器不应具有各向同性高斯特征，因为LeJEPA的对齐项耦合了特征幅值与方向，与各向同性高斯要求的独立性相冲突。最后，提出PolarReg，仅约束幅值和方向的边缘分布而不强制独立性。PolarReg无需调整超参数即可在不同数据集、批大小和嵌入维度上可靠优化。在ImageNet-1k上，PolarReg以4.7倍更少的epoch匹配LeJEPA及其变体的精度，并将最终精度提升1.8个百分点。
  🔗 [PDF](https://arxiv.org/pdf/2611.31216v1)

- **WorldLatent：用于世界感知与生成的统一4D潜在空间**
  *WorldLatent: A Unified 4D Latent Space for World Perception and Generation*

  📄 `arXiv:2611.31209` · cs.CV
  👥 **作者**：Jingxi Chen, Yujia Chen, Cornelia Fermuller, Yiannis Aloimonos, Wen-Sheng Chu, Du Tran
  🏛️ **单位**：University of Maryland, College Park, Google
  📝 **摘要**：针对4D时空视觉缺乏统一表示协议的问题，本文提出WorldLatent框架，将世界感知与生成统一在共享的4D潜在空间中。不同于依赖碎片化任务模型或未对齐的单模态堆叠，WorldLatent采用多模态VAE架构，将复杂的4D视觉外观、几何和动态压缩融合为单一结构化潜在表示。在该框架中，感知和生成作为同一潜在空间上的互补去噪过程，使单个生成模型能在单一训练循环中同时学习两种能力。实验在代表性4D基准上验证，WorldLatent实现了专家级的零样本4D感知、连贯的4D生成以及可控编辑。该工作证明了多样化4D任务可在共享表示协议下无缝统一，为通用4D空间智能提供了可扩展基础。
  🔗 [PDF](https://arxiv.org/pdf/2611.31209v1)

- **用于高效全能视频生成的在线策略编解码蒸馏**
  *On-Policy Codec Distillation for Efficient All-in-One Video Generation*

  📄 `arXiv:2611.31184` · cs.CV
  👥 **作者**：Boyang Wang, Kevin Blackburn-Matzen, Oindrila Saha, Matheus Gadelha, Zezhou Cheng
  🏛️ **单位**：Adobe Research, University of Virginia
  📝 **摘要**：现代视觉生成模型中，条件输入（如身份、草图、深度图）的token化导致计算成本高昂，且包含大量冗余时空信息。本文提出CodecOPSD，利用经典视频编解码器识别“真正新信息”的能力，引入基于编解码器的token剪枝方法丢弃冗余token。随后，提出在线策略自蒸馏（OPSD）策略训练DiT适配器，使其在不降低质量的情况下学习编解码剪枝模式。在自有视频扩散模型上，CodecOPSD扩展至16种条件模态，平均剪枝66%的条件token且几乎无质量损失，使去噪速度提升2倍，KV缓存模式下内存缩减高达73%。该方法还可扩展至其他最先进预训练图像和视频生成模型，在更多条件、更长帧数和更高分辨率下收益进一步增加。
  🔗 [PDF](https://arxiv.org/pdf/2611.31184v1)



---
