# Project Spine V0.2 产品概览

Project Spine 是一款帮助长期项目保持结构、上下文与执行脉络的 Windows 桌面工具。

它不把项目压缩成一串孤立任务，而是用 Project、Phase、Module、Task 与 Decision 组织完整脉络，并通过 Current Node 标记真正需要推进的位置。

## 两种工作空间

### Mini Workspace

Mini 是 V0.2 的默认日常入口。它保持当前项目、进度、阶段主线和当前路径可见，并提供项目切换、Task 状态更新、Quick Note、置顶、最小化与 Main 切换。

### Main Workspace

Main 用于查看和编辑完整项目结构。用户可以维护节点详情、目标、任务清单、关键产出、完成标准和备注，也可以在树形视图与 Canvas 之间切换。

## 从想法到项目脉络

Project Spine 支持导入 Blueprint JSON。用户可以让 AI 阅读公开的 Blueprint Generation Specification，根据自己的目标生成结构，再由 Project Spine 完成校验与预览。

```text
项目需求 → AI 生成 Blueprint → Project Spine 校验 / 预览 → 导入 → 开始执行
```

V0.2 继续使用 Blueprint Schema `0.1`，现有规范与模板无需升级版本号。

## 本地优先的数据管理

项目数据保存在本地。V0.2 支持选择主要项目数据的保存位置，并提供数据目录迁移入口。软件安装位置与业务数据位置相互独立，便于根据磁盘和工作方式进行安排。

## 适合的使用场景

- 需要跨数周或数月推进的个人项目；
- 包含多个阶段、模块、任务和关键决策的复杂工作；
- 经常中断，需要快速恢复上下文的项目；
- 希望用 AI 先建立结构，再在本地持续执行的工作流。

Project Spine 当前面向 Windows x64，V0.2.0 RC1 为预发布候选版本。
