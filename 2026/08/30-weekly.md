# 岛屿周报 · 08月24日 - 08月30日

## 本周概览

本周共收录 295 篇文章，来自 53 个信息源，其中 295 篇具有较高关注度。主要关注领域：tech、clustered。

---

## 本周核心


### 1. SpaceX 将在路易斯安那州建设第二个价值 1000 亿美元的“Starbase”航天港

SpaceX宣布将在路易斯安那州前Exxon地块建设第二个价值1000亿美元的“Starbase”发射场，旨在支持Starship火箭的发射。公司计划2027年开始施工，最早2029年实现首次发射，而路易斯安那州经济发展局预计2030年投入运营。该项目预计创造3000个直接就业岗位和3万多个建筑岗位。此举标志着SpaceX在Starship可重复使用技术尚未完全成熟前，已全力押注该火箭以支撑Sta...

**来源**：[TechCrunch](https://techcrunch.com/2026/08/25/spacex-will-build-a-second-100b-starbase-spaceport-in-louisiana/)


### 2. Dolly Parton 去世：Jolene、Imagination Library 与全民哀悼

美国乡村音乐传奇人物 Dolly Parton 去世，引发全球大规模悼念。文章回顾了她从田纳西州贫困山区崛起为超级明星的历程，重点提及她的代表作《Jolene》、《9 to 5》及公益项目 Imagination Library（儿童免费赠书计划）和 Dollywood 主题公园。评论界高度赞扬其音乐才华、商业成就及慈善贡献，称其为“国宝级”人物，强调其财富回馈社区及长期低调行善的形象。

**来源**：[极客洞察](https://newshacker.me/story?id=49438052)


### 3. Jalapeño 首批结果显示其在 AI 推理方面具有行业领先的速度和效率

OpenAI 发布其首款定制推理芯片 Jalapeño 的初步结果。该芯片旨在提供行业领先的 AI 推理速度和效率，具备更高的吞吐量和更低的延迟，同时显著提升了现代 AI 模型的能源效率。

**来源**：[OpenAI 博客](https://openai.com/index/jalapeno-first-results)


### 4. Oracle WebLogic 漏洞正被积极利用，允许未认证攻击者访问关键数据

美国CISA将Oracle HTTP Server和WebLogic Server中的最高严重性漏洞CVE-2026-21962（CVSS 10.0）加入已知被利用漏洞目录。该漏洞允许未认证的攻击者通过网络访问获取关键数据，且已有活跃利用证据。

**来源**：[The Hacker News](https://thehackernews.com/2026/08/actively-exploited-oracle-weblogic-flaw.html)


### 5. 关键 Keycloak 密码重置漏洞可能让未认证攻击者接管任何账户

Red Hat 和 Keycloak 项目已发布补丁，修复了开源身份和访问管理服务器中的严重安全漏洞（CVE-2026-18963）。该漏洞允许未认证的远程攻击者通过强制密码重置接管任何用户账户。Red Hat 将其 CVSS 评分定为 9.1，属于高危风险。

**来源**：[The Hacker News](https://thehackernews.com/2026/08/critical-keycloak-password-reset-flaw.html)


### 6. DeepSeek 充当大脑 Hermes 充当手脚，Unit 42 复盘的无人攻击

Unit 42 发布报告披露一起由单一中文威胁行为人利用 AI 模型实施的自主网络攻击。攻击者将 DeepSeek 作为推理大脑，结合开源框架 Hermes Agent 和 Telegram 作为控制界面，在开启 Yolo 模式（无需人工确认）的情况下，自主完成了漏洞侦察、PoC 获取、资产测绘及利用尝试。该攻击栈针对 460 多个目标，涉及 8 个 CVE，展示了 AI 在降低攻击人力成本、提升...

**来源**：[FreeBuf](https://www.freebuf.com/articles/vuls/497119.html)


### 7. CVE-2026-50522：一条不带凭据的 POST 请求攻击 SharePoint，顺手窃取了整台服务器的密钥

Microsoft SharePoint 本地部署曝出高危未认证反序列化 RCE 漏洞（CVE-2026-50522），CVSS 评分 9.8。攻击者无需凭据，通过向 /_trust/default.aspx 发送包含恶意 BinaryFormatter payload 的 POST 请求即可执行任意命令。该漏洞源于 WIF 组件中 SessionSecurityTokenHandler 的不安全...

**来源**：[FreeBuf](https://www.freebuf.com/articles/vuls/497107.html)


### 8. CVE-2026-63077：TeamCity 为 XStream 添加了白名单，但默认权限未移除导致防护失效

JetBrains TeamCity 存在高危未认证远程代码执行漏洞（CVE-2026-63077，CVSS 9.8），已被 CISA 列入 KEV 名录。根本原因在于 XStream 反序列化白名单配置错误：开发者仅通过 allowTypes 添加协议类，但未移除 XStream 默认存在的宽泛类型层级许可（如 Map、Throwable 等），导致白名单失效。攻击者可利用 /app/agent...

**来源**：[FreeBuf](https://www.freebuf.com/articles/vuls/496957.html)



---

## 趋势观察

本周信息集中在 tech、clustered 等领域。从更长的时间维度看，这些方向正在持续演进，建议关注其后续发展与跨领域融合趋势。

---

*本报告由 RSS-Claw 岛屿周报 AI 自动生成*