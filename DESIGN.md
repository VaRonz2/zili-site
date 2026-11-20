---
name: 字里 Zilily 网站
description: 墨蓝夜色上的一墙故事封面，纸白卡片承载文字，点词即见中文
colors:
  night: "#16181D"
  paper: "#F6F6F4"
  sheet: "#FFFFFF"
  ink: "#16181D"
  soft: "#5A5F68"
  line: "#DEDFE2"
  on-night-soft: "#B6BCC8"
  ink-blue: "#1E3F8F"
  ink-blue-deep: "#17306E"
  ink-blue-lift: "#3A5FC0"
  ink-blue-lift-hover: "#4A6FD0"
  blue-mist: "#C9D5F2"
  word-yellow: "#FFE58A"
  word-yellow-hover: "#FFF2BF"
  bezel: "#0B0D11"
typography:
  display:
    fontFamily: "WenKai, Kaiti SC, STKaiti, serif"
    fontSize: "clamp(40px, 5.2vw, 60px)"
    fontWeight: 600
    lineHeight: 1.16
    letterSpacing: "0.01em"
  headline:
    fontFamily: "WenKai, Kaiti SC, STKaiti, serif"
    fontSize: "clamp(32px, 4vw, 48px)"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "0.01em"
  title:
    fontFamily: "WenKai, Kaiti SC, STKaiti, serif"
    fontSize: "22px"
    fontWeight: 600
    lineHeight: 1.4
  body:
    fontFamily: "-apple-system, PingFang SC, Hiragino Sans GB, Microsoft YaHei, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.75
  reading:
    fontFamily: "Georgia, Times New Roman, serif"
    fontSize: "20px"
    fontWeight: 400
    lineHeight: 1.9
  word:
    fontFamily: "Georgia, Times New Roman, serif"
    fontSize: "36px"
    fontWeight: 700
    lineHeight: 1.2
  label:
    fontFamily: "-apple-system, PingFang SC, Hiragino Sans GB, Microsoft YaHei, system-ui, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.5
rounded:
  tag: "6px"
  chip: "12px"
  cover: "14px"
  card: "24px"
  panel: "28px"
  phone: "36px"
  pill: "999px"
spacing:
  gutter: "clamp(20px, 4.5vw, 64px)"
  section: "clamp(72px, 10vw, 128px)"
  container: "1180px"
  sheet-pad: "28px 30px 30px"
components:
  button-primary:
    backgroundColor: "{colors.ink-blue}"
    textColor: "{colors.sheet}"
    rounded: "{rounded.cover}"
    padding: "18px 28px"
  button-primary-hover:
    backgroundColor: "{colors.ink-blue-deep}"
  button-primary-on-night:
    backgroundColor: "{colors.ink-blue-lift}"
    textColor: "{colors.sheet}"
    rounded: "{rounded.cover}"
    padding: "18px 28px"
  button-primary-on-night-hover:
    backgroundColor: "{colors.ink-blue-lift-hover}"
  chip-action:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    rounded: "{rounded.chip}"
    padding: "12px 16px"
  chip-action-primary:
    backgroundColor: "{colors.ink-blue}"
    textColor: "{colors.sheet}"
    rounded: "{rounded.chip}"
    padding: "12px 16px"
  tag-category:
    backgroundColor: "{colors.sheet}"
    textColor: "{colors.ink}"
    rounded: "{rounded.pill}"
    padding: "6px 14px"
  word-tap-selected:
    backgroundColor: "{colors.word-yellow}"
    textColor: "{colors.ink}"
    rounded: "4px"
  card-story:
    backgroundColor: "{colors.sheet}"
    rounded: "{rounded.card}"
    padding: "clamp(22px, 3vw, 36px)"
  panel-hero:
    backgroundColor: "{colors.paper}"
    rounded: "{rounded.panel}"
    padding: "clamp(28px, 4vw, 48px)"
  cover-tile:
    rounded: "{rounded.cover}"
---

# Design System: 字里 Zilily 网站

## Overview

**Creative North Star: "夜里的书墙"**

网站沿用字里 App 的墨蓝主题：夜色墨底上铺满 App 里真实的文章封面插画，文字放在纸白卡片里，像从书墙上抽出一页来读。页面节奏是夜 / 纸交替：第一屏和安装段在夜色里，读词演示和书架在纸色里。

颜色极省：墨蓝只负责「可以按、已选中、焦点」，划词黄只属于「被点到的那个词」。图像只用 App 自己的东西（封面、截图），不用图库图或装饰插画。字体分三种声音：标题用霞鹜文楷（中文，有手写温度），说明用系统黑体，英文原文用衬线，让人一眼分清「这是要读的英文」。

