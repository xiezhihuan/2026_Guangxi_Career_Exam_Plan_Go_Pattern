---
description: 生成每日复习任务及配套资料
---

# 命令：/create_daily_task

本规则定义了如何生成每日复习任务文件及其配套的学习资料。

## 触发方式
用户输入：`/create_daily_task`

## 上下文信息
- **计划文件**: `2026_Guangxi_Career_Exam_Plan_Go_Pattern.md` (参考其中的"行动计划"或当前进度)
- **模板目录**: `.cursor/templates/`
- **输出目录**:
  - 任务文件: `daily_tasks/`
  - 笔记文件: `daily_task_materials/notes/`
  - 参考资料: `daily_task_materials/references/`

## 执行步骤

1.  **分析上下文**:
    - 确定任务的 **日期** 和 **天数** (通常是 `daily_tasks/` 目录下最新文件的后一天)。
    - 回顾 **计划文件**，根据当前的复习阶段，决定 G1(晨间)、G3(午间)、G4(晚间) 具体要复习的科目和知识点。

2.  **生成文件**:
    - **任务文件**: 使用模板 `.cursor/templates/daily_task_template.md` 创建 `daily_tasks/YYYY-MM-DD_Weekday.md`。将模板中的占位符 (`{{...}}`) 替换为具体的学习内容。
    - **笔记文件**: 使用模板 `.cursor/templates/note_template.md` 创建 `daily_task_materials/notes/DayN_{Topic}.md`。并在任务文件和笔记文件之间建立双向链接。
    - **参考资料**: 使用模板 `.cursor/templates/reference_template.md` 创建 `daily_task_materials/references/DayN_{Topic}.md` (仅当 G4 包含主观题练习时)。并在任务文件和资料文件之间建立双向链接。

3.  **更新计划**:
    - 将新生成的任务日志条目追加到 `2026_Guangxi_Career_Exam_Plan_Go_Pattern.md` 文件的 "8. 执行日志 (Action Log)" 章节中。

## 文件命名规范
- 任务文件: `YYYY-MM-DD_{Weekday}.md` (例如: `2025-12-06_Saturday.md`)
- 笔记文件: `Day{N}_{Topic}.md` (例如: `Day2_Verbal_Logic.md`)
- 参考资料: `Day{N}_{Topic}_Mock.md` (例如: `Day2_Composite_B_Mock.md`)

## 行为准则
- 始终使用预定义的模板。
- 确保文件之间的链接是相对路径且准确无误。
- **不要** 覆盖已存在的文件，除非用户明确要求。
