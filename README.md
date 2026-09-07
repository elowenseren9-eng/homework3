# 软件开发综合实践 第三次课作业

本仓库完成《CSS布局、响应式设计与Bootstrap》课堂实践。

## 页面

- `courses-page/index.html`：纯 CSS 响应式课程展示页
- `courses-page/bootstrap.html`：Bootstrap 响应式课程展示页
- `topic-page/index.html`：云南四季风物响应式专题页

## 独立研究

- 流式排版：`clamp()` 与 `min()`
- 自动深色模式：`prefers-color-scheme`
- 打印样式：`@media print`

研究记录位于 `research/` 目录。

## 本地运行

在仓库根目录运行：

```bash
python -m http.server 8001
```

浏览器访问：

- <http://localhost:8001/courses-page/>
- <http://localhost:8001/courses-page/bootstrap.html>
- <http://localhost:8001/topic-page/>
