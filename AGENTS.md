# Repository Guidelines

这个仓库存放「Codex 工作原理」系列视频的 HTML slides。

## 结构

- `NNN_topic/`：每期视频一个目录，例如 `069_reconnect/`。
- `index.html`：首页列表。
- `thumbs-tight/NNN.jpg`：首页缩略图。

## 编辑约定

- HTML slides 优先保持单文件自包含；必要素材放在同一期目录下。
- 可见文案使用清晰中文短句。
- 新增、重命名或删除期数时，同步更新 `index.html`。
- 新增页面的首页条目必须追加到 `index.html` 列表最末尾。

## 视觉验证

修改 HTML slides 后，必须使用 Playwright CLI 预览和截图：

```bash
playwright-cli open file:///.../NNN_topic/visual.html
playwright-cli resize 1440 900
playwright-cli screenshot --filename thumbs-tight/NNN.jpg
```

如果 `file://` 被当前环境阻止，可以临时启动只绑定 `127.0.0.1` 的本地静态服务，再继续使用 Playwright CLI。不要静默改用 Google Chrome headless 或其他截图方式。

## OpenAI 相关事实来源

涉及 OpenAI API、SDK、Codex 或其他 OpenAI 产品的问题时，优先使用官方 OpenAI 开发者文档作为事实来源，不要先依赖普通网页搜索。
