# Contributing to Codex Dream Skin

感谢参与 Codex Dream Skin。这个项目专注于 Codex Desktop 的外部主题、视觉体验和跨平台换肤工具链。

## 开发原则

- 只使用本机回环 CDP；不要开放 LAN 监听。
- 不修改官方 `.app`、`app.asar`、WindowsApps、签名或 API 配置。
- 不提交 `auth.json`、API Key、客户截图、本机 state 或日志。
- 新主题优先使用 `theme.json` schema 1，不要把文案和颜色重新硬编码到渲染器。

## 测试

macOS：

```bash
cd macos
npm test
```

Windows：

```powershell
powershell -File windows/tests/run-tests.ps1
```

视觉改动还应检查首页和任务页，并确认侧栏、项目选择、编辑器、建议卡片仍然可交互。

## Pull Request

请说明平台、用户价值、实际运行的测试，以及视觉改动前后的截图。提交信息优先使用 `type(scope): summary` 格式。