`ime.html`（字里输入法）的首屏按 Zhu 2026-11-17 给的参考图做：整屏墨蓝底，浅色模式的真实截图手机居中，左右各两条标注（划词黄的点和线指向截图里的具体位置，标题系统黑体 800），两角各一个 7% 白的大字（打 / 学），左下是白色主按钮和黑体大标题；窄于 1180px 时标题移到上面、标注排在手机下面不画线。这是一处例外：墨蓝做大面积底色、划词黄做标注点线，只限这个首屏。往下沿用同一套、纸色打字演示、夜色截图段、纸色承诺、夜色「怎么开始」。演示里的示意键盘（ime.html 的对比和打字演示、首页 `index.html` 的「打字的时候，也在学英文。」对比段）是唯一用到橙色（`#B85600`）的地方：它照搬键盘里「字里」标记的颜色，比系统橙深一档以保证网页上的对比度；不要在别处用橙色。

`support.html`、`privacy.html` 和 `ime-privacy.html` 是素净的阅读页，只共用纸色和系统黑体，不属于这套视觉世界的完整表达。

**Key Characteristics:**
- 夜色墨底 + 纸白卡片，两层对比承担全部层次
- 16:9 圆角封面是唯一的装饰素材，可倾斜、可缓慢平移
- 墨蓝只给动作和选中，划词黄只给词
- 文楷标题 / 黑体说明 / 衬线英文，三种字体各司其职

## Colors

一夜一纸，一蓝一黄：中性色铺底，两种强调色各守一个职责。

### Primary
- **墨蓝**（`ink-blue`）：主按钮、主操作 chip、焦点框、分类标签悬停描边。按下 / 悬停加深到 **深墨蓝**（`ink-blue-deep`）。
- **提亮墨蓝**（`ink-blue-lift`，悬停 `ink-blue-lift-hover`）：夜色背景上的主按钮。原墨蓝在夜底上对比不够，所以夜段换用这一档。
- **雾蓝**（`blue-mist`）：夜底上的辅助字色，品牌英文名「Zilily」和安装步骤的大号数字。

### Secondary
- **划词黄**（`word-yellow`）：被点中的词的底色，以及全站 `::selection`。悬停预示用 **浅划词黄**（`word-yellow-hover`）。

### Neutral
- **夜色墨**（`night`）：第一屏、截图段、安装段、页脚的底色，也是 `theme-color`。
- **纸色**（`paper`）：页面主背景、首屏文字卡、chip 和生词标签的底。
- **白纸**（`sheet`）：纸色上再浮起一层的卡片（故事卡、释义卡、分类标签）。
- **墨色**（`ink`）：正文字色，与夜色墨同值。
- **灰墨**（`soft`）：说明、元信息、次要文字。
- **细线**（`line`）：分隔线和标签描边。
- **夜底浅灰**（`on-night-soft`）：夜色背景上的说明文字。
- **机身黑**（`bezel`）：手机截图的边框和底。

### Named Rules
**The 一词一黄 Rule.** 划词黄只出现在被点中的词和文本选区上，不做按钮、徽标或强调底色。

**The 蓝即可按 Rule.** 墨蓝只用于能按的东西、已选中的状态和焦点框；不用于标题、正文强调或装饰。

## Typography

**Display Font:** 霞鹜文楷 Medium，自托管子集 `fonts/wenkai-medium.woff2`（OFL），回退 Kaiti SC / STKaiti
**Body Font:** 系统黑体（-apple-system / PingFang SC）
**Reading Font:** Georgia（英文原文、英文标题、封面说明）

**Character:** 文楷给中文标题一点手写书卷气，黑体负责清楚说明，衬线让英文看起来像书页而不是界面。

### Hierarchy
- **Display**（`display`）：首屏卡片大标题，一页一个。手机端固定 34px。
- **Headline**（`headline`）：每段的段标题，句号结尾的完整短句。
- **Title**（`title`，22–26px 文楷 600）：书架名、承诺条目、安装步骤、截图说明的小标题。
- **Body**（`body`）：说明文字，手机端 16px；段落说明限宽 36em。
- **Reading**（`reading`）：故事原文，限宽 65ch，手机端 18px。英文标题用同一衬线 700。
- **Word**（`word`）：释义卡里的单词，手机端 28px。
- **Label**（`label`）：元信息、「免费 · iPhone / iPad」这类小字。封面上的英文小标签用 12px 衬线 700。

### Named Rules
**The 先裁字再改标题 Rule.** 文楷是按页面用字裁出的子集。任何文楷文字（h1–h3、品牌名、标题样式的 `<b>`、步骤数字）改动后，必须用 `pyftsubset` 重新裁子集，否则新字会退回系统楷体。

**The 英文用衬线 Rule.** 页面上供阅读的英文（原文、篇名、封面标签）一律用衬线，并标 `lang="en"`；界面说明不用衬线。

## Layout

