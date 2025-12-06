# 文档结构与命名规范

## 目录结构

```
shiye/
├── .cursor/
│   ├── commands/          # Cursor命令定义
│   ├── templates/         # 文档模板
│   └── rules/            # 项目规则（本目录）
├── daily_tasks/          # 每日任务文件
├── daily_task_materials/ # 学习材料
│   ├── notes/            # 学习笔记
│   ├── references/       # 参考资料/模拟题
│   ├── exam_points_summary/ # 考点总结
│   └── wrong_questions/  # 错题本
├── 2026_Guangxi_Career_Exam_Plan_Go_Pattern.md  # 主计划文件
└── 2026_Guangxi_Career_Exam_Knowledge_Graph.md  # 知识图谱
```

## 命名规范

### 每日任务文件
- **格式**：`YYYY-MM-DD_Weekday.md`
- **示例**：`2025-12-05_Friday.md`
- **位置**：`daily_tasks/`

### 学习笔记文件
- **格式**：`Day{N}_{Topic}.md`
- **示例**：`Day1_DataAnalysis_Formula.md`
- **位置**：`daily_task_materials/notes/`
- **命名规则**：
  - 使用英文主题名（如：DataAnalysis, Graphic, Logic）
  - 使用描述性后缀（如：Formula, Verbal, Translation）

### 参考资料文件
- **格式**：`Day{N}_{Topic}_{SubTopic}.md`
- **示例**：`Day1_GrowthRate_Practice.md`, `Day1_CaseStudy_SongchiChina.md`
- **位置**：`daily_task_materials/references/`
- **命名规则**：
  - 练习类：`{Topic}_Practice.md`
  - 模拟题：`{Topic}_Mock.md`
  - 案例研究：`CaseStudy_{Name}.md`
  - 晨读材料：`Morning_Read.md`

### 考点总结文件
- **格式**：`Day{N}_{Topic}_{SpecificPoint}.md`
- **示例**：`Day1_DataAnalysis_KeyPoints.md`, `Day1_Calculation_Techniques_DirectDivision.md`
- **位置**：`daily_task_materials/exam_points_summary/`

### 错题文件
- **格式**：`YYYYMMDD_Module_QuestionID.png`
- **示例**：`20251205_DataAnalysis_01.png`
- **位置**：`daily_task_materials/wrong_questions/`
- **模块标识**：DataAnalysis, Graphic, Logic, Verbal, Quantitative, CommonSense

## 文档链接规范

### 相对路径规则
- 从任务文件链接到笔记：`../daily_task_materials/notes/{filename}`
- 从笔记链接回任务：`../../daily_tasks/{filename}`
- 从任务链接到参考资料：`../daily_task_materials/references/{filename}`

### Markdown链接格式
```markdown
- 📘 笔记: [Day1_DataAnalysis_Formula.md](../daily_task_materials/notes/Day1_DataAnalysis_Formula.md)
- 📄 模拟题: [Day1_GrowthRate_Practice.md](../daily_task_materials/references/Day1_GrowthRate_Practice.md)
- 📂 错题本: [wrong_questions/](../daily_task_materials/wrong_questions/README.md)
```

## 文档模板使用

### 任务文件模板
- **模板位置**：`.cursor/templates/daily_task_template.md`
- **使用场景**：创建新的每日任务文件时
- **变量替换**：`{{day_number}}`, `{{date}}`, `{{weekday}}`, `{{target_description}}`等

### 笔记文件模板
- **模板位置**：`.cursor/templates/note_template.md`
- **使用场景**：创建新的学习笔记时
- **必需字段**：核心概念、技巧与公式、避坑指南

### 参考资料模板
- **模板位置**：`.cursor/templates/reference_template.md`
- **使用场景**：创建模拟题或案例材料时
- **必需字段**：材料、练习任务、答题区


