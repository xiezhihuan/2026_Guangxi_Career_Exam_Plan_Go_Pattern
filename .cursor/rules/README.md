# 项目规则总览

本目录包含项目的所有核心规则和规范，用于指导项目的开发、维护和使用。

## 规则文件索引

### 1. [项目概述与核心原则](./project_overview.md)
- 项目性质与目标
- 核心原则（Go语言设计模式隐喻、在职备考优化、科学记忆规律）
- 目标用户画像
- 考试目标

### 2. [文档结构与命名规范](./documentation_structure.md)
- 目录结构说明
- 文件命名规范（任务、笔记、参考资料、错题）
- 文档链接规范
- 模板使用说明

### 3. [时间管理与任务调度规则](./time_management.md)
- Goroutine调度模型（G1-G4协程）
- 时间分配策略（职测、综应）
- 异常处理与熔断机制
- Deadline控制

### 4. [学习策略与记忆规律](./learning_strategy.md)
- 4D原则（新学、复习、练习、平衡）
- 三阶段备考架构（Stage 1-3）
- 各模块学习策略
- 解题算法与技巧

### 5. [Go语言设计模式隐喻规则](./go_pattern_metaphor.md)
- 常用隐喻对照表（并发、系统架构、数据处理、错误处理）
- 文档中的Go风格示例
- 命名规范
- 注释风格

### 6. [错题管理规范](./error_management.md)
- 错题收集规则
- 复盘三问（为什么错、正确思路、如何避坑）
- 错题复盘流程
- 错题分析模板

### 7. [Cursor命令使用规则](./cursor_commands.md)
- `/create_daily_task`：生成每日任务
- `/answer_reference`：点评主观题答案
- 命令使用场景
- 命令扩展规则

## 快速参考

### 核心原则速查
1. **Go语言设计模式隐喻**：所有策略都用Go概念组织
2. **在职备考优化**：时间分片、上下文切换、熔断降级
3. **科学记忆规律**：Day-1、Day-3、Day-7滚动复习
4. **结构化文档管理**：Markdown格式，双向链接

### 时间协程速查
- **G1**：06:30-07:30，晨间协程，CPU密集型任务
- **G1.5**：07:30-08:30，晨间缓冲，Life Support + 晨读
- **G2**：08:30-09:00，通勤微服务，IO等待型任务
- **G3**：12:00-13:30，午休协程，Motion + Study + Eat + Sleep
- **G4**：20:00-23:00，晚间批处理，系统性学习

### 文件命名速查
- **任务文件**：`YYYY-MM-DD_Weekday.md`
- **笔记文件**：`Day{N}_{Topic}.md`
- **参考资料**：`Day{N}_{Topic}_{SubTopic}.md`
- **错题文件**：`YYYYMMDD_Module_QuestionID.png`

### 4D原则速查
- **New Learning**：工作日1-2个新知识点
- **Review**：Day-1、Day-3、Day-7滚动复习
- **Practice**：学练结合，错题重做
- **Balance**：计算类与语言逻辑类交替

## 使用建议

1. **新用户**：先阅读[项目概述](./project_overview.md)，了解项目整体情况
2. **创建任务**：参考[文档结构规范](./documentation_structure.md)和[时间管理规则](./time_management.md)
3. **学习规划**：参考[学习策略](./learning_strategy.md)中的4D原则和三阶段架构
4. **错题管理**：遵循[错题管理规范](./error_management.md)进行复盘
5. **使用命令**：查看[Cursor命令规则](./cursor_commands.md)了解可用命令

## 规则更新

当项目规则发生变化时，请及时更新对应的规则文件，并在此README中更新索引和快速参考部分。

## 相关文档

- **主计划文件**：`2026_Guangxi_Career_Exam_Plan_Go_Pattern.md`
- **知识图谱**：`2026_Guangxi_Career_Exam_Knowledge_Graph.md`
- **命令定义**：`.cursor/commands/`
- **文档模板**：`.cursor/templates/`

