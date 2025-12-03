---
description: 生成符合科学记忆规律的每日复习任务
---

# 命令：/create_daily_task

本规则定义了如何根据 **艾宾浩斯遗忘曲线** 和 **认知负荷理论**，生成科学的每日复习任务及配套资料。

## 触发方式
用户输入：`/create_daily_task`

## 核心逻辑：科学备考策略 (Scientific Strategy)

在生成任务前，必须遵循以下 **4D 原则** 进行排期：

1.  **New Learning (新学维度)**
    *   **容量控制**: 工作日每天仅安排 **1-2 个** 核心新知识点 (主要在 G1/G4 黄金时间)。
    *   **逻辑衔接**: 新知识点必须基于上一阶段的进度，确保知识链条连续。

2.  **Review (复习维度 - 对抗遗忘)**
    *   **强制回顾**: 每天分配 **10-15%** 的时间 (G1.5 晨读 / G3 午间) 用于“旧知唤醒”。
    *   **滚动周期**: 必须覆盖 **Day-1 (昨日)**、**Day-3 (前天)**、**Day-7 (上周)** 的错题或笔记。
    *   **周末汇总**: 周末必须安排一段时间对本周所有新学内容进行 System Review。

3.  **Practice (练习维度 - 闭环验证)**
    *   **学练结合**: 新知识点后必须紧跟一组 (5-10题) **专项训练 (Unit Test)**。
    *   **错题重做**: G3 或 G4 必须包含昨日错题的重做环节，确保消灭盲点。

4.  **Balance (调节维度 - 脑力续航)**
    *   **科目交替**: 穿插安排 **“计算类”** (资料/数量/图形) 与 **“语言逻辑类”** (言语/综应/逻辑)，利用大脑不同区域兴奋点。
    *   **难度弹性**: 
        *   **工作日 (Mon-Fri)**: 侧重碎片化、单一知识点突破。
        *   **周末 (Sat-Sun)**: 侧重系统化、全真模考 (Integration Test)、难点攻坚。

## 执行步骤 (Execution Pipeline)

1.  **Analyze (分析上下文)**
    *   **确定日期**: 识别目标日期及其属性 (工作日/周末)。
    *   **读取进度**: 扫描 `2026_Guangxi_Career_Exam_Plan_Go_Pattern.md`，确定当前 Stage 和已完成的 Topic。
    *   **应用策略**: 根据上述 **4D 原则**，规划 G1-G4 的具体内容。

2.  **Generate (生成文件)**
    *   **Task File**: 使用 `.cursor/templates/daily_task_template.md` 生成 `daily_tasks/YYYY-MM-DD_Weekday.md`。
    *   **Note File**: 使用 `.cursor/templates/note_template.md` 生成 `daily_task_materials/notes/DayN_{Topic}.md` (并在任务文件中建立双向链接)。
    *   **Reference File**: 使用 `.cursor/templates/reference_template.md` 生成 `daily_task_materials/references/DayN_{Topic}.md` (仅当涉及主观题/模考时)。

3.  **Update (更新日志)**
    *   将生成的任务链接追加到 `2026_Guangxi_Career_Exam_Plan_Go_Pattern.md` 的 **"8. 执行日志 (Action Log)"** 中。

## 目录结构与命名
*   **计划文件**: `2026_Guangxi_Career_Exam_Plan_Go_Pattern.md`
*   **输出目录**:
    *   任务: `daily_tasks/YYYY-MM-DD_{Weekday}.md`
    *   笔记: `daily_task_materials/notes/Day{N}_{Topic}.md`
    *   资料: `daily_task_materials/references/Day{N}_{Topic}_Mock.md`

## 行为准则
*   **禁止堆砌**: 不要为了赶进度而塞入过多内容，优先保证完成率。
*   **链接检查**: 确保生成的所有 Markdown 链接都能正确跳转 (使用相对路径)。
*   **幂等性**: 如果目标日期的文件已存在，除非用户明确要求覆盖，否则不要修改。
