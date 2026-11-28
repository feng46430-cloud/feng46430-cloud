# 徐峰（Feng Xu）

平时在做 AI 交互玩法原型、评测（Eval）体系和游戏质量工程（2020 至今，上海）。

[![Portfolio CI](https://github.com/feng46430-cloud/ai-engineering-portfolio/actions/workflows/verify.yml/badge.svg)](https://github.com/feng46430-cloud/ai-engineering-portfolio/actions/workflows/verify.yml)
[![Starlight CI](https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint/actions/workflows/verify.yml/badge.svg)](https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint/actions/workflows/verify.yml)

<img src="https://raw.githubusercontent.com/feng46430-cloud/starlight-market-ai-npc-blueprint/main/media/01_blind_start_theater.png" alt="星海交易局 Unity 6 URP 3D AI-NPC 原型" width="100%" />

这里主要放三块公开的工作记录——遇到什么问题、当时试了什么思路、跑出来是什么结果，按主题分好了入口，挑感兴趣的地方看就行：

- **[`ai-engineering-portfolio`](https://github.com/feng46430-cloud/ai-engineering-portfolio)** — **综合工程笔记与仿真脚本**  
  按主题收录了 5 块记录：AI 评测口径校准与记忆指标拆分、5,000 盒抽卡保底概率与防摸包仿真、4 段端到端延迟拆解与底层排障、废弃连线画布的交互迭代记录、以及文档×源码对齐的 5-Gate QA 流程。
- **[`starlight-market-ai-npc-blueprint`](https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint)** — **《星海交易局》3D AI-NPC 原型进度记录**  
  Unity 6 URP 情报博弈原型的架构笔记与持续迭代记录（规则层隔离账本与机密、本机 16 GiB 显卡 `9.30 GiB` 四模型联调环境、Run 01–04 云端 `L4 BF16` 批跑演进日志与本地校验脚本）。
- **[`ai-field-notes`](https://github.com/feng46430-cloud/ai-field-notes)** — **人机协作踩坑与排雷笔记**  
  独立于具体项目仓之外，记录平时和 AI 协作写代码、搭评测、整理公开仓时踩过的坑、走过的弯路和解法（文末单向索引对应公开项目）。

<details>
<summary><strong>本地零依赖脚本（想直接跑着看的话）</strong></summary>

```bash
# 1) 卡池概率仿真、长周期曲线校准与 HITL CAS 内存态校验单测
git clone https://github.com/feng46430-cloud/ai-engineering-portfolio.git
python ai-engineering-portfolio/02-ai-eval-and-simulation/demo-simulation/run_gacha_box_sim.py
python ai-engineering-portfolio/02-ai-eval-and-simulation/demo-simulation/run_sim.py
node --test ai-engineering-portfolio/01-multi-agent-orchestrator/mve/mve.test.mjs

# 2) 核验《星海交易局》Run 03 脱敏评测快照的评分重算与门禁校验
git clone https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint.git
python starlight-market-ai-npc-blueprint/repro/verify_scorecard.py
```

</details>

---

*注：仓库中的架构思路、评测设计与验收由本人主导，编码与脚本协同 AI Coding 工具完成；内容均已脱敏，不含任职企业 NDA 资产。*
