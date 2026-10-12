<p align="center">
  <img alt="mu-multi-agent" src="assets/default-banner.png" width="100%">
</p>

# 🐝 mu-multi-agent · 多Agent协作指挥官

> 10 份简历要初筛、三个方向要调研、报告下班前就要交？它把你手上那个 AI Agent 变成一支分工明确的小队：并行调研、分头产出、独立评审——而且第一步先告诉你，哪些任务根本不用组队。

[English](README.md) | **中文** | [🌐 在线主页](https://muippt.github.io/mu-multi-agent/)

[![微信公众号](https://img.shields.io/badge/muippt-07C160?logo=wechat&logoColor=white)](https://mp.weixin.qq.com/s/YLtXENt_7WzO2DgJCFUtPA)
[![小红书](https://img.shields.io/badge/muippt-FF2442?logo=xiaohongshu&logoColor=white)](https://xhslink.com/m/ESxtgUNMdl)
[![书籍](https://img.shields.io/badge/书籍-图解团队管理-BBDDE5?logo=bookstack&logoColor=white)](https://item.m.jd.com/product/14547345.html)
[![mu-skill集合](https://img.shields.io/badge/mu--skill集合-9E95B7?logo=refinedgithub&logoColor=white)](https://muippt.github.io/mu-skill-hub/)
[![License](https://img.shields.io/github/license/muippt/mu-multi-agent)](LICENSE)
[![Version](https://img.shields.io/github/v/release/muippt/mu-multi-agent)](https://github.com/muippt/mu-multi-agent/releases)
[![Stars](https://img.shields.io/github/stars/muippt/mu-multi-agent)](https://github.com/muippt/mu-multi-agent/stargazers)

---

### 💡 使用场景示例

- 🔍 **多方向并行调研，回来一份报告** — 三个调研员同时出发，主 Agent 负责合流；你拿到的是一份汇总好的报告，不是三个互相矛盾的版本。
- 🧮 **批量简历初筛** — 多个评估员并行打分，最后交到你手上的是一张排序清晰的对比表，不是十份各自为政的小作文。
- 🏁 **多维度竞对分析** — 价格、功能、口碑各派一名调研员，主 Agent 拉通成一份完整分析。
- ✍️ **多版本文案** — 三种风格同时开写，附一份"建议用哪版"的对比结论。
- 🌐 **批量文档处理** — 一摞文档并行翻译或总结，主 Agent 逐份验收结果。
- 📝 **重要报告流水线** — 先调研、再出初稿、最后独立评审打分，通过之后才轮到你过目。
- 🧐 **发出前的第二双眼睛** — 同一个模型、全新上下文、五维评分表，职责就是挑错，不是夸奖。

---

### ✨ 核心亮点

#### 🚦 先告诉你什么时候"不用组队"

多数多 Agent 翻车，都从"Agent 越多越好"这个念头开始。任务进来先过一张前置判断清单：它真的能拆成互相独立的子任务吗？还是一个 Agent、甚至一个专项 Skill 干得更利索？简单顺序任务会被礼貌地劝退。省下的是 token、等待时间，以及几个 Agent 互相转述打圈圈的那种特殊混乱。

#### 🧭 你只说任务，队形它来定

没有模式菜单，也没有连线图。带调研味的活自动走指挥官队形（真正并行、带工具）；多角度分析、批量翻译这类纯文本任务走快速流水线；"先调研，再给我三个版本"则自动变成两阶段的混合模式。你继续谈结果，排兵布阵交给它。

#### 📜 三条铁律，守着队伍最容易散的地方

第一，可拆分性必须先判断——单一顺序任务绝不强行并行。第二，派活保持极简："谁 + 做什么"，一个字都不多附。第三，主 Agent 亲自汇总验证结果——子 Agent 的原始输出永远不会被直接粘贴给你。围绕这三条，还有一张九条常见坑的对照表（沉默开局、token 爆炸、假忙转述、意大利面连线……每条都写明错的做法和对的改法），以及严格的拓扑原则：只允许线性和扇出，"以防万一"的连接一律删掉。

#### 🔎 写的人，永远不给自己打分

刚写完报告的 Agent，往往会相当喜欢自己的报告。这个 Skill 把执行和评审切开：一个全新上下文的评审 Agent，按五维评分表（事实、结构、逻辑、证据、格式）逐项打分，结果只有两种——通过，或一份具体的修改清单。同一个模型，判断明显更靠谱，因为打分的人不在写作现场。

#### 📊 每次跑完，交一张"战报"

每一轮结束都有标准统计卡：哪些 Agent 上场了、什么角色、耗时多少、状态如何、并行比串行省了多少时间、主对话的上下文被隔离掉多少。团队到底值不值，一眼看得出。而且统计卡没输出、结果没合流、评审没通过之前，任务不算完成。

#### 🪂 环境不支持子 Agent？也能稳稳落地

如果你的 Agent 运行时压根派不出子 Agent，主 Agent 会依次扮演每个角色：流水线模式完整可用，评审分离改用"隔一段上下文再审"来保住独立性。说实话，比真并行慢——但不装快。不用装框架、不用 Python、零依赖，它是一套能贴着你现有 Agent 用起来的方法论。

---

### 📌 与同类工具对比

| 维度 | 🧭 mu-multi-agent | 直接在对话框里手动指挥 | 代码型多 Agent 框架 |
|---|---|---|---|
| 安装成本 | 放进去就能用，零依赖 | 无 | 装框架、写编排代码 |
| 何时该用多 Agent | 内置清单自动判断 | 每次自己猜 | 自己写死在代码里 |
| 执行与评审分离 | 独立评审 Agent + 五维评分表 | 同一个上下文给自己打分 | 自己接线 |
| 最终汇总纪律 | 主 Agent 必须亲自验证合流 | 自己复制粘贴做调和 | 自己接线 |
| 成本可见性 | 每次跑完一张统计卡 | 无 | 框架仪表盘 |
| 不写代码也能用 | ✅ | ✅ | ❌ |
| 运行环境 | 任何支持 Skill / SKILL.md 约定的 Agent | 任意聊天窗口 | Python 环境 |

---

### 🚀 核心工作流

| 工作流 | 什么时候上场 | 触发示例 |
|---|---|---|
| 🎯 指挥官模式 | 多方向/多信息源调研，需要联网和工具，真并行 | "同时调研 A、B、C 三个方向" |
| 🔄 流水线模式 | 纯文本任务：多角度分析、多风格写作、批量翻译 | "用三个角度分析这个问题" |
| 🔀 混合模式 | 先调研，再多版本输出 | "调研完给我三版不同风格的文案" |

你不必特意说"组队"。任务自然拆成两个以上独立子任务、需要同时查多个信息源、同类任务成批出现、或产出高风险内容时，它会自己醒来。专项 Skill 或简单顺序就能搞定的任务，它保持安静——这是设计如此。

**背景怎么传给子 Agent**

子 Agent 是全新会话，不自带上下文，所以背景注入有三种受控方式：

- **背景注入**（默认）：任务前附一行"[背景] 谁在做什么、给谁看"。
- **前序结果传递**：串行环节中，上一个 Agent 的发现以结构化要点传给下一个。
- **读文件**：背景较重时，让子 Agent 读一个背景文件，而不是贴一屏文字。

**拓扑原则——拒绝意大利面**

工作流只允许线性（A → B → C）或扇出（A → [B, C, D] → E）。加任何连接前先问三句：B 真的需要 A 的产出吗？没有它 B 能独立干活吗？这条连接是不是"以防万一"加的？是，就删。

---

### ⚙️ 技术规格

| 项目 | 说明 |
|---|---|
| 类型 | 方法论 Skill（单一 SKILL.md，纯提示词，无脚本） |
| 版本 | 2.2.0 |
| 依赖 | 零依赖——无脚本、无安装包、无需 API Key |
| 兼容性 | Compatible with Claude Code, Claude Desktop, OpenClaw, and any agent supporting the Skill / SKILL.md convention |
| 能力契约 | 4 个抽象契约：`spawn` · `monitor` · `history` · `notify`（按能力签名对号入座，不绑工具名） |
| 降级路径 | 运行时无子 Agent 能力时，主 Agent 串行扮演各角色；流水线模式与评审分离完整保留 |
| Skill 语言 | 中文（提示词可用你自己的语言） |
| 文件结构 | `SKILL.md` + `assets/` |
| 遥测 | 无 |
| 许可证 | MIT |

---

### 🛠️ 快速开始

**① 安装**

```bash
git clone https://github.com/muippt/mu-multi-agent.git ~/.claude/skills/mu-multi-agent
```

> 其他 Agent 可改用其约定的 Skill 目录，或项目级 `.claude/skills/mu-multi-agent`。

**② 验证**

重启或重新加载你的 Agent 后，直接问：

```text
列出我当前可用的 Skills
```

**③ 使用**

```text
这 10 份简历帮我并行初筛，最后给一张对比表。
```

也可以直接进入指定工作流：

```text
同时调研竞品的价格、功能和口碑，回来汇总成一份报告。
```

```text
先调研行业背景，再给我三版不同风格的宣传文案。
```

```text
把这份对外报告走一遍独立评审，按五维评分表打完分再给我。
```

---

### 🔒 安全与隐私

- 完全在你本地的 Agent 里运行——无服务器、无账号、无需注册。
- 零依赖、零脚本、零遥测、零数据收集。
- 你的文件和提示词只留在你信任的那个 Agent 里，不上传到任何地方。
- 它是一份方法论文档，不是一项服务——没有后台可回传，因为它压根没有后台。

---

### ⭐ Star 趋势

如果它帮你省下过一个傍晚的来回切换和复制粘贴调和，点一颗 star，让下一个人也能找到它。

[![Star History Chart](assets/star-history.png)](https://www.star-history.com/?repos=muippt%2Fmu-multi-agent&type=date)

> 一个 Agent 是一双手；一支简报清楚、还知道何时不必出动的队伍，是一个部门。

---

### 👤 作者简介

🎓 清华大学出版社签约作家 / 2026当当影响力作家 / 某互联网大厂 AI 大模型业务 HR 砖家 / 一级人力资源管理师 / 二级心理咨询师 / 野生设计师

📚 著有[《图解团队管理》](https://item.m.jd.com/product/14547345.html)，服务客户有字节跳动、腾讯、百度、中国移动、SMG、BOE…

💡 微信公众号[木先生iPPT](https://mp.weixin.qq.com/s/YLtXENt_7WzO2DgJCFUtPA) / [小红书](https://xhslink.com/m/ESxtgUNMdl)：muippt

---

### 📄 许可证与致谢

[MIT](LICENSE) © 2026 木先生iPPT

感谢 Skill / SKILL.md 开放约定背后的 Agent 开源社区，以及所有公开分享过多 Agent 编排经验的同行——这里的铁律，蒸馏自大量可公开共鸣的失败。

> 声明：本项目大部分内容由 AI 辅助完成。如您认为您的作品被使用但未获得适当署名，请提交 issue。
