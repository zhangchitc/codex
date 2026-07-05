# codex

「Codex 工作原理」系列视频的 HTML slides 仓库。

结构参考 `~/claude_code`：每期视频一个目录，根目录 `index.html` 作为列表首页，`thumbs-tight/` 存放首页缩略图。

## 结构

- `NNN_topic/`：每期视频一个文件夹，存放该期 HTML slides。
- `index.html`：列表首页。
- `thumbs-tight/NNN.jpg`：首页缩略图，建议使用 slides 中信息量最高的一屏。

## 添加一期新 slides

1. 建立 `NNN_topic/` 目录，把 HTML slides 放进去。
2. 生成缩略图到 `thumbs-tight/NNN.jpg`。
3. 在 `index.html` 的 `.list` 里追加一个 `<a class="row">` 条目。
4. 如需发布，commit 并 push。

## 当前内容

- `069_reconnect/visual.html`：Reconnecting 背后的传输层问题。
- `070_codex_trace/structure_diagram.html`：一句 hello 背后的 Responses API 请求结构。
- `072_codex_tokenizer/visual.html`：文字如何变成token。
