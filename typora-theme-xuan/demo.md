# 宣纸 Xuan

> 一套为中文长文写作准备的 Typora 浅色主题。这份文档本身就是它的效果示例。

## 一、中西混排

中文正文用**霞鹜文楷**，西文交给 EB Garamond——两者摆在同一个段落里，行高与字重都不会打架：

> The craft of making *xuan* paper has been passed down for more than a thousand years. 宣纸的寿命令人吃惊，所谓「纸寿千年」，说的是它不蛀、不腐、不脆。Ink sits on its surface rather than sinking into it, which is why 墨色在宣纸上总能留住那一点点**洇开**的呼吸。

行内代码写成 `typora-theme-xuan`，链接是[这样的](https://support.typora.io/About-Themes/)，高亮写作 ==宣纸 #faf7f0==。

## 二、标题与层级

### 三级标题：黛青方点

#### 四级标题：藤黄斜标

##### 五级标题

###### 六级标题

## 三、代码

```js
// 中文注释与西文代码混排时，注释退回思源黑体
function ink(paper, stroke) {
  return paper.hold(stroke, { diffusion: 0.18 });  // 交界处那一点毛边
}
```

## 四、表格与列表

| 元素 | 处理 |
| --- | --- |
| 纸 / 墨 | 宣纸 `#faf7f0` 底，正文墨 `#2f2b26` |
| 标题 | 京华老宋体（单字重 400） |
| 引用 | 朱砂左线 + 渐变底 |
| 打印 | 导出 PDF 时段落首行缩进两字符 |

- 无序列表第一层
  - 第二层
    - 第三层
- [x] 已完成的待办
- [ ] 未完成的待办

1. 有序列表
2. 第二项

---

*最后一步：文件末尾的「可选微调开关」一节，取消注释即可调首行缩进、行宽、字号。*
