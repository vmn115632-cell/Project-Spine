# Project Spine V0.2 Release Notes

当前版本：`v0.2.0-rc.1`

状态：Pre-release / Release Candidate

平台：Windows x64

V0.2 重点提升 Mini 的日常使用体验，并补全数据位置控制和项目生命周期能力。

## Mini Workspace

- 默认以 Mini 作为日常工作入口；
- 直接查看当前项目、总体进度、当前路径和项目主脉络；
- 在 Mini 中快速切换项目；
- 快速修改 Task 状态，包括完成、重新打开、开始处理和阻塞；
- Quick Note 支持查看已有记录，并与 Main 中的 Notes 保持一致；
- 优化 Pin、最小化、关闭以及 Main / Mini 切换体验。

## 项目管理

- 支持编辑项目名称与描述；
- 支持删除项目，并在删除前提供独立确认；
- 删除项目时继续保护项目数据一致性，并为其他项目选择合适的回退入口。

## 数据与安装

- Windows 安装向导支持自定义软件安装目录；
- 支持选择 Project Spine 主要项目数据的保存位置；
- 支持从应用内迁移数据目录；
- 软件程序与业务数据相互独立，卸载应用时默认保留业务数据。

Windows 与应用运行框架仍可能在系统用户目录保存少量运行配置或缓存。

## 性能与稳定性

- 针对较大项目优化 Mini 状态更新与界面渲染；
- 减少普通点击、展开和状态操作时的界面阻塞；
- 改善 Windows 窗口恢复、前台显示和生命周期行为。

## AI Blueprint

AI Blueprint Generation 继续可用，Blueprint Schema 仍为 `0.1`。现有 V0.1 生成规范、基础模板和公开示例可继续使用。

## 下载校验

- 文件：`Project-Spine-Setup-0.2.0-rc.1.exe`
- 大小：`123,360,429 bytes`
- SHA-256：`44C904089913C52FBB4351B80168C43C75DA66C18CE46C892887DBDCE0594973`

当前版本仍为 Release Candidate，安装前请同时阅读 [安装说明](INSTALL_GUIDE.md) 与 [Known Issues](KNOWN_ISSUES_PUBLIC_V0.2.md)。
