
# 衡水体英语字体 (Hengshui English Handwriting Fonts)

> 根据中高考英语试卷"衡水体"书写风格制作的开源英文字体，提供 TTF / OTF / WOFF / WOFF2 / SVG 五种格式。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 项目简介

本项目包含两套根据中国中高考英语试卷上流行的**"衡水体"**书写风格制作的英文字体。

**衡水体**是中国中学生英语考试中一种非常流行的书写风格，其特点是：

- 字母圆润饱满，笔画均匀
- 排列整齐紧凑，行距均匀
- 倾斜度小，接近印刷体效果
- 整体观感工整美观，阅卷友好

本项目将这种手写风格数字化为矢量字体，方便在各种场景中使用。

---

## 字体介绍

### 1. 衡水中性笔体（Hengshui Gel Pen）

模拟中性笔（凝胶笔）书写效果。笔画圆润流畅，线条粗细较为均匀，适合日常书写、文档排版和打印使用。

| 属性 | 值 |
|------|------|
| 字体名称 | 衡水中性笔体 |
| 英文名 | Hengshui Gel Pen |
| 字体族 ID | `hengshui_gelpen` |
| 字重 | Regular (400) |
| 字体方向 | 水平 |

### 2. 衡水钢笔体（Hengshui Fountain Pen）

模拟钢笔书写效果。笔画带有钢笔书写的自然粗细变化，起笔和收笔处有明显的笔触特征，更具手写感和书写韵味。

| 属性 | 值 |
|------|------|
| 字体名称 | 衡水钢笔体 |
| 英文名 | Hengshui Fountain Pen |
| 字体族 ID | `hengshui_fountainpen` |
| 字重 | Regular (400) |
| 字体方向 | 水平 |

---

## 可用格式

每套字体均已转换为以下五种格式，覆盖桌面应用、Web 开发和矢量图形等场景：

| 格式 | 扩展名 | 适用场景 |
|------|--------|----------|
| TTF (TrueType Font) | `.ttf` | 兼容性最好，适用于 Windows / macOS / Linux 系统及大多数办公软件 |
| OTF (OpenType Font) | `.otf` | 支持更多高级排版功能（连字、替代字形等），适合专业排版 |
| WOFF | `.woff` | Web 字体格式，适用于 CSS `@font-face` 嵌入网页 |
| WOFF2 | `.woff2` | Web 字体格式，压缩率比 WOFF 更高，页面加载更快 |
| SVG | `.svg` | 矢量格式，可无限放大不失真，也可作为 SVG 字体直接在 HTML 中使用 |

---

## 快速开始

### Web 使用（CSS @font-face）

```css
/* 衡水中性笔体 */
@font-face {
  font-family: 'Hengshui Gel Pen';
  src: url('fonts/hengshui_gelpen.woff2') format('woff2'),
       url('fonts/hengshui_gelpen.woff') format('woff'),
       url('fonts/hengshui_gelpen.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
}

/* 衡水钢笔体 */
@font-face {
  font-family: 'Hengshui Fountain Pen';
  src: url('fonts/hengshui_fountainpen.woff2') format('woff2'),
       url('fonts/hengshui_fountainpen.woff') format('woff'),
       url('fonts/hengshui_fountainpen.ttf') format('truetype');
  font-weight: normal;
  font-style: normal;
}

/* 使用字体 */
body {
  font-family: 'Hengshui Gel Pen', 'Hengshui Fountain Pen', cursive;
}
```

### SVG 字体直接在 HTML 中使用

```html
<!-- 将 SVG 字体文件直接嵌入页面 -->
<object type="image/svg+xml" data="hengshui_gelpen.svg#hengshui_gelpen-Regular"></object>
```

### 桌面应用安装

将 `.ttf` 或 `.otf` 文件双击，在字体预览器中确认效果后点击"安装"即可在系统中使用该字体。

---

## 文件结构

```
├── README.md                  # 项目说明文件
├── LICENSE                    # MIT 开源许可证
├── 衡水中性笔体.ttf
├── 衡水中性笔体.otf
├── 衡水中性笔体.woff
├── 衡水中性笔体.woff2
└── 衡水中性笔体.svg
├── 衡水钢笔体.ttf
├── 衡水钢笔体.otf
├── 衡水钢笔体.woff
├── 衡水钢笔体.woff2
└── 衡水钢笔体.svg


## 注意事项

1. **Web 性能**：生产环境推荐使用 WOFF2 格式以获得最佳压缩效果；如需兼容旧版浏览器，可同时提供 WOFF 作为降级方案。
2. **SVG 字体**：SVG 格式可直接在浏览器中通过 `<object>` 或 `@font-face` 引入使用，但部分浏览器可能对 SVG 字体支持有限，建议作为备选方案。
3. **字符集**：当前版本主要覆盖英文字母（大写/小写）、数字及常用标点符号。如需扩展字符集（如希腊字母、音标符号等），欢迎提交 Issue 或 Pull Request。
4. **字体渲染**：不同操作系统和浏览器的字体渲染引擎存在差异，建议在实际部署环境中测试渲染效果。

---

## 开源协议

本项目采用 **MIT 协议** 开源。

你可以自由地：

- 商业使用
- 修改字体
- 分发副本
- 集成到闭源项目中

但需保留版权声明和许可声明。

详见 [LICENSE](LICENSE) 文件。

---

## 贡献指南

欢迎提交 Issue 反馈问题或提出改进建议，也欢迎提交 Pull Request 参与开发。

贡献前请阅读：

1. 确保代码风格一致
2. 更新相关文档
3. 提交清晰的 Commit Message

---

## 联系方式

如有问题或合作意向，欢迎通过 [Issues](../../issues) 联系我们。

---

*衡水体字体 — 让英文书写更工整美观*
