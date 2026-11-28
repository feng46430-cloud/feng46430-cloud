# 徐峰（Feng Xu）

**AI 玩法与智能 NPC 系统设计 · AI 评测（Eval）与质量工程（QA Lead，2020 至今）** · 上海

[![Portfolio CI](https://github.com/feng46430-cloud/ai-engineering-portfolio/actions/workflows/verify.yml/badge.svg)](https://github.com/feng46430-cloud/ai-engineering-portfolio/actions/workflows/verify.yml)
[![Starlight CI](https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint/actions/workflows/verify.yml/badge.svg)](https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint/actions/workflows/verify.yml)

<img src="https://raw.githubusercontent.com/feng46430-cloud/starlight-market-ai-npc-blueprint/main/media/01_blind_start_theater.png" alt="星海交易局 Unity 6 URP 3D AI-NPC 实验原型" width="100%" />

专注用**确定性规则边界、不注水的自动化评测与可控变量实验**解决 AI 交互玩法和质量工程里的真实问题。

---

### 核心公开仓库（2 个主入口）

1. **[`ai-engineering-portfolio`](https://github.com/feng46430-cloud/ai-engineering-portfolio)** — **综合作品集主入口（推荐先看）**  
   含 5 项核心实证：AI 评测打假（拆穿 98% 假全绿、“注入率 ≠ 表达率”）、5,000 盒抽卡防摸包与期望守恒仿真、4 段端到端延迟控变量拆解与底层排障、废弃连线画布的产品减法实拍对比、以及 5-Gate 文档×源码防幻觉 QA 规范。
2. **[`starlight-market-ai-npc-blueprint`](https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint)** — **《星海交易局》3D AI-NPC 实验原型**  
   Unity 6 URP 盲测博弈原型（规则层隔离账本与机密、单机 16 GiB 显卡 `9.30 GiB` 四模型本地演示环境）、3 轮云端 `L4 BF16` 批跑实测记录（如实公开当前 `48.62 · F` 开放缺陷与通用精排负向边界实证）与本地校验脚本。

<details>
<summary><strong>30 秒本地零依赖验证命令</strong></summary>

```bash
# 1) 5,000 盒卡池概率守恒与防摸包仿真 + 数值校准 + HITL CAS 单测
git clone https://github.com/feng46430-cloud/ai-engineering-portfolio.git
python ai-engineering-portfolio/02-ai-eval-and-simulation/demo-simulation/run_gacha_box_sim.py
python ai-engineering-portfolio/02-ai-eval-and-simulation/demo-simulation/run_sim.py
node --test ai-engineering-portfolio/01-multi-agent-orchestrator/mve/mve.test.mjs

# 2) 核验《星海交易局》Run 03 脱敏诊断快照重算与严格定级审计
git clone https://github.com/feng46430-cloud/starlight-market-ai-npc-blueprint.git
python starlight-market-ai-npc-blueprint/repro/verify_scorecard.py
```

</details>

---

*声明：以上仓库架构规格、评测体系与验收由本人主导，协同 AI Coding 工具实现；内容已脱敏，不含任职企业 NDA 资产。*
