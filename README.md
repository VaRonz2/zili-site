# 字里 · 网页

字里 App 的公开网站，网址 https://zilily.app （GitHub Pages）。

- `index.html`：首页（封面墙 + 点词演示 + 截图 + 怎么装 TestFlight）。单文件，样式和脚本都在里面。
- `ime.html`：字里输入法（iPhone 键盘）介绍页：打字演示（候选和释义是输入法引擎真实打出来的）+ 截图 + 隐私承诺 + 怎么开始。`ime-privacy.html`：字里输入法的隐私政策（手写，App Store 填这个网址）。`img/shot-ime-*.jpg`：输入法真实截图（模拟器；`shot-ime-light.jpg` 是首屏用的浅色模式，标注位置对着它量的，换截图要重量 `ime.html` 里的 `--x` / `top`）。
- `support.html`：帮助页。`privacy.html`：隐私政策，由 App 仓库 `mobile/scripts/build_privacy.ts` 生成，不要在这里手改。
- `img/covers/`：App 文章封面（来自 Supabase 的 covers 桶，缩到 560 宽）；`img/shot-*.jpg`：App 真实截图（模拟器，深色模式）。
- `fonts/wenkai-medium.woff2`：霞鹜文楷（OFL）按页面用到的字裁出来的子集。改了标题文字要重新裁（2026-11-17 起把 index / ime / support 三页全文都裁进去），否则新字会退回系统楷体：
  `pyftsubset LXGWWenKai-Medium.ttf --text-file=<页面文字> --flavor=woff2 --output-file=fonts/wenkai-medium.woff2`
- 设计规则见 `DESIGN.md`。
