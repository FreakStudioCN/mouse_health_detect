# 美国/英文豚鼠社区初步采样报告（层 1 执行结果）

**采样时间**：2026-05-01
**方法**：reddit-mcp-buddy MCP（已装，待重启生效）+ Reddit JSON 端点直采 + Jina 抓 The Guinea Pig Forum + Chewy 直接 + Jina 兜底（均失败）
**字面采样规模**：r/guineapigs 25 月度热帖 + 3 组关键词搜索（45 条结果）+ Guinea Pig Forum 首页结构

---

## 渠道活性快照

| 渠道 | 状态 | 规模 | 抓取结果 |
|---|---|---|---|
| **r/guineapigs** | ✅ 245,134 订阅 | JSON 端点工作 | 拿到 70+ 帖子标题/分数/评论数/flair |
| **The Guinea Pig Forum (.co.uk)** | ✅ 44,968 用户 / 299 万消息 / 205,872 主题，2 分钟前还有人发帖 | 通过 Jina 抓 | 拿到全部分区结构 + 健康类标题 |
| **Chewy 评论区** | ⚠️ 直接 + Jina 双双 429 | — | 阻塞，需 CDP（用户真实 Chrome）兜底，下次执行 |
| **reddit-mcp-buddy** | ✅ 已装入 `.claude.json` | — | 重启 Claude Code 后可用 |

---

## 关键发现 1：豚宝保的核心识别能力（脚垫卡脚 / 呼吸道）= 真实痛点

### 「bumblefoot」（脚垫卡脚 / pododermatitis）—— 强信号

r/guineapigs 过去一年 top 12 条命中里有 9 条直接是健康问题：

| 分数 | 评论 | flair | 标题 |
|---|---|---|---|
| 503 | 33 | Help & Advice | **Sudden death of my guinea pig Eggs** |
| 236 | 33 | Health & Diet | how do her feetsie's look? |
| 136 | 20 | Help & Advice | Tumor on Toe |
| 93 | 25 | Health & Diet | Caring for my boy's feet |
| 93 | 6 | Help & Advice | **Bumblefoot?** |
| 47 | 6 | Health & Diet | **I'm at a loss with bumblefoot.** |
| 39 | 6 | Health & Diet | **Is this early bumblefoot?** |
| 21 | 9 | Help & Advice | Falling over Periodically… Causes?? |

**关键观察**：标题原话「I'm at a loss with bumblefoot」「Is this early bumblefoot?」——用户**主动求识别帮助**。豚宝保「视觉自动识别脚垫卡脚」直接命中这个询问语场，PMF 假设第一条✅。Guinea Pig Forum 也有专门的 "Health & Illness Support Corner" 和 "Grooming Care & Health Monitoring" 子版。

### 「URI / respiratory」—— 强情绪信号但姿态不同

15 条命中里 **6 条带 🌈 Rainbow Bridge flair**（社区悼念已逝豚鼠的固定仪式），原文如：
- "Woke up to Timmy having passed away"
- "my star passed in the night 🌈⭐️"
- "Willows gone"
- "pumpkin 2020-2026 🕊️"
- "Michael has passed away"

另一条 **756 分 / 84 评论**：「**New Guinea Pig Owner, What Are These Noises!**」——新手对呼吸道异常声音听不出来，跑来问。

**关键观察**：豚鼠 URI 致死率高且急（往往一夜过世），呼吸道问题晚发现 = 后悔。豚宝保「听觉异常呼吸声识别」对应的不是「主动诊断」需求，而是「夜间无人时帮我听到异常」的**焦虑代偿**需求。营销叙事应靠近 Rainbow Bridge 类内容的情感重量，而不是科技参数。

---

## 关键发现 2：「pet camera / monitor」当前不是健康类语言

「camera / monitor / webcam」搜索 15 条命中**全部不是健康监测**：
- 都是萌宠图、社区玩笑（"Don't worry, Kiki is monitoring the situation 🔍"）、新摄像头晒图
- 没有任何一条把「camera」和「pet health」联系起来

**关键观察**：英文豚鼠社区目前**没有「健康监测摄像头」的心智锚点**。这是双刃剑：
- ✅ 蓝海，可以定义品类
- ❌ 不能当成已有需求去 SEO，要做「教育式叙事」（show case→建立认知→交易）

