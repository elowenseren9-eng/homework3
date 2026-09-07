# 深色模式研究

## 资料

- MDN `prefers-color-scheme`：https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme

## 实验

专题页使用下面的媒体特性读取操作系统或浏览器的颜色偏好：

```css
@media (prefers-color-scheme: dark) {
  html { color-scheme: dark; }
  body { color: #e4eee8; background: #132019; }
}
```

当环境选择深色模式时，查询条件自动成立。页面会同时调整背景、正文、链接、导航、卡片、标签和边框颜色，而不是只把背景变黑。`color-scheme: dark` 也提示浏览器使用合适的深色内置控件配色。

## 检查结果与截图

人工检查时先使用系统浅色模式截图，再切换到深色模式并刷新页面截图。两种模式下应保持文字和背景有清晰对比，卡片边界可辨认，链接仍容易识别。
