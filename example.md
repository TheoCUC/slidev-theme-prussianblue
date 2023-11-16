---
theme: ./
contents: 
  - About
  - Slidev
  - Demo
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
contents: 
  - About
  - Image
  - Slidev
```

To highlight the section being demonstrated, you need to add the following code to the front of the page:

```
---
id: 1
---
```

To give it a Keynote-like appearance, I used the styles for headings and text in [@slidev/theme-apple-basic](https://github.com/slidevjs/themes/tree/main/packages/theme-apple-basic). 


---
id: 2
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

Read more about [Why Slidev?](https://sli.dev/guide/why)

---
id: 2
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
id: 3
---

# 最优控制

随着技术的发展和生产的需要, 对生产过程的要求也在逐渐提高. 所以除了要求闭环系统稳定、安全地运行外, 还会提出一些附加的要求, 譬如**过渡时间尽量短、运动过程中消耗的能量尽量少、生产成本尽量低而收益尽量大**等. 这些附加的要求也是表示系统性能的指标, 它们可以用某种比之前的误差积分指标更复杂的函数形式来描述. 

最优控制研究的主要问题是:根据已建立的被控对象的数学模型, 选择一个容许的**控制律**, 使得被控对象按预定要求运行, 并使给定的某一性能指标达到极小值(或极大值). 

从数学观点来看, 最优控制研究的问题是求解一类带有约束条件的泛函极值问题, 属于变分学的范畴。然而, 经典变分理论只能解决控制无约束, 即容许控制属于开集的一类, 实际所遇到的控制多数是有约束的. 20实际50年代出现了现代变分理论, 其中最常用的方法是**极小值**(极大值)**原理**和**动态规划**. 


---
id: 3
---

# 最优控制问题

---
id: 3
---

# 最优控制问题的数学描述

最优控制问题应包含以下几个方面的内容: 

* **被控系统的数学模型**    一个集总参数的系统可以用状态方程
$$
\dot{ {\bm x}} = {\bm f} [{\bm x}(t), {\bm u}(t), t]
$$
表示, 对于线性定常系统可以表示为:
$$
    \dot{ {\bm x}} (t) = {\bm A} {\bm x}(t) + {\bm B} {\bm u} (t). 
$$
这样的方程表示在控制 ${\bm u}(t)$ 的作用下, 系统从一个状态转移到另一个状态, 或者说从 $n$ 维状态空间中的一个点转移到另一个点. 



---
id: 3
---

## 最优控制问题的数学描述

* **边界条件和目标集**    最优控制中的初始时刻 $t_0$ 和初始状态(**初态**) ${\bm x}(t_0)$ 通常是已知的, 而末端时刻 $t_f$ 和末端状态(**末态**) ${\bm x}(t_f)$ 则不一定. 
末态即控制过程要达到的目标, 这个目标可能是一个给定的固定点, 也可能是满足条件的一个区域. 
满足末态约束条件的状态集合被称为**目标集**, 计为 $M$ .  当目标集为一个点时, 控制问题被称为**固定终端问题**.  
末态范围的约束可以用末态约束方程或不等式描述:
$$
{\bm g}[{\bm x}(t_f), t_f] = 0 \quad  or \quad {\bm h}[{\bm x}(t_f), t_f] \leq 0
$$

---
id: 3
---

## 例题

求泛函 $J=\int^1_0 x^2 (t) {\rm d}t$ 的变分. 

<v-click>

## 解

$$
    \begin{aligned}
        \Delta J &= \int ^1 _0 [x+ \delta x]^2 {\rm d}t - \int ^1 _0 x^2 {\rm d}t   \\
        &= \int ^1 _0 [x^2+ 2 x \delta x + (\delta x)^2] {\rm d}t - \int ^1 _0 x^2 {\rm d}t   \\
        &= \int ^1 _0 2 x \delta x  {\rm d}t - \int ^1 _0 (\delta x)^2 {\rm d}t.     \\
        \delta J &= \int^1 _0 2 x(t) \delta x {\rm d} t. 
    \end{aligned}
$$

</v-click>