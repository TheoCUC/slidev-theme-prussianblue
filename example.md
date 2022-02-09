---
theme: ./
contents: About|Image|Slidev
---

# Slidev Theme Starter

Presentation slides for developers

<div class="pt-12">
  <span @click="next" class="px-2 p-1 rounded cursor-pointer hover:bg-white hover:bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

---
id: 1
---

# About this theme

This theme has a great feature, the progress bar. 

To use this theme, you must fill the outline for this slider in the front matter.

```
contents: About|Image|Slidev
```

To highlight the section being demonstrated, you need to add the following code to the front of the page:

```
---
id: 1
---

# About this theme
```

To give it a Keynote-like appearance, I used the styles for headings and text in [@slidev/theme-apple-basic](https://github.com/slidevjs/themes/tree/main/packages/theme-apple-basic). The image was modified using [slidev-theme-purplin](https://github.com/moudev/slidev-theme-purplin) as a base; I really like this theme, but its image function isn't as powerful as I'd like.



---
layout: imagex
image: https://gitee.com/isaaccaa/pictures/raw/master/img2022/0186795d843896a8012060be1cbe75.jpg
pos: center
size: h-260px
id: 2
---

关于“一墩难求”的问题，北京冬奥组委新闻发言人赵卫东1月6日表示目前相关部门正在加大协调力度增加“冰墩墩”供应量。

“北京冬奥会的特许商品，将至少持续销售到今年6月底，可以满足广大消费者的需要。”有知情人士告诉《证券日报》记者，“相关北京冬奥会的特许生产企业正在积极投入到产品的生产当中，尽全力在保障产品质量的前提下，早日将产品投放市场”。


---
id: 2
---

## image

I'd like to make it simple to insert a picture and change its position and size. So, if you want to insert a picture on a single page, set the layout to `imagex` and paste the image's url into `image`.

While I just want to align my image to center or to right, I made a option to do this. When you type `pos: right`, the image will float to the right. And all other inputs will center your image.

The size is also an important consideration, as your image's size may not appear balanced in your slider for the first time. To change the size of the image, use `size: h-100px`, `size: h-1/3`, or `size: w-300px`.

---
id: 2
---

## image

Actually, the `size` attribute is linked to the img tag, so if you want to change its other style, just type something like `mx-5px` here. However, in **Windi CSS** style. 

The preceding page is represented by the flowing code.

```markdown
---
layout: imagex
image: https://gitee.com/isaaccaa/pictures/raw/master/img2022/0186795d843896a8012060be1cbe75.jpg
pos: center
size: h-260px
---
```

---
layout: imagex
image: https://gitee.com/isaaccaa/pictures/raw/master/img2022/0186795d843896a8012060be1cbe75.jpg
pos: right
size: h-260px mx-15px
id: 2
---

关于“一墩难求”的问题，北京冬奥组委新闻发言人赵卫东1月6日表示目前相关部门正在加大协调力度增加“冰墩墩”供应量。

“北京冬奥会的特许商品，将至少持续销售到今年6月底，可以满足广大消费者的需要。”有知情人士告诉《证券日报》记者，“相关北京冬奥会的特许生产企业正在积极投入到产品的生产当中，尽全力在保障产品质量的前提下，早日将产品投放市场”。

---
id: 2
---

“鉴于上述冬奥特许商品近期受到广大消费者的热捧，公司已经组织工厂全面开工生产，全力协调产能配给，保障冬奥会特许商品的供应，尽最大努力满足广大消费者的需求。”元隆雅图亦在投资者互动平台上表示。

```markdown
---
layout: imagex
image: https://gitee.com/isaaccaa/pictures/raw/master/img2022/0186795d843896a8012060be1cbe75.jpg
pos: right
size: h-260px mx-15px
---
```

---
id: 3
---

# What is Slidev?

Slidev is a slides maker and presenter designed for developers, consist of the following features

- 📝 **Text-based** - focus on the content with Markdown, and then style them later
- 🎨 **Themable** - theme can be shared and used with npm packages
- 🧑‍💻 **Developer Friendly** - code highlighting, live coding with autocompletion
- 🤹 **Interactive** - embedding Vue components to enhance your expressions
- 🎥 **Recording** - built-in recording and camera view
- 📤 **Portable** - export into PDF, PNGs, or even a hostable SPA
- 🛠 **Hackable** - anything possible on a webpage

<br>
<br>

Read more about [Why Slidev?](https://sli.dev/guide/why)

---
id: 3
---

# Navigation

Hover on the bottom-left corner to see the navigation's controls panel

### Keyboard Shortcuts

|     |     |
| --- | --- |
| <kbd>space</kbd> / <kbd>tab</kbd> / <kbd>right</kbd> | next animation or slide |
| <kbd>left</kbd>  / <kbd>shift</kbd><kbd>space</kbd> | previous animation or slide |
| <kbd>up</kbd> | previous slide |
| <kbd>down</kbd> | next slide |

---
layout: image-right
image: 'https://source.unsplash.com/collection/94734566/1920x1080'
---

# Code

Use code snippets and get the highlighting directly!

```ts
interface User {
  id: number
  firstName: string
  lastName: string
  role: string
}

function updateUser(id: number, update: Partial<User>) {
  const user = getUser(id)
  const newUser = {...user, ...update}  
  saveUser(id, newUser)
}
```

---
layout: center
class: "text-center"
---

# Learn More

[Documentations](https://sli.dev) / [GitHub Repo](https://github.com/slidevjs/slidev)
