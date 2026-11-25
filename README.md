# Notion Widgets

Custom widgets built for the **Dark XP Student Planner** Notion template.
Hosted on GitHub Pages — embed using Notion's `/embed` block.

---

## 🔗 Widget Links

| Widget | Link |
|--------|------|
| 🌦 Weather | https://adrisol-studio.github.io/notion-widgets/widget-weather.html |
| 🕰 Flip Clock | https://adrisol-studio.github.io/notion-widgets/widget-flip-clock.html |
| ⏱ Pomodoro Timer | https://adrisol-studio.github.io/notion-widgets/widget-pomodoro.html |
| 🌄 Scenic Pomodoro | https://adrisol-studio.github.io/notion-widgets/widget-pomodoro-scenic.html |
| 🎵 Music Player | https://adrisol-studio.github.io/notion-widgets/widget-music-player.html |
| 🌧 Matrix Rain | https://adrisol-studio.github.io/notion-widgets/widget-matrix.html |
| 🗓 Timetable | https://adrisol-studio.github.io/notion-widgets/widget-timetable.html |

---

## 📐 Recommended Embed Sizes

| Widget | Mode | Width | Height |
|--------|------|-------|--------|
| Weather | Full (hourly + 7-day) | 520px | 350px |
| Weather | Compact (current only) | 340px | 190px |
| Flip Clock | Standard (4-tile) | 500px | 220px |
| Flip Clock | Compact (2-tile) | 320px | 200px |
| Pomodoro Timer | — | 420px | 620px |
| Scenic Pomodoro | — | 640px | 360px |
| Music Player | Full (Spotify / YouTube) | 420px | 460px |
| Music Player | Compact (Spotify only) | 420px | 140px |
| Matrix Rain | — | any | any |
| Timetable | Full (Today / Week) | 520px | 600px |
| Timetable | Narrow | 340px | 520px |

---

## 📁 Files

- `widget-weather.html` — Live weather widget powered by Open-Meteo (free, no API key, CORS-enabled). Settings include:
  - **Location** — city search plus a multi-city switcher: save up to 5 cities and switch instantly via tabs on the widget; each city's data is cached so switching back is instant, with a silent background refresh when stale; if a refresh fails (e.g. Wi-Fi drops) the last weather stays on screen and it refreshes again once you're back online
  - **Units** — °C or °F
  - **Forecast Days** — 3, 5, or 7 day outlook
  - **Layout** — Full (current conditions + scrollable hourly strip + daily forecast) or Compact (current conditions only)
  - **Day Labels** — Short (Mon) or Full (Monday)
  - **Theme** — Light or Dark, with per-theme background and text colour palettes plus full HSV custom colour pickers
  - **Display toggles** — Ambient gradient background, Hourly strip, Air quality (AQI), Feels-like temp, Rain chance, Forecast rain %, Dates, Condition text, Animated icons, Greyscale icons
  - **Zoom** — 50 – 160 % scale; the widget always shrinks to fit its embed, so nothing (including the gear) is ever cut off
  - **Adapts to the device** — works in the Notion mobile app: bigger tap targets on touchscreens, slightly narrower tiles on phones so 5–7 days fit, **swipe left / right to switch saved cities** (also in Compact), and a settings popup that fits small screens
  - **Multi-model consensus** — blends five forecast models (ECMWF, GFS, ICON, GEM, JMA) and takes the median of every value, so one outlier model can't show a false storm
  - **Smart rain detection** — weather codes are reconciled against actual precipitation amount (mm) and cloud cover, so dramatic icons and the rain chip only appear when rain is genuinely forecast
  - Custom inline-SVG weather icons (clear/cloud/fog/drizzle/rain/snow/thunder, day & night variants) with optional CSS animation; location-local clock; "Weather by Open-Meteo" attribution (CC BY 4.0)

- `widget-flip-clock.html` — Flip clock with Standard (4-tile) and Compact (2-tile) modes. Settings include:
  - **Fonts** — Anton, Bebas Neue, Oswald, JetBrains Mono, Squada One, Chakra Petch
  - **Tile presets** — 7 built-in colour presets (Charcoal, Obsidian, Nord, Coffee, Cyber, Gold, Parchment) + custom colour picker
  - **Colour pickers** — separate controls for tile, number, and date/day colours; the **number** and **date** swatch palettes adapt to the selected theme so the colours always contrast the background they sit on (custom colour stays available in both themes)
  - **Motion** — Smooth, Mechanical, Minimal, or Instant flip animation with physics-quality 3D perspective, depth gradient shading, and cast drop shadows on the rotating flap
  - **Theme** — Light or Dark
  - **Format** — 12 HR or 24 HR
  - **Display** — Day & Date, Date only, Day only, or None
  - **Zoom** — 50 – 150 % scale; the clock always shrinks to fit its embed, so the tiles, gear and date are never cut off
  - **Tile presets keep the numbers readable** — picking a light tile (Parchment) under white numbers, or a dark tile under black ones, switches the numbers to black / white
  - **Adapts to the device** — works in the Notion mobile app: bigger tap targets on touchscreens and a settings popup that fits small screens; the time re-syncs instantly when you come back to the tab
  - Responsive layout for narrow embeds; gear icon auto-adapts to tile brightness

