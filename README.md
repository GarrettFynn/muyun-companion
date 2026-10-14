# MuYun Companion

> Reading & writing aids for Obsidian — the companion plugin of the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun). Pure local computation, no network, no telemetry.
> Obsidian 阅读/写作增强插件——[MuYun 慕云主题](https://github.com/GarrettFynn/obsidian-muyun)的配套插件。纯本地计算、零联网、零遥测。

**[English](#overview)** · [中文](#概述-overview)

---

## Overview 概述

**EN** — MuYun Companion adds what a pure-CSS theme cannot do: a suite of reading & writing aids, each with an independent toggle. It was designed alongside the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun) and looks best with it, but it styles itself through Obsidian's standard CSS variables (with fallback values), so it works under any theme. Everything is computed locally — no network access, no telemetry; your reading data never leaves `data.json` in your vault.

**中文** — MuYun Companion 补足纯 CSS 主题做不到的部分：一套阅读/写作增强，每项可独立开关。它随 [MuYun 主题](https://github.com/GarrettFynn/obsidian-muyun)一同设计、在 MuYun 下观感最佳，但样式全部走 Obsidian 标准 CSS 变量（自带兜底值），任何主题下均可使用。所有计算纯本地——零联网、零遥测，阅读数据只存在库内 `data.json`。

## Features 功能

**EN** — Grouped by what you're doing; every feature has its own toggle in Settings → MuYun Companion (15 commands are also in the command palette and keyboard-bindable).

**中文** — 按使用场景分组；每项功能都在 设置 → MuYun Companion 里有独立开关（另有 15 条命令可从命令面板调用并绑定快捷键）。

### 读长文时 · While reading a long note

| Feature 功能 | Default 默认 | What you get 效果 |
| --- | --- | --- |
| Reading progress bar 阅读进度条 | On 开 | Always know how far in you are: a thin gradient bar at the top fills as you scroll, with small notches marking each chapter (notches hide automatically in very chapter-heavy notes). 顶部一条细渐变条随滚动填充，一眼看清读到哪；章节处有细刻度（章节过多时自动隐藏） |
| Edge minimap 侧缘小地图 | On 开 | A column of dots on the right edge — one dot per heading. The current section's title floats beside your position with a small pointer arrow, dots you've already passed stay lit, and clicking any dot jumps straight to that section; in very long outlines dots auto-condense so every heading keeps one. 右缘一列圆点，一个标题一个点：当前小节标题带小箭头常驻在旁、走过的点亮着、点一下直达该章；超长大纲自动缩点不丢章节 |
| Heading breadcrumb 标题面包屑 | On 开 | The status bar always shows where you are (`Chapter › Section`); click any level to jump back there. 状态栏实时显示「章 › 节」路径，点任意一级跳回 |
| Resume reading 续读记忆 | On 开 | Reopen any note and you're back exactly where you left off (remembers the last 400 notes). 重开笔记自动回到上次读到的位置（记住最近 400 篇） |
| Read marks 已读标记 | On 开 | Finished notes get a green ✓ after their name in the file tree — automatic once you've read past 95% (adjustable), or mark one yourself in the reading tray; marks follow renames. 读过的笔记在文件树里名字后带绿 ✓——读到 95%（可调）自动标，也可在队列手动标；改名后 ✓ 跟着走 |
| Reading spotlight 阅读聚光灯 | Off 关 | Dim everything except the section you're reading, so long pages stop feeling like a wall of text. 当前小节之外全部调暗，长文不再糊成一片 |
| Smooth folding 折叠平滑展开 | On 开 | Click a fold arrow and sections ease open/shut with a short animation instead of snapping (keyboard folding stays instant; auto-off under Efficiency mode / reduced motion). 点击折叠箭头短动画平滑展开收拢（键盘折叠保持瞬时；效率模式/系统减动效下自动关闭） |
| Finish glow 读完柔光 | On 开 | The first time you reach the end of a note, the progress bar softly glows once — a little reward. 每篇笔记首次读到结尾，进度条轻柔发光一次 |

### 回到阅读 · Picking your reading back up

| Feature 功能 | Default 默认 | What you get 效果 |
| --- | --- | --- |
| Reading tray 继续阅读队列 | — | Click 📖 in the status bar to see everything you're in the middle of: search by title/path, group by folder, 📌 pin, ✓ mark finished; each row shows progress, the last chapter you reached and the total time spent on that note (Ctrl+click opens in a new pane). 点击状态栏 📖 列出所有在读笔记：可搜索、按文件夹分组、置顶、标记读完；每行显示进度、读到的章节与本篇累计时长（Ctrl+点击新窗格打开） |

### 写稿时 · While writing

| Feature 功能 | Default 默认 | What you get 效果 |
| --- | --- | --- |
| Paragraph focus 段落聚焦 | Off 关 | The paragraph under your cursor stays bright, everything else fades a little — good for drafting. 光标所在段落保持明亮、其余微暗，适合专注写稿 |
| Typewriter scrolling 打字机滚动 | Off 关 | Keep your typing line anchored (top quarter / upper third / middle — adjustable) so the text you're writing never slides off-screen. 光标行固定在锚点线（上四分之一/上三分之一/中线可调），写到的字不会滑出屏幕 |
| Copy section link 复制小节链接 | — | One command copies `[[Note#Section]]` for wherever you are — handy for cross-referencing. 一条命令复制当前位置的 `[[笔记#小节]]` 链接，交叉引用方便 |

### 回顾阅读 · Looking back at your reading

| Feature 功能 | Default 默认 | What you get 效果 |
| --- | --- | --- |
| Reading stats 阅读统计 | Off 关 | Pure-local time tracking: per-day and per-note reading time, daily goal with a ✓ when you hit it, current & best streaks, which hours of the day you actually read, session counts, a 12-week heatmap, and a weekly report you can export as a note. 开启后纯本地记录：每天/每篇读了多久、每日目标达成打 ✓、连续天数（当前+最佳）、你常在几点读书、会话数、12 周热图、可导出的周报笔记 |
| Reading time 阅读时长 | On 开 | The status bar shows real time spent on the current note — this session · all-time total (needs stats on; otherwise shows a rough remaining-time estimate). 状态栏显示这篇笔记的真实已读时长「⏱ 本次 · 本篇累计」（需开统计；未开时显示剩余分钟估算） |

## Requirements 要求

- Obsidian **1.4.0** or newer. 需要 Obsidian 1.4.0 及以上。
- Optional: the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun) (visually tuned pairing — the plugin works with any theme). 可选：MuYun 主题（为插件调校的视觉搭配，不装也可用）。

## Install 安装

- **Community directory 社区目录（推荐）**：Settings → Community plugins → Browse → search **"MuYun Companion"**（目录搜索同步有数小时延迟）。设置 → 第三方插件 → 浏览 → 搜索 MuYun Companion。
- **Manual 手动安装**：Download `main.js`, `manifest.json`, `styles.css` from [Releases](https://github.com/GarrettFynn/muyun-companion/releases), put them into `<vault>/.obsidian/plugins/muyun-companion/`, then enable **MuYun Companion** in Settings → Community plugins and press `Ctrl+R` once. 从 [Releases](https://github.com/GarrettFynn/muyun-companion/releases) 下载三件套，放入库目录 `.obsidian/plugins/muyun-companion/`，在第三方插件设置中启用后按一次 `Ctrl+R`。
- **BRAT（自动更新）**：Install [BRAT](https://github.com/TfTHacker/obsidian42-brat) → Add Beta plugin → `GarrettFynn/muyun-companion`. 用 BRAT 添加 Beta 插件即可获得后续自动更新。
- **Style Settings（optional 可选）**：install it from the community directory — Settings → Community plugins → Browse → search **"Style Settings"** → Install & enable; then open Settings → **Style Settings** → **MuYun** section. Together with the MuYun theme it unlocks 12 companion visual options + 24 theme options (without the MuYun theme this adds nothing). 社区目录安装：设置 → 第三方插件 → 浏览 → 搜索 **Style Settings** 安装并启用，再到 设置 → **Style Settings** → **MuYun** 分组调整；配合 MuYun 主题解锁 12 项插件视觉参数与 24 项主题参数（不装 MuYun 主题则无额外选项）。

## Settings 设置

Every feature has its own toggle under Settings → MuYun Companion; spotlight dimness, the read-mark threshold and stats options are adjustable there too. 所有功能在 设置 → MuYun Companion 下独立开关；聚光灯暗度、已读阈值与统计参数也可调。

## FAQ 常见问题

- **Spotlight doesn't move in live preview? 实时预览聚光灯不动？** It follows the **cursor**, not scrolling, in that mode; scroll-driven behavior lives in reading view. 实时预览下它跟随**光标**而非滚动；滚动跟随在阅读视图里。
- **Folding doesn't animate? 折叠没有动画？** The animation triggers on **clicking the fold arrow** in the editor; folding via keyboard shortcuts stays instant, and it is disabled under Efficiency mode / system reduced-motion. 动画仅由编辑视图**点击折叠箭头**触发；键盘折叠保持瞬时，效率模式与系统「减弱动态效果」下自动禁用。
- **Progress bar invisible? 进度条不显示？** Markdown views only, and only when content exceeds one screen. 仅 Markdown 视图且内容超过一屏时出现。
- **Mobile? 移动端？** Installable on mobile, but status-bar items (breadcrumb / reading time) are desktop-oriented and mobile behavior is not extensively tested — feedback welcome. 移动端可安装，但状态栏类功能（面包屑/阅读时长）面向桌面，移动端未经充分测试，欢迎反馈。

## Privacy 隐私

Pure local computation — no network access, no telemetry. Since 0.5.1, all plugin data (settings, reading stats, resume positions, trails) persists to the plugin's `data.json` inside your vault — isolated per vault and included in vault backups; data from ≤0.5.0 (stored in localStorage) migrates automatically on first launch. 纯本地计算——零联网零遥测。0.5.1 起全部插件数据（设置/阅读统计/续读位置/轨迹）存于库内插件的 `data.json`，按库隔离、随库备份；≤0.5.0 的旧数据（localStorage）首次启动时自动迁入。

## License

MIT © [GarrettFynn](https://github.com/GarrettFynn)（甘慕云）
