# slidev-theme-prussianblue

[![NPM version](https://img.shields.io/npm/v/slidev-theme-prussianblue?color=3AB9D4&label=)](https://www.npmjs.com/package/slidev-theme-prussianblue)

[![Netlify Status](https://api.netlify.com/api/v1/badges/9c541f8b-74b5-4f87-80dc-a28abdf5d8c9/deploy-status)](https://app.netlify.com/sites/slidev-theme-prussianblue/deploys)

[Live demo](https://slidev-theme-prussianblue.netlify.app)

A (...) theme for [Slidev](https://github.com/slidevjs/slidev).

<!--
  Learn more about how to write a theme:
  https://sli.dev/themes/write-a-theme.html
--->

<!--
  run `npm run dev` to check out the slides for more details of how to start writing a theme
-->

<!--
  Put some screenshots here to demonstrate your theme

  Live demo: [...]
-->

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

<pre><code>---
theme: <b>prussianblue</b>
---</code></pre>

Learn more about [how to use a theme](https://sli.dev/themes/use).

## Layouts

This theme provides the following layouts:

### cover

![cover](export/01.png)

### default page

要使用下方的页面指示器，请在扉页中列出文章的大纲，并在每一页前标出相应的ID：


```
contents:
  - Slidev简介
  - 主题介绍
  - 使用说明

......

---
id: 1
---
```

![about](export/03.png)

## Components

This theme provides the following components:

### 滚动窗

[示例](https://slidev-theme-vatis.netlify.app/8),使用方法：

```html
<scrool h=30>
// 这里要注意空一行
...... Markdown ......
// 这里要注意空一行
</scrool>
```

等价于

```html
<div class="overflow-auto max-h-30">
// 这里要注意空一行
...... Markdown ......
// 这里要注意空一行
</div>
```

### 图片框

[示例](https://slidev-theme-vatis.netlify.app/9),使用方法：

```html
<mimage layout="c" url="URL" class="h-50" />
```

`layout` 为图片布局方式，有以下三种：
* 水平居中，上下环绕式
* 向右浮动式
* 右上角悬浮式(可能无法正常导出)

通过设置 `h` 或 `w` 可以控制图片的尺寸，默认为图片添加了圆角和阴影。

| 居中(center)(c)            | 向右(right)(r)         | 右上(rt)               |
| -------------------------- | ---------------------- | ---------------------- |
| ![居中布局](export/10.png) | ![向右](export/11.png) | ![右上](export/12.png) |


## 已知问题

* 在Mac与iPad上的元素定位可能会不大一致
* 导出为pdf时，每页下方会有一条白线
* 导出为pdf时，最后一页下方会有一块白色区域，可以在最后插入空白页并删除pdf中的空白页解决
* 图片阴影在某些PDF阅读器中可能显示不正确
* 右上角悬浮的图片样式可能无法正常导出


## Contributing

- `npm install`
- `npm run dev` to start theme preview of `example.md`
- Edit the `example.md` and style to see the changes
- `npm run export` to generate the preview PDF
- `npm run screenshot` to generate the preview PNG