- `widget-pomodoro.html` — Pomodoro timer with focus/break cycles and session tracking. Settings include:
  - **Theme** — Dark or Light
  - **Widget Color** — custom background colour picker
  - **Accent Color** — custom accent colour picker
  - **Glow** — adjustable ring glow intensity slider
  - **Ring Style** — Smooth or Sharp progress ring
  - **Durations** — Focus, Short Break, and Long Break lengths (minutes)
  - **Sessions** — number of sessions per cycle (default 4)
  - **Auto-advance** — automatically start the next session/break
  - **Sound** — toggle notification sound on/off, with volume slider
  - **Zoom** — 50 – 150 % scale
  - Session history panel with editable past entries; dots indicator shows cycle progress

- `widget-pomodoro-scenic.html` — Scenic Pomodoro inspired by studywithme.io: a full-bleed animated background with minimal white UI floating on top (no card or border). Fonts are Fredoka (timer digits) + Quicksand (UI). Settings include:
  - **Scene** — 6 self-contained backgrounds with no image files (Sunset, Ocean, Forest, Night, Sakura, Noir), built from inline SVG art and CSS gradients; Night adds a generated star field
  - **Custom background** — paste any image URL and toggle **Use custom image** to use it instead of a built-in scene
  - **Motion** — Ken Burns (zoom + drift), Pan left → right, Pan right → left, Slow zoom, or Static
  - **Overlay darkness** — 0 – 60 % tint over the scene for text legibility
  - **Zoom** — 70 – 130 % scale of the floating UI
  - **Durations** — Pomodoro, Short Break, and Long Break lengths (minutes)
  - **Sequence** — Pomodoros before a long break (2 – 8) and an **Auto-start next** toggle
  - **Sound** — Bell, Chime, Soft, or None alert (Web Audio, no files), with a play-on-end toggle, volume slider, and Test button
  - Timestamp-based countdown that stays accurate across tab throttling; session dots under the mode pills fill as focus sessions complete; dark settings modal with General / Timers / Sounds tabs

- `widget-music-player.html` — Embedded Spotify or YouTube player. Settings include:
  - **Theme** — Minimal, Dark, OLED, Mono
  - **Ambient Glow** — pulsing glow effect on the player card
  - **Zoom** — 50 – 150 % scale
  - **Link** — paste any Spotify or YouTube URL to load it
  - **Spotify View** — toggle between Compact (80px) and Full (400px) player
  - **Presets** — save and manage custom playlist/track presets with labels; recent links history
  - Switches automatically between Spotify and YouTube embed based on the pasted URL

- `widget-matrix.html` — Fullscreen Matrix-style digital rain. Settings include:
  - **Theme** — Dark or Light canvas background
  - **Style** — Bold or Normal characters
  - **Characters** — Matrix (カナ), Alpha (ABC), Binary (01), Digits (123), Glitch (!@#), or Chaos — picked from a tile grid that previews a sample character
  - **Colour** — 6 theme-aware preset swatches (bright tones on the dark theme, deeper tones on the light theme) plus a full HSV custom colour picker; switching theme migrates the choice by index so the rain stays visible
  - **Speed** — 1 – 4 (step 0.25)
  - **Font Size** — 8 – 20 px (step 1)
  - **Trail Length** — 2 – 14 (step 1)
  - Settings panel opens in the top-left corner with no overlay so live changes are visible behind it
  - Fills any embed size; settings accessible via gear icon

- `widget-timetable.html` — Class timetable in the Dark XP look (Dark, Light or Auto). Features:
  - **AI import** — the widget provides a ready-made prompt; paste it into Claude, ChatGPT or Gemini with a photo of your timetable, paste the JSON reply back, preview it (bad rows are listed and skipped), then **Replace all** or **Add to current**. Holiday dates shown on the timetable come through too
  - **Today view** — a Now / Next card with a live XP-style progress bar and time left, free time between classes, "First up", "Done for today" and the next class on another day; step through other days with the arrows
  - **Week view** — colour-coded grid with a current-time line, side-by-side overlapping classes, weekends shown automatically only when needed
  - **Holidays & exam weeks** — date ranges; holidays clear the timetable for those days, exam weeks show a banner; next holiday countdown in the footer
  - **Per-class extras** — sticker (40 built in), colour, note, room, teacher, type; **cancel a class for one day** without editing the timetable
  - **Week A / Week B** for alternating timetables (switched on automatically when the AI import finds one)
  - **Attendance link** — paste your Notion "Today's Attendance" page link and a **Log attendance** button appears during class
  - **Portable link** — packs the whole timetable into the embed link (`#d=…`), so the same timetable shows on every device; plus copy-backup / restore
  - **Adapts to the device** — detects touch vs mouse and the embed's own width (phone / tablet / desktop), so it also works in the Notion mobile app: bigger tap targets on touch, swipe left / right between days, long course names wrap on phones, the week grid scrolls sideways on phones (opening on today, with hours and day names pinned), and form fields don't trigger iPhone zoom
  - **Samples** — try it before importing: a hypothetical **B.Tech CSE** 3rd-semester timetable (Mon–Sat, labs, tutorials, mid-sem exams + Diwali break) or a **General college** timetable
  - Accent colour, 12 / 24 h, week starts Mon / Sun, zoom 70 – 140 %; `?instance=name` keeps several copies on one page separate

