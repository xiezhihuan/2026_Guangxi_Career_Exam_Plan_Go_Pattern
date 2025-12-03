# Day 2 重点笔记：逻辑判断 - 翻译推理

> **返回任务卡**: [2025-12-06_Saturday.md](../../daily_tasks/2025-12-06_Saturday.md)

## 1. 核心概念 (Core Concepts)
*   **翻译推理**: 将自然语言转化为逻辑表达式 ($A \rightarrow B$)。
*   **口诀**: “肯前必肯后，否后必否前”。

## 2. 技巧与公式 (Techniques & Formulas)

### 2.1 充分条件 (If...Then)
*   **关联词**: 如果...那么... / 只要...就... / 所有...都... / ...离不开...
*   **翻译**: **前推后** ($A \rightarrow B$)。
*   **例**: 如果下雨，地就会湿。 ($雨 \rightarrow 湿$)

### 2.2 必要条件 (Only If)
*   **关联词**: 只有...才... / 除非...否则不... / ...是...的基础/前提/关键。
*   **翻译**: **后推前** ($B \rightarrow A$)。
*   **例**: 只有努力，才能成功。 ($成功 \rightarrow 努力$)

### 2.3 逆否等价 (Contrapositive)
*   $A \rightarrow B$ 等价于 $\neg B \rightarrow \neg A$。
*   **否前** ($\neg A$) 和 **肯后** ($B$) 推不出确定结论（可能真也可能假）。

## 3. 避坑指南 (Pitfalls)
*   **“除非A否则B”**:
    *   标准翻译: $\neg B \rightarrow A$ (否后推前)。
    *   例: 除非下雨，否则我去跑步。 ($\neg 跑步 \rightarrow 下雨$ / $\neg 下雨 \rightarrow 跑步$)。
*   **不要用生活逻辑**: 逻辑题只认公式，不认常识。即使结论荒谬，只要符合推理规则就是对的。

