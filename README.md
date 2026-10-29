# AIProject

个人 AI 项目合集。每个项目使用独立目录，保留其上游文档、源码和许可证。

## 项目索引

| 项目 | 功能 | 上游 |
| --- | --- | --- |
| [VoiceStudio](./VoiceStudio/) | 声音克隆、语音合成、视频配音、转写和有声书 | [debpalash/VoiceStudio](https://github.com/debpalash/VoiceStudio) |

## 目录结构

```text
AIProject/
├── README.md
├── .gitmodules
└── VoiceStudio/
    ├── README.md
    ├── LICENSE
    ├── LICENSE-NOTICE.md
    └── ...
```

以后新增项目时，在仓库根目录创建对应的项目文件夹，并更新上方索引。

## 查看与使用 VoiceStudio

克隆仓库并初始化项目的子模块：

```bash
git clone --recurse-submodules https://github.com/ZachEvan/AIProject.git
cd AIProject/VoiceStudio
```

如已克隆仓库，在 AIProject 根目录执行：

```bash
git submodule update --init --recursive -- VoiceStudio/omnivoice-gallery
```

安装要求和操作步骤见 [VoiceStudio 项目说明](./VoiceStudio/README.md)及其 [macOS 安装指南](./VoiceStudio/docs/install/macos.md)。后续项目命令以 VoiceStudio 目录为工作目录。

## 来源、许可证与更新

- VoiceStudio 保存自上游提交 [9caf24171e51fcdc1b4a7eecc09ac0f2d9f2685e](https://github.com/debpalash/VoiceStudio/commit/9caf24171e51fcdc1b4a7eecc09ac0f2d9f2685e)。目录迁移时完整保留原项目内容和已有 Git 历史。
- 各项目遵循自己的许可证；VoiceStudio 的条款见 [LICENSE](./VoiceStudio/LICENSE) 和 [LICENSE-NOTICE.md](./VoiceStudio/LICENSE-NOTICE.md)。
- 仓库根目录的 `.gitmodules` 记录实际子模块路径；项目目录内保留的 `.gitmodules` 是上游原文件。
- 后续同步 VoiceStudio 时，只更新 `VoiceStudio/` 子目录及相应子模块映射。请勿直接使用 GitHub 的 **Sync fork** 将上游根目录合并到合集根目录。
- 上游 GitHub 工作流保存在 `VoiceStudio/.github/workflows/`，作为项目源码留存，不会作为本合集的工作流自动运行。部分依赖 Git 仓库根路径的开发或发布脚本需另行适配；需要完整上游开发流程时，可单独克隆上游仓库。
