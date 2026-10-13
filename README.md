# MuYun Companion

> Reading & writing aids for Obsidian — the companion plugin of the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun). Pure local computation, no network, no telemetry.
> Obsidian 阅读/写作增强插件——[MuYun 慕云主题](https://github.com/GarrettFynn/obsidian-muyun)的配套插件。纯本地计算、零联网、零遥测。

**[English](#overview)** · [中文](#概述-overview)

---

## Overview 概述

**EN** — MuYun Companion adds what a pure-CSS theme cannot do: ten reading & writing aids, each with an independent toggle. It was designed alongside the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun) and looks best with it, but it styles itself through Obsidian's standard CSS variables (with fallback values), so it works under any theme. Everything is computed locally — no network access, no telemetry; your reading data never leaves `data.json` in your vault.

**中文** — MuYun Companion 补足纯 CSS 主题做不到的部分：十项阅读/写作增强，每项可独立开关。它随 [MuYun 主题](https://github.com/GarrettFynn/obsidian-muyun)一同设计、在 MuYun 下观感最佳，但样式全部走 Obsidian 标准 CSS 变量（自带兜底值），任何主题下均可使用。所有计算纯本地——零联网、零遥测，阅读数据只存在库内 `data.json`。

## Features 功能

| Feature 功能 | Default 默认 | What it does 说明 |
| --- | --- | --- |
| Reading progress bar 阅读进度条 | On 开 | 4px gradient bar at the top, follows scrolling. 顶部 4px 渐变细条，随滚动显示读到哪了 |
| Edge minimap 侧缘小地图 | On 开 | Heading dot-rail on the right; tracks scrolling (reading) or cursor (live preview); click to jump; read trail persisted. 右缘标题点轨，阅读态随滚动、编辑态随光标，点击跳转，已读轨迹持久化 |
| Reading spotlight 阅读聚光灯 | Off 关 | Current section lit, others dimmed — scroll-driven in reading view, cursor-driven in live preview. 当前小节全亮其余降透明：阅读态跟滚动、实时预览跟光标 |
| Resume reading 续读记忆 | On 开 | Reopens each note at the position you left (LRU 400 notes). 每篇笔记记住上次读到的位置 |
| Heading breadcrumb 标题面包屑 | On 开 | Status bar shows `Chapter › Section` and updates as you scroll. 状态栏实时显示当前章节路径 |
| Reading time 阅读时长估计 | On 开 | "≈N min" in the status bar (400 CJK chars/min). 状态栏显示预计阅读分钟数 |
| Reading stats 阅读统计 | Off 关 | Local daily/per-note time tracking, daily goal, weekly report, 12-week heatmap. 本地记录每日/每篇阅读时长、每日目标、周报与 12 周热图 |
| Copy section link 复制小节链接 | — | Command that copies `[[Note#Section]]` to the clipboard. 一键复制当前小节的维基链接 |
| Paragraph focus 段落聚焦 | Off 关 | In live preview, the paragraph around the cursor stays lit, the rest fades (writing mode). 光标所在段落全亮、其余淡出（写稿模式） |
| Typewriter scrolling 打字机滚动 | Off 关 | Keeps the cursor at the upper third of the screen, smooth-eased. 光标始终保持在屏幕上三分之一处（平滑滚动） |

## Requirements 要求

- Obsidian **1.4.0** or newer. 需要 Obsidian 1.4.0 及以上。
- Optional: the [MuYun theme](https://github.com/GarrettFynn/obsidian-muyun) (visually tuned pairing — the plugin works with any theme). 可选：MuYun 主题（为插件调校的视觉搭配，不装也可用）。

## Install 安装

- **Community directory 社区目录（推荐）**：Settings → Community plugins → Browse → search **"MuYun Companion"**（目录搜索同步有数小时延迟）。设置 → 第三方插件 → 浏览 → 搜索 MuYun Companion。
- **Manual 手动安装**：Download `main.js`, `manifest.json`, `styles.css` from [Releases](https://github.com/GarrettFynn/muyun-companion/releases), put them into `<vault>/.obsidian/plugins/muyun-companion/`, then enable **MuYun Companion** in Settings → Community plugins and press `Ctrl+R` once. 从 [Releases](https://github.com/GarrettFynn/muyun-companion/releases) 下载三件套，放入库目录 `.obsidian/plugins/muyun-companion/`，在第三方插件设置中启用后按一次 `Ctrl+R`。
- **BRAT（自动更新）**：Install [BRAT](https://github.com/TfTHacker/obsidian42-brat) → Add Beta plugin → `GarrettFynn/muyun-companion`. 用 BRAT 添加 Beta 插件即可获得后续自动更新。
- Optional: install [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) — together with the MuYun theme it unlocks 12 companion options + 24 theme options. 可选：安装 Style Settings，配合 MuYun 主题解锁 12 项插件参数与 24 项主题参数。

## Settings 设置

Every feature has its own toggle under Settings → MuYun Companion; spotlight dimness and stats options are adjustable there too. 所有功能在 设置 → MuYun Companion 下独立开关，聚光灯暗度与统计参数也可调。

## FAQ 常见问题

- **Spotlight doesn't move in live preview? 实时预览聚光灯不动？** It follows the **cursor**, not scrolling, in that mode; scroll-driven behavior lives in reading view. 实时预览下它跟随**光标**而非滚动；滚动跟随在阅读视图里。
- **Progress bar invisible? 进度条不显示？** Markdown views only, and only when content exceeds one screen. 仅 Markdown 视图且内容超过一屏时出现。
- **Mobile? 移动端？** Installable on mobile, but status-bar items (breadcrumb / reading time) are desktop-oriented and mobile behavior is not extensively tested — feedback welcome. 移动端可安装，但状态栏类功能（面包屑/阅读时长）面向桌面，移动端未经充分测试，欢迎反馈。

## Privacy 隐私

Pure local computation — no network access, no telemetry. Since 0.5.1, all plugin data (settings, reading stats, resume positions, trails) persists to the plugin's `data.json` inside your vault — isolated per vault and included in vault backups; data from ≤0.5.0 (stored in localStorage) migrates automatically on first launch. 纯本地计算——零联网零遥测。0.5.1 起全部插件数据（设置/阅读统计/续读位置/轨迹）存于库内插件的 `data.json`，按库隔离、随库备份；≤0.5.0 的旧数据（localStorage）首次启动时自动迁入。

## License

MIT © [GarrettFynn](https://github.com/GarrettFynn)（甘慕云）
