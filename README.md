# ⚡ Startup Signals

**自动化创业机会信号发现引擎** — 每日/每周扫描全球开发者社区与中文科技圈，用 AI 从海量噪音中提炼真实的市场空白信号。

🌐 **在线报告：** https://0xHerbertChan.github.io/startup-signals/

---

## 它在做什么

每次运行扫描约 500 条原始内容，经两阶段过滤后输出 5-8 个评分信号：

```
560 条原始数据
  → 规则预过滤（分数阈值 + 关键词）→ ~60 条候选   节省 89% token
  → LLM 精分析（Claude）          → 5-8 个信号
  → 六维评分 + HTML 报告 + GitHub Pages 自动发布
```

**数据源：**

| 英文圈 | 中文圈 |
|--------|--------|
| Reddit（19个版块） | 掘金 |
| Hacker News | V2EX |
| Lobsters | 少数派 |
| Product Hunt | 36Kr |
| Dev.to | — |
| GitHub Trending | — |

---

## 六维评分体系

每个信号在 6 个维度上评 1-5 分：

| 维度 | 含义 | 5分代表 |
|------|------|---------|
| **痛点** | 用户痛苦有多真实 | 强情绪用词 + 1000+ 赞 + 明确付费意愿 |
| **空白** | 现有方案有多差 | 完全没有解决方案，靠 Excel 凑合 |
| **付费** | 用户愿意掏钱吗 | 帖子里直接说了"I'd pay $X for this" |
| **获客** | 能低成本触达客户吗 | 信号来源社区就是目标客户 |
| **监管** | 进入市场有多难 | 纯软件工具，无行业监管 |
| **机会** | 综合加权结论 | EXTREME — 现在就应该做 |

---

## 报告归档

| 日期 | 范围 | 新信号 | 查看 |
|------|------|--------|------|
| 2026-05-21 | 今日 | 3 | [报告](https://0xHerbertChan.github.io/startup-signals/reports/signal-report-2026-05-21-d2.html) |
| 2026-05-21 | 今日 | 4 | [报告](https://0xHerbertChan.github.io/startup-signals/reports/signal-report-2026-05-21-d.html) |
| 2026-05-21 | 本周 | 6 | [报告](https://0xHerbertChan.github.io/startup-signals/reports/signal-report-2026-05-21-week.html) |
| 2026-05-20 | 3日 | 5 | [报告](https://0xHerbertChan.github.io/startup-signals/reports/signal-report-2026-05-20-3d.html) |

---

## 信号追踪记忆

系统维护 `seen.json`，记录所有历史信号的关键词指纹。重复出现的信号会被标记 🔁 并追踪出现频次——**重复出现的信号往往比首次出现更值得关注**，说明市场在持续强化同一个问题。

当前已追踪：**26 个信号**

---

## 运行方式

本项目通过 Claude Code 自定义命令驱动，支持三种时间范围：

```
/创业信号        # 本周扫描（默认，每周一次）
/创业信号 3d     # 近3天扫描
/创业信号 d      # 今日快扫
```

运行后自动发布到此 GitHub Pages。

---

*Powered by Claude Code · 数据来源均为公开社区内容*
