# 流式排版研究

## 资料

- MDN `clamp()`：https://developer.mozilla.org/en-US/docs/Web/CSS/clamp
- MDN `min()`：https://developer.mozilla.org/en-US/docs/Web/CSS/min

## 实验

专题页原来的主标题和二级标题分别使用 `40px`、`28px` 固定字号。实验后改为：

```css
h1 { font-size: clamp(2rem, 1.3rem + 3vw, 4rem); }
h2 { font-size: clamp(1.5rem, 1.2rem + 1vw, 2rem); }
```

`clamp(最小值, 首选值, 最大值)` 会把首选值限制在上下界之间。主标题最小为 `2rem`，首选值随视口宽度 `3vw` 平滑增长，最大不超过 `4rem`；因此手机上不会过大，桌面上也不会无限增大。二级标题使用较小的变化范围，保持层级关系。

页面容器还使用 `width: min(100% - 2rem, 68rem)`：浏览器会选择两个值中较小的一个，使窄屏保留边距、宽屏限制行宽。

## 截图对比

人工截图时分别设置 375px、768px、1200px 宽度。三档中标题应逐渐增大，卡片分别为一列、两列、三列，并且页面没有横向滚动。
