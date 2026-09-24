# Project Spine AI Blueprint Generation Specification V0.1

## 1. 文档目的

本文档定义 Project Spine Blueprint 的 AI 生成规范。

目标：

任何 AI 阅读本文档后，都能够理解 Project Spine 项目结构，并生成符合
Blueprint Import Schema V0.1 的 JSON 文件。

------------------------------------------------------------------------

## 2. Project Spine 核心理念

Project Spine 不是简单 Todo 工具。

它管理长期项目中的：

-   项目目标
-   阶段结构
-   执行节点
-   关键决策
-   项目产出
-   完成标准

结构：

    Project
    └── Phase
        └── Module
            ├── Task
            └── Decision

AI 的任务不是生成任务清单，而是将用户目标转换为完整项目脉络。

------------------------------------------------------------------------

## 3. Blueprint 顶层 JSON

合法结构：

``` json
{
  "schemaVersion": "0.1",
  "project": {},
  "nodes": []
}
```

允许字段：

-   schemaVersion
-   project
-   nodes

禁止：

-   version
-   metadata
-   currentNode

------------------------------------------------------------------------

## 4. Node 类型

### Phase

项目主要阶段：

``` json
"type": "phase"
```

### Module

概念上的 Stage：

``` json
"type": "module"
```

Project Spine 不使用 stage 类型。

### Task

执行节点：

``` json
"type": "task"
```

### Decision

关键决策：

``` json
"type": "decision"
```

完成 Decision 必须记录：

``` json
"decisionResult"
```

------------------------------------------------------------------------

## 5. 字段映射

  概念        JSON字段
  ----------- ---------------------
  版本        schemaVersion
  项目目标    project.description
  Stage       type=module
  节点目标    goal
  当前节点    status=doing
  Checklist   tasks
  完成标准    definitionOfDone
  决策        decision节点

禁止使用：

-   project.goal
-   stage
-   description
-   checklist
-   dod
-   decisions
-   currentNode

------------------------------------------------------------------------

## 6. 层级规则

合法：

    Project
    └── Phase
        └── Module
            ├── Task
            └── Decision

禁止：

-   Project 直接包含 Task
-   Task 包含 children
-   Decision 包含 children

------------------------------------------------------------------------

## 7. 状态规则

Task / Decision：

-   todo：未开始
-   doing：执行中
-   blocked：阻塞
-   done：完成

规则：

-   Phase 和 Module 不填写 status
-   全部 Blueprint 最多一个 doing
-   doing 即 Current Node
-   blocked 必须有 blockedReason
-   done Decision 必须有 decisionResult

------------------------------------------------------------------------

## 8. AI 生成流程

生成前分析：

1.  项目最终目标
2.  最终交付成果
3.  项目边界
4.  Phase 路线
5.  Module 划分
6.  Task 与 Decision
7.  当前真实状态

生成顺序：

项目目标 → Phase → Module → Task/Decision

不要从零散 Todo 拼项目。

------------------------------------------------------------------------

## 9. 结构设计要求

错误：

    学习 Python
    - 看视频
    - 写代码

正确：

    Python学习项目

    Phase:
    基础认知

    Module:
    Python语法基础

    Task:
    掌握变量与数据类型

------------------------------------------------------------------------

## 10. JSON 输出要求

最终输出：

只能包含合法 JSON。

禁止：

-   Markdown代码块
-   解释文字
-   注释
-   null
-   undefined
-   尾随逗号

输出必须可以保存为 UTF-8 `.json` 文件并直接导入 Project Spine。

------------------------------------------------------------------------

## 11. 输出前检查

检查：

-   顶层字段正确
-   schemaVersion 为 0.1
-   ID 唯一
-   Node 类型合法
-   层级合法
-   Task/Decision 无子节点
-   doing 不超过一个
-   blocked 有原因
-   Decision 完成有结果

------------------------------------------------------------------------

## Version

Project Spine AI Blueprint Generation Specification V0.1
