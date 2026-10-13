# MuYun Companion

> Reading & writing aids for Obsidian — the companion plugin of the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun). Pure local computation, no network, no telemetry.
> Obsidian 阅读/写作增强插件——[MuYun 慕云主题](https://github.com/GarrettFynn/obsidian-muyun)的配套插件。纯本地计算、零联网、零遥测。

**[English](#overview)** · [中文](#概述-overview)

---

## Overview 概述

**EN** — MuYun Companion adds what a pure-CSS theme cannot do: twelve reading & writing aids, each with an independent toggle. It was designed alongside the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun) and looks best with it, but it styles itself through Obsidian's standard CSS variables (with fallback values), so it works under any theme. Everything is computed locally — no network access, no telemetry; your reading data never leaves `data.json` in your vault.

**中文** — MuYun Companion 补足纯 CSS 主题做不到的部分：十二项阅读/写作增强，每项可独立开关。它随 [MuYun 主题](https://github.com/GarrettFynn/obsidian-muyun)一同设计、在 MuYun 下观感最佳，但样式全部走 Obsidian 标准 CSS 变量（自带兜底值），任何主题下均可使用。所有计算纯本地——零联网、零遥测，阅读数据只存在库内 `data.json`。

## Features 功能

| Feature 功能 | Default 默认 | What it does 说明 |
| --- | --- | --- |
| Reading progress bar 阅读进度条 | On 开 | 4px gradient bar at the top, follows scrolling; thin ticks mark H2 chapter boundaries. 顶部 4px 渐变细条，随滚动显示读到哪了；细刻度标出 H2 章节边界 |
| Edge minimap 侧缘小地图 | On 开 | Heading dot-rail on the right; tracks scrolling (reading) or cursor (live preview); click to jump; read trail persisted. 右缘标题点轨，阅读态随滚动、编辑态随光标，点击跳转，已读轨迹持久化 |
| Reading spotlight 阅读聚光灯 | Off 关 | Current section lit, others dimmed — scroll-driven in reading view, cursor-driven in live preview. 当前小节全亮其余降透明：阅读态跟滚动、实时预览跟光标 |
| Resume reading 续读记忆 | On 开 | Reopens each note at the position you left (LRU 400 notes). 每篇笔记记住上次读到的位置 |
| Reading tray 继续阅读队列 | — | Command or status-bar 📖 click opens recently-read notes with position, progress & last chapter; one click jumps back, 📌 pins, Ctrl+click opens in a new pane. 命令或点击状态栏 📖 打开在读列表（含进度与最近章节），一键回到上次位置，可置顶、Ctrl+点击新窗格打开 |
| Heading breadcrumb 标题面包屑 | On 开 | Status bar shows `Chapter › Section`, updates as you scroll; click any level to jump back to it. 状态栏实时显示当前章节路径，点击任意一级跳回该章节 |
| Reading time 阅读时长 | On 开 | Status bar shows time actually spent on the note: current session · all-time total (needs reading stats on; falls back to a remaining-time estimate otherwise). 状态栏显示真实已读时长「⏱ 本次 · 本篇累计」（需开阅读统计；未开时退回剩余分钟估算） |
| Reading stats 阅读统计 | Off 关 | Local daily/per-note time tracking with hourly distribution & session counts, daily goal, streak (current & best), exportable weekly report, 12-week heatmap. 本地记录每日/每篇阅读时长（含时段分布与会话）、每日目标、连续天数（当前+最佳）、可导出周报与 12 周热图 |
| Copy section link 复制小节链接 | — | Command that copies `[[Note#Section]]` to the clipboard. 一键复制当前小节的维基链接 |
| Paragraph focus 段落聚焦 | Off 关 | In live preview, the paragraph around the cursor stays lit, the rest fades (writing mode). 光标所在段落全亮、其余淡出（写稿模式） |
| Typewriter scrolling 打字机滚动 | Off 关 | Keeps the cursor on an anchor line (top quarter / upper third / middle — adjustable), smooth-eased. 光标保持在可调锚点线处（上四分之一/上三分之一/中线），平滑滚动 |
| Smooth folding 折叠平滑展开 | On 开 | Click a fold arrow in the editor and the section eases open/shut with a short animation (170ms; off under Efficiency mode / reduced motion). 编辑视图点击折叠箭头时短动画平滑收拢展开；效率模式与系统减动效下自动禁用 |

## Requirements 要求

- Obsidian **1.4.0** or newer. 需要 Obsidian 1.4.0 及以上。
- Optional: the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun) (visually tuned pairing — the plugin works with any theme). 可选：MuYun 主题（为插件调校的视觉搭配，不装也可用）。

## Install 安装

- **Community directory 社区目录（推荐）**：Settings → Community plugins → Browse → search **"MuYun Companion"**（目录搜索同步有数小时延迟）。设置 → 第三方插件 → 浏览 → 搜索 MuYun Companion。
- **Manual 手动安装**：Download `main.js`, `manifest.json`, `styles.css` from [Releases](https://github.com/GarrettFynn/muyun-companion/releases), put them into `<vault>/.obsidian/plugins/muyun-companion/`, then enable **MuYun Companion** in Settings → Community plugins and press `Ctrl+R` once. 从 [Releases](https://github.com/GarrettFynn/muyun-companion/releases) 下载三件套，放入库目录 `.obsidian/plugins/muyun-companion/`，在第三方插件设置中启用后按一次 `Ctrl+R`。
- **BRAT（自动更新）**：Install [BRAT](https://github.com/TfTHacker/obsidian42-brat) → Add Beta plugin → `GarrettFynn/muyun-companion`. 用 BRAT 添加 Beta 插件即可获得后续自动更新。
- **Style Settings（optional 可选）**：install it from the community directory — Settings → Community plugins → Browse → search **"Style Settings"** → Install & enable; then open Settings → **Style Settings** → **MuYun** section. Together with the MuYun theme it unlocks 12 companion visual options + 24 theme options (without the MuYun theme this adds nothing). 社区目录安装：设置 → 第三方插件 → 浏览 → 搜索 **Style Settings** 安装并启用，再到 设置 → **Style Settings** → **MuYun** 分组调整；配合 MuYun 主题解锁 12 项插件视觉参数与 24 项主题参数（不装 MuYun 主题则无额外选项）。

## Settings 设置

Every feature has its own toggle under Settings → MuYun Companion; spotlight dimness and stats options are adjustable there too. 所有功能在 设置 → MuYun Companion 下独立开关，聚光灯暗度与统计参数也可调。

## FAQ 常见问题

- **Spotlight doesn't move in live preview? 实时预览聚光灯不动？** It follows the **cursor**, not scrolling, in that mode; scroll-driven behavior lives in reading view. 实时预览下它跟随**光标**而非滚动；滚动跟随在阅读视图里。
- **Folding doesn't animate? 折叠没有动画？** The animation triggers on **clicking the fold arrow** in the editor; folding via keyboard shortcuts stays instant, and it is disabled under Efficiency mode / system reduced-motion. 动画仅由编辑视图**点击折叠箭头**触发；键盘折叠保持瞬时，效率模式与系统「减弱动态效果」下自动禁用。
- **Progress bar invisible? 进度条不显示？** Markdown views only, and only when content exceeds one screen. 仅 Markdown 视图且内容超过一屏时出现。
- **Mobile? 移动端？** Installable on mobile, but status-bar items (breadcrumb / reading time) are desktop-oriented and mobile behavior is not extensively tested — feedback welcome. 移动端可安装，但状态栏类功能（面包屑/阅读时长）面向桌面，移动端未经充分测试，欢迎反馈。

## Privacy 隐私

Pure local computation — no network access, no telemetry. Since 0.5.1, all plugin data (settings, reading stats, resume positions, trails) persists to the plugin's `data.json` inside your vault — isolated per vault and included in vault backups; data from ≤0.5.0 (stored in localStorage) migrates automatically on first launch. 纯本地计算——零联网零遥测。0.5.1 起全部插件数据（设置/阅读统计/续读位置/轨迹）存于库内插件的 `data.json`，按库隔离、随库备份；≤0.5.0 的旧数据（localStorage）首次启动时自动迁入。

## License

MIT © [GarrettFynn](https://github.com/GarrettFynn)（甘慕云）
