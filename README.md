# WPS 本地自动化与报告排版

WPS 本地自动化 Skill：Writer / Calc / Impress 操作、报告排版、会话准入与并发租约；含可迁移 wps-cli 后端。

这是独立的软件自动化项目，源文件、安装包和版本在本仓库分别维护。总合集只提供[项目分类索引](https://github.com/EagleRanger/windows-app-automation-skills)，不替代本仓库。

## 包含内容

- [wps-local-sync](skills/wps-local-sync/SKILL.md)
- [wps-report-workflow](skills/wps-report-workflow/SKILL.md)

## 下载与安装

从[本项目 Release](https://github.com/EagleRanger/wps-local-automation-skills/releases/latest) 下载独立 ZIP，解压后运行：

```powershell
powershell -ExecutionPolicy Bypass -File .\install.ps1 -All
```

安装器只复制本仓库的 2 个 Skill，可通过 `-Skill` 选装或 `-Destination` 指定目录。
相同内容重复安装不变，已有不同版本拒绝覆盖；`-WhatIf` 仅预览。不启动应用、不登录、不修改其他 Skill，不自动安装软件、后端或大模型。

## 使用条件与边界

随包提供 wps-cli 后端与 MIT 许可证。安装器仅复制 Skill；自行创建隔离 Python 环境、安装后端，并为两个 Skill 设置 WPS_LOCAL_AI_HOME。真实软件连接需接收方另行验收。

保留原 Skill 里的实测版本和失败边界；迁移包安装通过不等于接收方电脑已完成真实应用连接或业务验收。仅在当前用户授权范围内操作，保护已有文件与窗口。

## 来源、许可与贡献

见 [分项许可与来源](LICENSES.md)，以及各 Skill 保留的第三方说明。本包不含账号、密码、API 密钥、Cookie、生产图纸、私人日志和本机缓存。

EagleRanger 提出需求和验收；OpenAI Codex 协助整理、包装与校审。控制逻辑沿用已审查版本，本次只拆分发布结构。
