# 平台对照

## 运行模型（两边相同）

```text
用户本机主题工具
    │  启动官方 Codex + 本机 CDP
    ▼
官方 Codex Desktop（不改 asar / 签名）
    │  注入 CSS + 装饰 DOM
    ▼
仍用原生侧栏 / 输入框 / 建议卡
```

## 路径速查

### macOS

| 用途 | 路径 |
|------|------|
| 源码（本整理包） | `Codex-Dream-Skin/macos/` |
| 安装后引擎 | `~/.codex/codex-dream-skin-studio` |
| 状态 / 日志 | `~/Library/Application Support/CodexDreamSkinStudio` |
| Codex 配置 | `~/.codex/config.toml`（仅外观相关项可能被改，可恢复） |

### Windows

| 用途 | 路径 |
|------|------|
| 源码（本整理包） | `Codex-Dream-Skin/windows/` |
| 状态 / 日志 | `%LOCALAPPDATA%\CodexDreamSkin` |
| Codex 配置 | `%USERPROFILE%\.codex\config.toml` |
| 默认 CDP 端口 | 首选 `9335`，冲突时自动选空闲口（Mac 包默认从 `9341` 起） |

## 能力矩阵

| 功能 | macOS | Windows |
|------|:-----:|:-------:|
| 安装脚本 | ✅ | ✅ |
| 启动 + 注入 | ✅ | ✅ |
| 一键恢复 | ✅ | ✅ |
| 实机 verify / 截图 | ✅ | ✅ |
| 用户选图定制 | ✅ | ✅（编辑 `windows/assets/theme.json` 并替换同目录图片） |
| 主题配置模型 | `theme.json` schema 1 | `theme.json` schema 1 |
| 官方签名校验 | ✅ | Store 签名类型 + 包身份 |
| 客户部署提示词 | ✅ | ❌（可用 Mac 文案改写） |
| 打客户 ZIP | ✅ `build-client-release.sh` | 手动压缩 `windows/` |

## 不要放进这个目录的东西

- API Key、`.codex/auth.json`
- 中转站密钥、服务器私钥
- 含客户隐私的实机截图（若要公开）

## 主题配置

当前默认视觉主题名为 **Aurora Atelier**：macOS 深色壳使用墨蓝与冰青，浅色壳和 Windows 使用奶油白、雾紫与珊瑚色；两端共享主题字段，但保留平台原生可读性适配。

两端都使用 `theme.json` schema 1。主题图片必须和配置文件位于同一目录，且只允许 PNG、JPEG 或 WebP；运行时会校验图片大小、文件名和配置字段，不会读取主题目录之外的路径。

- macOS：通过 `Customize` / `load-image-theme-macos.sh` 生成或替换 `~/Library/Application Support/CodexDreamSkinStudio/theme/`
- Windows：复制 `windows/assets/` 为自己的主题目录，编辑 `theme.json`，再把图片放在同目录；需要高级调用时可向 injector 传入 `--theme-dir <目录>`
