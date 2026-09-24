# Project Spine AI Blueprint 模板

本目录提供 Project Spine Blueprint V0.1 的公开生成规范、基础模板和完整示例。你可以把这些文件与自己的项目需求一起提供给 AI，让 AI 生成可由 Project Spine 校验并导入的 Blueprint JSON。

## 文件说明

### AI Blueprint Generation Specification

[Project_Spine_AI_Blueprint_Generation_Specification_V0.1.md](Project_Spine_AI_Blueprint_Generation_Specification_V0.1.md)

这是提供给 AI 阅读的正式生成规范，说明 Blueprint 的节点类型、层级关系、字段映射、状态约束和输出规则。生成前，应优先让 AI 阅读此文件。

### Blueprint JSON Template

[Blueprint_Template_V0.1.json](Blueprint_Template_V0.1.json)

这是符合 Project Spine Blueprint Import Schema V0.1 的基础 JSON 模板。AI 可以在保留字段结构和层级规则的前提下，用真实项目内容替换模板中的提示文字。

### Example Blueprint

[Example_Project_Blueprint.json](examples/Example_Project_Blueprint.json)

这是一个完整、可导入的示例，用于展示 Project、Phase、Module 和 Task 如何组成项目脉络，以及任务状态、检查项、产出和完成标准应如何表达。

## 推荐使用流程

1. 准备项目目标、预期成果、约束和当前进度；
2. 将生成规范和 JSON 模板提供给 AI；
3. 要求 AI 只输出合法 Blueprint JSON，不附加解释文字或 Markdown 代码围栏；
4. 对照示例检查层级、节点状态和当前节点；
5. 将生成的 `.json` 文件导入 Project Spine；
6. 在导入预览中确认校验结果，再建立项目。

Project Spine 会在导入前检查 JSON 格式、节点类型、层级关系和 Current Node 唯一性。AI 生成的内容仍应由用户确认，确保它真实反映项目范围和执行状态。

[返回 Project Spine 产品介绍](../README.md)
