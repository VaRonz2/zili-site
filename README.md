# 字里 · 网页

字里 App 的公开网站，网址 https://zilily.app （GitHub Pages）。

- `index.html`：首页（封面墙 + 点词演示 + 截图 + 怎么装 TestFlight）。单文件，样式和脚本都在里面。
- `support.html`：帮助页。`privacy.html`：隐私政策，由 App 仓库 `mobile/scripts/build_privacy.ts` 生成，不要在这里手改。
- `img/covers/`：App 文章封面（来自 Supabase 的 covers 桶，缩到 560 宽）；`img/shot-*.jpg`：App 真实截图（模拟器，深色模式）。
- `fonts/wenkai-medium.woff2`：霞鹜文楷（OFL）按页面用到的字裁出来的子集。改了标题文字要重新裁，否则新字会退回系统楷体：
  `pyftsubset LXGWWenKai-Medium.ttf --text-file=<页面文字> --flavor=woff2 --output-file=fonts/wenkai-medium.woff2`
- 设计规则见 `DESIGN.md`。
