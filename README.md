# Kilo AI 客户端汉化配置

本仓库提供 Kilo AI 客户端的中文配置、指令文件和界面文本译名表，让 Kilo 的 **AI 回复**固定为简体中文，并提供配置文件的中文注释与界面字符串的中文对照。

> 说明：Kilo Desktop / Kilo CLI 目前**没有内置界面语言切换功能**（设置中无 Language 项，应用界面仅提供英文）。因此本仓库做两件事：
> 1. 通过全局指令让 AI 始终使用简体中文回复；
> 2. 提供界面字符串的中文译名表（`ui-strings.zh-CN.json`）供参考。

## 目录说明

```
kilo-zh/
├── AGENTS.md              全局中文指令文件（要求始终使用简体中文回复）
├── kilo.jsonc             Kilo AI 客户端配置文件（键名不变，仅添加中文注释）
├── ui-strings.zh-CN.json  界面字符串中文译名表（部分提取）
└── README.md              本文件
```

## 文件说明

| 文件 | 说明 |
| --- | --- |
| `AGENTS.md` | 全局指令：AI 的任何回复、计划、总结都使用简体中文；代码、命令、路径保持原样。 |
| `kilo.jsonc` | 客户端配置：所有键名与 JSON 结构保持英文原样，只添加 `//` 中文注释；`permission.bash` 预置了几条常用命令的允许规则。 |
| `ui-strings.zh-CN.json` | 从 `kilo.exe`（Kilo CLI/TUI 主程序）与 TUI 资源包中提取的可见界面字符串的中文译名。 |
| `README.md` | 本说明文件。 |

## 如何使用

1. 复制 `AGENTS.md` 到 Kilo 全局配置目录：

   ```text
   C:\Users\cuiyuxin\.config\kilo\AGENTS.md
   ```

   （macOS / Linux 对应 `~/.config/kilo/AGENTS.md`）

2. 复制 `kilo.jsonc` 到：

   ```text
   C:\Users\cuiyuxin\.config\kilo\kilo.jsonc
   ```

   注意：如果你本地已有 `kilo.jsonc`，请合并而不是直接覆盖，避免丢失原有配置。

3. 重启 Kilo Desktop 或新建会话，AI 的回复即为简体中文。

## 关于界面文本汉化

- 可执行文件位置（Windows，Kilo Desktop 0.1.11）：

  ```text
  C:\Users\cuiyuxin\AppData\Local\KiloDesktop\app-0.1.11\resources\kilo\windows-x64-baseline\bin\kilo.exe
  ```

  注意：`C:\Users\cuiyuxin\.config\kilo\kilo.exe` 并不存在。

- `ui-strings.zh-CN.json` 收录了设置分区名称（通用、外观、模型、权限、MCP 等）与内置工具名（应用补丁、搜索内容、读取文件等）的中文译名。
- 由于应用未内置 i18n 机制，将译文真正注入界面需要修改并重新打包应用，本仓库不包含该操作；如在 GitHub issue 中提出多语言支持请求，可加速官方中文化。

## 隐私说明

- 本仓库不包含任何本地绝对路径（文档中出现的路径均为官方文档式示例）。
- 不包含账号名、密码、密钥、Token。
- 不包含真实 API Key、数据库连接串、个人数据。
