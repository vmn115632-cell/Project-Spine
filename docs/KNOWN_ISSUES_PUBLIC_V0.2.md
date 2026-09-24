# Project Spine V0.2 Known Issues

本文列出 `v0.2.0-rc.1` 中与用户相关的已知限制。

## Release Candidate

当前版本是 Release Candidate，不是 Stable。它已经可以用于实际体验，但仍建议对重要项目数据保持谨慎。

## Windows 安装包未签名

当前 Installer 尚未进行 Authenticode 代码签名。Windows SmartScreen 可能显示“未知发布者”或额外安全提示。

请只从本仓库正式 Releases 页面下载，并在安装前核对文件名、版本和 SHA-256。不要通过关闭系统安全功能来绕过提示。

## V0.1 升级覆盖

V0.1 到 V0.2 的完整实装覆盖升级场景尚未全部覆盖。升级前请正常关闭正在运行的 Project Spine，并为重要项目数据保留独立备份。

## 数据位置迁移

迁移重要项目数据前，建议确认目标磁盘可用并保留备份。迁移过程中不要强制终止应用或断开目标磁盘。

主要 Project Spine 项目数据可以存放到用户选择的位置；Windows 与应用运行框架仍可能在系统用户目录保存少量运行配置或缓存。

## Windows 窗口场景

部分极端的多显示器、显示器断开/重连、虚拟桌面或前台焦点竞争场景，仍可能在后续版本继续优化。
