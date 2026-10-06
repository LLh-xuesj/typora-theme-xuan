# 宣纸 Xuan · Typora 主题

一个为**中文长文写作**准备的 Typora 浅色主题：宣纸底、墨色字、朱砂点缀，正文用霞鹜文楷，西文用放大过的 EB Garamond，中文加粗走真字重而不是浏览器合成的假粗体。

## 安装

1. 下载整个仓库（**Code → Download ZIP**，或把 `xuan.css` 与 `xuan/` 文件夹一起拷下来）——**两者必须放在同一层**，CSS 靠 `./xuan/EBGaramond-*.ttf` 取字体。
2. 把 `xuan.css` 和 `xuan/` 放进 Typora 的主题目录：

   | 系统 | 主题目录 |
   | --- | --- |
   | Windows | `%APPDATA%\Typora\themes` |
   | macOS | `~/Library/Application Support/abnerworks.Typora/themes` |
   | Linux | `~/.config/Typora/themes` |

3. 重启 Typora，或在窗口里按 `Ctrl` / `Cmd` + `Shift` + `F5` 重载主题，然后在「主题」菜单里选 **xuan**。

装好之后大概长这样：

```
themes/
├── xuan.css
└── xuan/
    ├── EBGaramond-Regular.ttf
    ├── EBGaramond-Italic.ttf
    ├── EBGaramond-Medium.ttf
    ├── EBGaramond-MediumItalic.ttf
    ├── EBGaramond-SemiBold.ttf
    ├── EBGaramond-SemiBoldItalic.ttf
    └── OFL.txt
```

## 效果

仓库里的 [`demo.md`](demo.md) 就是效果示例：用 Typora 打开它，标题层级、中西混排、引用、行内代码、高亮、代码块、表格、多层列表、任务列表、分隔线都在里面。

## 风格速查

| 元素 | 处理 |
| --- | --- |
| 纸 / 墨 | 宣纸 `#faf7f0` 为底、正文纸 `#fdfbf6`，正文墨色 `#2f2b26` |
| 点缀色 | 朱砂 `#b23a2e`、黛青 `#3c5b6f`、藤黄 `#d6b24a` |
| 正文 | 霞鹜文楷 17px / 行高 1.9 / 两端对齐 |
| 西文 | EB Garamond Medium，用 `@font-face` + `size-adjust` 放大 115%，随主题打包 |
| 加粗 | 西文 Garamond SemiBold + 中文霞鹜文楷 Medium（都是真字面，不合成） |
| 斜体 | 西文用 Garamond 真斜体，中文不做合成倾斜 |
| 标题 | 京华老宋体（单字重），标题字重用常规字重，避免合成加粗糊掉横细竖粗 |
| 代码 | Fira Code（保留连字），代码块内的中文注释回退思源黑体 |
| 表格 | 表头米色底 + 真字重、隔行纸色、悬停时朱砂淡底 |
| 引用 | 朱砂左线 + 渐变底；另支持 GitHub 风格提示块 |
| 打印 / 导出 PDF | 段落首行缩进两个汉字（中文文档规范）；屏幕上默认不缩进 |

## 字体依赖（可选）

**不装也能用**——按字体栈回退到思源宋体 / 系统字体，只是观感会打折。装了更好看的是这三套：

- **霞鹜文楷**（含 Medium 字重）— 正文与加粗
- **京華老宋体**（KingHwaOldSong）— 中文标题
- **Fira Code** — 代码

EB Garamond 已经打包在 `xuan/` 里（SIL OFL 1.1），不需要额外安装。

## 微调

`xuan.css` 末尾有一节「可选微调开关」，共 17 条，**默认全部注释掉**。每条都是「整行删掉本行与结尾那行」即生效，例如：

- 屏幕上也让段落首行缩进两格
- 行宽 / 正文字号 / 行距换一档（默认 980px · 17px · 1.9，另有更疏朗的一档）
- 中式强调：把 `*斜体*` 变成字下加点的着重号
- 线装书式的题签一级标题、宋版书「版框」、去掉「纸张浮起」回到纯平面
- 代码块改深色、关掉 Fira Code 的连字
- 引文改用霞鹜文楷 Light、代码块改用霞鹜文楷等宽
- 西文换 Georgia、数字改用等高（lining）数字、西文字号再放大一档

## 适配

Typora 1.14.x。主题基于 Typora 的文档结构（`#write`）与常规 Markdown 元素编写，跟上 1.14.x 的小版本升级不需要改动。

## 许可

- 主题样式与示例文档：MIT License，见 [`LICENSE`](LICENSE)。
- 随主题打包的 EB Garamond 字体：SIL Open Font License 1.1，见 [`xuan/OFL.txt`](xuan/OFL.txt)，允许随主题一起分发。
- 上面提到、但**没有**打包的中文字体（霞鹜文楷、京华老宋体、Fira Code）各自遵循其原始许可，请从官方渠道安装。
