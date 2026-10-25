**简体中文** | [English](README-EN.md) | [繁體中文](README-ZH_TW.md)

# PCL-CE unrestrict

跟随 [PCL 社区版（PCL-CE）](https://github.com/PCL-Community/PCL-CE) 官方发版，自动构建解除地区功能限制的版本。

本仓库是个人维护的非官方 fork，源码和主要功能来自上游。修改集中在 `RestrictedFeaturePolicy.cs`：保留地区评估逻辑，让地区功能限制检查直接放行。

## 下载

前往 [Releases](https://github.com/RyanWu080/PCL-CE-unrestrict/releases)，选择对应版本的附件：

- 普通 Intel / AMD Windows 电脑：`PCL2_CE_Release_x64_unrestrict.exe`，Beta 对应 `PCL2_CE_Beta_x64_unrestrict.exe`。
- Windows ARM 设备：选择文件名包含 `ARM64_unrestrict.exe` 的附件。
- 运行环境：[.NET 10 Desktop Runtime](https://get.dot.net/10)。

请下载带 `unrestrict` 的可执行附件。Release 中的自动源码压缩包来自官方原始标签；解除限制补丁保存在本仓库的 `.github/release-sync/RestrictedFeaturePolicy.cs`，构建来源和文件校验值见附件 `unrestrict-build.json`。

## 自动发布规则

- 以 **v2.15.1 正式版**为起点；不补发 v2.15.1 之前的版本或 v2.15.1 的旧 Beta。
- 每小时第 41 分钟检查官方新 Release，包括后续更高版本的正式版和 Beta。GitHub 调度可能延迟。
- 根据官方对应标签取源码、应用补丁，分别构建 x64 和 ARM64；构建成功后才公开发布。
- 标签、版本标题、说明和正式 / Beta 标识跟随官方；附件名增加 `unrestrict`。已发布版本不会重复构建，官方说明更新时会同步。
- 上游限制代码变化、补丁不兼容或编译失败时停止该版本发布，等待检查。

Release 说明按官方原文同步，其中的外部下载链接和签名信息属于官方发行版；本仓库修改后的附件以本仓库的 Assets 为准。

## 分支与工作流

| 位置 | 用途 |
| --- | --- |
| `dev`（默认分支） | 本仓库说明、自动化配置和发布脚本 |
| `custom/dev-unrestricted` | 跟随上游 `dev` 的开发源码，保留单独的解除限制提交；其中说明文档沿用上游 |
| `sync-custom-dev.yml` | 每小时第 23 分钟合并上游开发代码，冲突时停止，保留补丁，不强制推送 |
| `follow-official-releases.yml` | 检测官方 Release、构建并发布对应的解除限制版 |

发布构建使用**官方版本标签**，不使用开发分支的最新代码。开发源码同步与 Release 发布相互独立。

## 当前验证范围

已验证自动同步、版本筛选、编译和发布流程；实际启动、登录和下载功能仍需运行验证。构建未包含官方私有服务密钥，依赖这些密钥的服务功能可能与官方构建不同。官方签名不适用于修改后的二进制文件。

## 来源与许可

- 上游项目：[PCL-Community/PCL-CE](https://github.com/PCL-Community/PCL-CE)，基于龙腾猫跃的 PCL 开源代码，由社区开发者维护。
- `Plain Craft Launcher 2/` 使用原有 [自定义许可证](Plain%20Craft%20Launcher%202/LICENCE)。
- 其余目录使用 [Apache License 2.0](LICENSE)。原有许可证、版权和作者归属保持不变。

本 fork 的自动化和解除限制相关问题请先在本仓库排查，勿将其当作官方发行版反馈。