**进入策略含义**：早期不要叫 "guinea pig camera"，叫 "**guinea pig health monitor**" 或更具体的 "**bumblefoot watcher**" / "**guinea pig nightly health report**"——直接挂上他们已经在用的疼痛词。

---

## 关键发现 3：The Guinea Pig Forum 的结构 = 产品功能映射图

它的子版分布几乎是豚宝保 features 的功能分类：

| Forum 子版 | 豚宝保对应能力 |
|---|---|
| Health & Illness Support Corner | 疾病早期预警 |
| Grooming Care & Health Monitoring | 每日健康报告 |
| Behaviour, Bonds and Species Understanding | 运动量统计、行为分析 |
| Diet | 饮水/进食频率 |
| Housing, Enrichment, Travel and Climate | 远程关怀（外出场景） |
| End of Life and Bereavement Support / Rainbow Bridge | 「早发现早干预」叙事的情感终点 |

**含义**：The Guinea Pig Forum 应该是早期种子用户**第一渠道**——用户已经按豚宝保的产品维度自己做了分类，告诉他们哪个子版对应哪个 feature 即可。2 分钟前还有人发帖说明活跃度足以走「免费内测招募」。

---

## 阻塞与遗留

1. **Chewy 评论区**：直连 + Jina 都 429。下一轮要走 web-access CDP（启动 CDP Proxy + 用户真实 Chrome）才能拿。预计能补充：哪些笼子缺陷、食盆设计槽点、健康用品差评——产品设计输入的金矿。
2. **reddit-mcp-buddy 重启生效**：MCP server 已写入 `C:\Users\Haipeng Wu\.claude.json`，本会话用不上，重启 Claude Code 后下次可直接让 Claude 调 MCP 工具搜 r/guineapigs，效率比 curl JSON 高。
3. **Help & Advice flair 搜索语法**：`flair:"Help & Advice"` 和 `flair_name:"Help & Advice"` 都返回 0 命中，要换 URL 编码或 MCP 重启后用工具内置的 flair filter。
4. **未抓**：Discord disboard、HappyCavy 博客、guineapigcages.com（要 CDP 绕 Cloudflare）—— 层 1 必要项已覆盖，这些放层 2/3。

---

## 立刻可做的下一步动作（按性价比）

1. **重启 Claude Code** → 验证 reddit-mcp-buddy 加载成功，下次调研直接走 MCP
2. **下次开 CDP 抓 Chewy 评论**（豚鼠类目 Top 5 销量产品的 1 / 2 / 3 星评论 = 产品设计输入）
3. **去 The Guinea Pig Forum 的 "Health & Illness Support Corner" 抓最近 2 周帖子**（Jina 友好，可量化 frequency-weighted 痛点列表）
4. **整理「英文豚鼠用户痛点词典」**：bumblefoot、URI、scurvy、bladder stones、impaction、weight loss、bonded pair、URI noise、stargazing 等——为产品文案、SEO、社区话题切入做语言锚

---

## 产品决策含义（写给后续看产品/出海材料的同事）

| 假设 | 验证状态 | 证据 |
|---|---|---|
| 美国/英文豚鼠主人会主动搜「bumblefoot」并自承「I'm at a loss」 | ✅ | 15 条月度搜索结果全命中，多条带 Help & Advice / Health & Diet flair |
| 主人对「夜间猝死/呼吸道问题晚发现」有强情绪焦虑 | ✅ | 6/15 条 URI 搜索结果带 Rainbow Bridge flair，社区有专门悼念仪式 |
| 「pet camera」已在用户语言中代表健康监测 | ❌ | 全部命中是萌宠图，没有任何一条联想到健康——需要重新教育市场 |
| 有现成英文垂直社区可做内测招募 | ✅ | The Guinea Pig Forum 4.5w 用户 + r/guineapigs 24.5w 订阅，活跃度都足够 |
| 可走「老式垂直论坛 + Reddit + 商品评论」三角抓痛点而不必死磕 X / FB | ✅ | 三个渠道都已验证可访问，X / FB 信息密度低且接入贵，按计划放弃 |

**产品策略可执行结论**：
- 海外页面/落地页主语应是 "**guinea pig health monitor**"（健康+监测），不是 "guinea pig camera"
- 早期 hero 用例：bumblefoot 自动识别 + 夜间呼吸道异常监听，明显比 "运动量统计" 更能击中已有疼痛
- 内测招募首选 The Guinea Pig Forum 健康相关子版 + r/guineapigs Help & Advice flair 热帖回复
