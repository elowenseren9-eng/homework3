# 打印样式研究

## 资料

- MDN Printing：https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Printing
- MDN `@media`：https://developer.mozilla.org/en-US/docs/Web/CSS/@media

## 实验

专题页在 `@media print` 中加入专用规则：

- `.site-header, .site-footer { display: none; }`：打印时隐藏导航和页脚，避免出现只对屏幕浏览有用的内容。
- `body` 改为黑字白底：节省彩色墨水并保证打印对比度。
- `main { width: 100%; }`：正文使用纸张可用宽度。
- `.card-grid, .tip-list { grid-template-columns: 1fr; }`：把网格改为单栏，按照阅读顺序打印。
- `.feature-card { break-inside: avoid; }`：尽量避免一张卡片被分页拆开。
- `@page { margin: 1.5cm; }`：为纸张四周保留稳定页边距。

## 检查结果与截图

人工截图时在浏览器按 `Ctrl+P` 打开打印预览。预览中导航和页脚应消失，正文与六张卡片按单栏排列，页面使用黑字白底。
