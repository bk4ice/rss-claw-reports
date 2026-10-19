# 岛屿周报 · 10月12日 - 10月18日

## 本周概览

本周共收录 300 篇文章，来自 30 个信息源，其中 300 篇具有较高关注度。主要关注领域：clustered。

---

## 本周核心


### 1. Ledger确认加密钱包中隐藏芯片，涉9200万美元盗窃指控

Ledger确认其Nano系列硬件钱包在经销环节被植入隐藏芯片，涉及约9200万美元盗窃。攻击者通过监听CPU与显示屏间未加密的SPI总线数据，在助记词显示时窃取密钥并经LTE网络外传，绕过Secure Element保护。由于原始安全芯片未被替换，设备仍可通过Genuine Check验证，暴露了供应链物理完整性漏洞。讨论聚焦于防拆设计不足、多签方案及Crypto信任转移问题，强调显示链路成为安...

**来源**：[极客洞察](https://newshacker.me/story?id=50054092)


### 2. 通用漏洞披露编号 2025-32433 漏洞复现分析报告：爱立言开放电信平台安全外壳协议服务器预认证远程代码执行

FreeBuf 发布 CVE-2025-32433 复现分析：Erlang/OTP 内置 SSH 库在密钥交换与认证完成前处理 exec 通道请求，攻击者仅需 3 个明文报文即可无凭据远程代码执行。漏洞 CVSS 10.0，已列入 CISA KEV，影响 OTP 27.3.2 等版本，修复版本包括 OTP-27.3.3、OTP-26.2.5.11、OTP-25.3.2.20；因 Erlang SS...

**来源**：[FreeBuf](https://www.freebuf.com/articles/vuls/505881.html)


### 3. Muse Wonder

Meta发布Muse Wonder系列模型，包括Muse Wonder和Muse Wonder Full，旨在提供个人和专业代理任务的前沿性能。该系列整合了Active Memory和Active Focus技术，以增强上下文记忆和持续任务执行能力。模型在Meta Model API和Muse Code中可用，标志着Meta在构建个人超级智能道路上的重要里程碑，并在编码、领域专业知识及泛化能力上达...

**来源**：[Hacker News 首页](https://research.meta.ai/blog/muse-wonder)


### 4. 我发现 Google 的一个价值 9 万美元的远程代码执行漏洞

研究者发现 Google 开发者文档站点共享 OAuth 流程中，Flask session cookie 使用 pickle 序列化，且 OAuth client secret 同时用于签名，攻击者可伪造 cookie 触发 pickle.loads 实现未认证远程代码执行。漏洞影响 developers.google.com、firebase.google.com 等多个站点。报告获 Goog...

**来源**：[Hacker News 首页](https://simonkoeck.com/writeups/google-devsite-flask-session-pickle-rce)


### 5. 消息称 DeepSeek 将完成 1000 亿元融资，投前估值仍为约 5000 亿元

据《财经》报道，大模型公司DeepSeek第二轮融资临近完成，金额从500亿元增至约1000亿元，投前估值维持约5000亿元。新进投资方包括石溪资本、中芯聚源、吉利等产业资本，老股东宁德时代拟增资100亿元。创始人梁文锋倾向于引入产业链赋能型投资方。同时，DeepSeek正筹备科创板IPO，已聘请中信证券，计划最快2026年末递表，目标2027年挂牌。

**来源**：[IT之家](https://www.ithome.com/1/012/172.htm)


### 6. CVE-2026-97229：GitLab CI/CD正则表达式编译器整数溢出漏洞——分析与缓解

GitLab发布紧急补丁修复CVE-2026-97229，这是一个CVSS 10.0的严重漏洞，存在于CI/CD正则表达式编译器中。攻击者可通过特制正则表达式触发整数溢出，实现无需认证的远程代码执行。这是GitLab一个月内第三个正则引擎漏洞，影响19.2.x至19.4.x的自托管版本。GitLab敦促立即升级，因为该漏洞可导致服务器被完全控制，进而威胁供应链安全。

**来源**：[Dev.to](https://dev.to/iamfaizanakhtar/cve-2026-97229-gitlab-cicd-regex-compiler-integer-overflow-vulnerability-analysis-mitigation-4fpc)


### 7. 攻击者劫持丹佛斯控制器，法国超市冷柜被加热至50℃

攻击者远程入侵法国数百家超市的丹佛斯（Danfoss）制冷控制器，将冷柜温度升至50℃，导致大量食品报废，预计损失数千万欧元。受影响设备主要为已停止更新的老旧型号AK-SM 800和AK-SC 355，以及部分运行过时固件的AK-SM 800A。法国CERT-FR要求立即断开控制器网络连接或严格过滤访问权限。调查已启动，ANSSI发现软件漏洞，西班牙、德国等多国也疑似受波及。

**来源**：[FreeBuf](https://www.freebuf.com/news/506197.html)


### 8. Rust借用检查器中发现存在11年的内存安全漏洞

Rust语言借用检查器发现存在11年的严重内存安全漏洞（Issue #164250）。该漏洞允许通过协变字段赋值绕过结构体的生命周期要求，导致在Drop实现中访问已释放的内存，引发栈使用越界。此问题自Rust 1.18.0版本起存在，被标记为P-critical级别。Rust团队强调类型系统安全性的重要性，并正在通过Project Zero等项目修复此类底层缺陷。

**来源**：[Hacker News 首页](https://github.com/rust-lang/rust/issues/164250)



---

## 趋势观察

本周信息集中在 clustered 等领域。从更长的时间维度看，这些方向正在持续演进，建议关注其后续发展与跨领域融合趋势。

---

*本报告由 RSS-Claw 岛屿周报 AI 自动生成*