单列分段，每段左右留白 `gutter`、上下 `section`，内容收在 `container` 宽度内。首屏是满高的夜色舞台（最高 980px），封面墙 6 列网格整体旋转 -4° 并超出四边，中间径向压暗，纸色卡片居中（最宽 640px）；手机端卡片沉到底部，墙改 3 列。

读词演示是左宽右窄两栏（1.15 : 0.85），释义卡 `sticky` 跟随；900px 以下改单栏，释义卡吸在屏幕底部。截图三张错落下沉（0 / 72 / 144px），手机端改横向滑动。书架是横向滚动的封面轨道，带 scroll-snap。

断点：900px（两栏变单栏）、600px（手机排版）。

## Elevation & Depth

层次主要靠夜 / 纸 / 白三层底色的对比，阴影只用在「浮起来的纸」上，全部是柔和的大半径投影，没有硬边偏移阴影。

### Shadow Vocabulary
- **首屏卡片**（`0 30px 80px rgba(0,0,0,.45)`）：夜底上托起纸卡。
- **释义卡**（`0 18px 48px rgba(22,24,29,.12)`）：纸底上浮起的交互卡。
- **故事卡**（`0 2px 10px rgba(22,24,29,.06)`）：几乎贴地，只是让白卡和纸底分开。
- **手机截图**（`0 30px 60px rgba(0,0,0,.4)`）：夜底上的设备。

### Named Rules
**The 纸才有影 Rule.** 只有承载文字的纸卡和截图有投影；封面、标签、按钮都是平的。

## Shapes

圆角统一偏大、柔和：封面和按钮 14px，chip 12px，卡片 24px，首屏卡 28px（手机 22px），手机截图 36px，分类标签全圆。封面始终 16:9 裁切（故事头图例外，16:7）。描边只用 1–1.5px 细线；可点的词用 2px 点状下划线提示。

## Components

### Buttons
- **Shape:** 圆角 14px，图标在文字右侧（18px 描线箭头 SVG）。
- **Primary:** 墨蓝底白字，18px / 700，`18px 28px` 内距；手机端撑满宽。
- **Hover / Focus:** 悬停加深为深墨蓝，按下下移 1px，过渡 0.2s `cubic-bezier(.16,1,.3,1)`；焦点为 3px 墨蓝外框（夜底上改白色）。
- **夜底变体:** 换用提亮墨蓝。

### Chips
- **Action chip:** 纸色底墨字，15px / 700，圆角 12px，带 16px 描线 SVG 图标。主操作版为墨蓝底白字。
- **分类标签:** 白底细线描边全圆，14px / 700；悬停描边和文字变墨蓝。手机端单行横滑。

### Cards / Containers
- **首屏纸卡:** 纸色、圆角 28px、大投影，内含标题、说明、分类标签、主按钮。
- **故事卡:** 白底、圆角 24px、头图满宽，内文为衬线原文。
- **释义卡:** 白底、圆角 24px，单词（衬线 700）→ 音标（灰墨）→ 中文释义 → 操作 chip；切词时内容 0.45s 轻弹入。

### Navigation
只有品牌名（文楷 24px + 雾蓝小字 Zilily）和两个文字链接（帮助、隐私政策），浮在首屏夜色上，悬停变白加下划线。页脚在夜色里重复链接和联系邮箱。

### 可点的词（Signature）
英文原文里的词是 `<button>`：默认 2px 点状灰下划线，悬停浅划词黄，选中划词黄底、去掉下划线，并同步更新释义卡。这是网站与 App 共用的核心交互，新页面要演示查词时照此复用。

### 封面墙（Signature）
真实封面 16:9、圆角 14px，网格整体 -4° 倾斜，90 秒线性往返缓慢平移；少数封面左下角压一枚白底衬线英文篇名。上面叠径向暗角，保证中间文字可读。`prefers-reduced-motion` 下停止平移。安装段底部用 28% 透明度的同款墙作收尾。

## Do's and Don'ts

### Do:
- **Do** 用 App 的真实封面和真实截图作为全部图像素材，封面保持 16:9、圆角 14px。
- **Do** 把文字放在纸色或白色卡片上，夜色只做舞台和底色。
- **Do** 夜底上的主按钮用提亮墨蓝，焦点框改白色。
- **Do** 改动任何文楷文字后重新裁字体子集。
- **Do** 所有动画在 `prefers-reduced-motion: reduce` 下关闭。
- **Do** 图标用内联描线 SVG（描边 2–2.4，圆头）。

### Don't:
- **Don't** 把划词黄用在词和选区以外的地方。
- **Don't** 把墨蓝用于标题、装饰或大面积底色。
- **Don't** 用硬边偏移阴影或给封面、按钮加投影。
- **Don't** 用文字字符或 emoji 充当图标。
- **Don't** 用 App 之外的图库图、装饰插画或渐变色块代替 App 封面。
