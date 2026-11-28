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
| 🎓 GPA Calculator | https://adrisol-studio.github.io/notion-widgets/widget-gpa.html |
| 🎧 Ambient Sounds | https://adrisol-studio.github.io/notion-widgets/widget-sounds.html |

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
| GPA Calculator | Full | 560px | 640px |
| GPA Calculator | Narrow | 340px | 560px |
| Ambient Sounds | Full | 560px | 560px |
| Ambient Sounds | Narrow | 340px | 720px |

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
  - **Theme** — Auto (follows your system), Dark or Light
  - **Widget Color** — per-theme background swatches plus a custom colour picker
  - **Accent Color** — preset swatches plus a custom colour picker (the white swatch turns black in light theme so the ring stays visible)
  - **Glow** — adjustable ring glow intensity slider
  - **Ring Style** — Smooth or Segmented progress ring
  - **Durations** — Focus, Short Break, and Long Break lengths (1 – 180 minutes)
  - **Sessions** — number of sessions per cycle (default 4, up to 12)
  - **Auto Start** — when a phase ends it is recorded and the next session/break starts by itself; with it off, the timer counts overtime (+MM:SS) until you press stop
  - **Sound** — toggle notification sound on/off, with volume slider
  - **Zoom** — 50 – 150 % scale; the card always shrinks to fit its embed
  - Accurate in background tabs — the countdown follows the real clock, and a running timer carries on after a reload
  - Session history panel grouped by month and day, with editable entries (1 – 480 min); deleting a whole month or day takes two taps; dots indicator shows cycle progress
  - **Adapts to the device** — works in the Notion mobile app: bigger tap targets on touchscreens, history edit / delete buttons always visible on touch, and number fields that don't trigger iPhone zoom

- `widget-pomodoro-scenic.html` — Scenic Pomodoro inspired by studywithme.io: a full-bleed animated background with minimal white UI floating on top (no card or border). Fonts are Fredoka (timer digits) + Quicksand (UI). Settings include:
  - **Background** — 19 built-in scenes drawn in inline SVG (no image files), grouped by the motion they use: **Pan** (Ocean, Forest, City Skyline, Autumn Forest, Lavender Field, Countryside, Desert Dunes, Mountain Valley, Winter Village), **Zoom** (Night, Sakura, Snowy Peaks, Dreamy Clouds, Lily Pond, Rainy Lake), **Ken Burns** (Sunset, Misty Lake, Starry Sky) and **Cinemagraph** (Noir, a rainy street). Switching backgrounds crossfades smoothly
  - **Living scenes** — every built-in scene has gentle ambient motion matched to it: rain and puddle splashes, snowfall, cherry-blossom petals, falling leaves, twinkling stars, fireflies, drifting mist, sparkles on water, blowing sand. It runs on the GPU so it stays smooth for a whole session, and switches off for custom backgrounds and for anyone whose device is set to reduce motion
  - **Custom background** — paste any image or video link (.mp4 / .webm / .mov…) and toggle **Use custom background**; pick its motion (Ken Burns, Pan, Slow zoom or Static). A video that fails to load falls back to the built-in scene
  - **Overlay darkness** — 0 – 60 % tint over the scene for text legibility
  - **Zoom** — 70 – 130 % scale of the floating UI; it always shrinks to fit the embed
  - **Durations** — Pomodoro (1 – 180), Short Break and Long Break (1 – 120) lengths in minutes
  - **Sequence** — Pomodoros before a long break (2 – 8) and an **Auto-start next** toggle
  - **Sound** — Bell, Chime, Soft, or None alert (Web Audio, no files), with a play-on-end toggle, volume slider, and Test button
  - **Controls** — start / pause, skip to the next session, reset; keyboard shortcuts: Space start / pause · R reset · S skip · 1 / 2 / 3 modes · Esc closes settings
  - Timestamp-based countdown that stays accurate across tab throttling, and a running timer (with its session dots) carries on after a reload or switching Notion pages; session dots under the mode pills fill as focus sessions complete; dark settings modal with General / Timers / Sounds tabs
  - **Adapts to the device** — works in the Notion mobile app: bigger tap targets on touchscreens, fields that don't trigger iPhone zoom, and on narrow embeds the settings tabs move to the top so the options get the full width

- `widget-music-player.html` — Embedded Spotify or YouTube player. Settings include:
  - **Theme** — Auto (follows your system), Minimal, Dark, OLED, Mono
  - **Ambient Glow** — pulsing glow effect on the player card
  - **Zoom** — 50 – 150 % scale; the card always fits its embed, so nothing is cut off
  - **Link** — paste any Spotify link (playlist, album, track, episode, podcast) or YouTube / YouTube Music link — videos, playlists, Shorts and Live links; a start time in the link (`?t=90` or `t=1m30s`) is kept
  - **Spotify View** — toggle between Compact (80px) and Full (400px) player
  - **Presets** — built-in focus presets plus your own saved ones (saving the same link again just renames it); removed built-ins can be restored; recent links history shows preset names
  - **Adapts to the device** — works in the Notion mobile app: bigger tap targets on touchscreens, link fields that don't trigger iPhone zoom, settings popup that fits narrow embeds
  - Switches automatically between Spotify and YouTube embed based on the pasted URL; `?instance=name` keeps several copies on one page separate

- `widget-matrix.html` — Fullscreen Matrix-style digital rain. Settings include:
  - **Theme** — Auto (follows your system), Dark or Light canvas background
  - **Style** — Bold or Normal characters
  - **Characters** — Matrix (カナ), Alpha (ABC), Binary (01), Digits (123), Glitch (!@#), or Chaos — picked from a tile grid that previews a sample character
  - **Colour** — 6 theme-aware preset swatches (bright tones on the dark theme, deeper tones on the light theme) plus a full HSV custom colour picker; switching theme migrates the choice by index so the rain stays visible
  - **Speed** — 1 – 4 (step 0.25)
  - **Font Size** — 8 – 20 px (step 1)
  - **Trail Length** — 2 – 14 (step 1)
  - Settings panel opens in the top-left corner with no overlay so live changes are visible behind it
  - Fills any embed size; settings accessible via gear icon (always visible on touchscreens), Esc closes the panel
  - **Adapts to the device** — characters are drawn at the screen's real resolution, so they stay sharp on phones and Retina screens; the settings panel fits narrow embeds
  - **Link options** — `?charset=katakana|latin|binary|numbers|symbols|mixed&theme=dark|light&color=00ff41&speed=1-4&size=8-20&trail=2-14`; values that aren't valid are ignored

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
  - **Safe with your data** — if the browser won't let the embed save (private mode, blocked storage) a warning points you to the portable link; the same widget open in two tabs stays in sync instead of overwriting each other
  - **Keyboard friendly** — every button, class and colour is reachable with Tab, opens with Enter / Space, panels close with Esc and return focus where you were
  - **Samples** — try it before importing: a hypothetical **B.Tech CSE** 3rd-semester timetable (Mon–Sat, labs, tutorials, mid-sem exams + a winter break) or a **General college** timetable
  - Accent colour, 12 / 24 h, week starts Mon / Sun, zoom 70 – 140 %; `?instance=name` keeps several copies on one page separate

- `widget-gpa.html` — GPA / CGPA calculator with a Notion-native minimal look: Notion's own dark grey (#191919) or white page colours (or Auto), clean Inter type with large numbers, a thin progress bar with your target marked on it, and flat cards; accent colours from Notion's palette (mint by default, blue, purple, orange, pink, yellow) or custom. Features:
  - **Grading scales** — **4.0 GPA** (A+ … F with +/-, the default), **10-point CGPA** (O, A+, A, B+, B, C, P, F) or **Percentage** (marks out of 100); switching scale keeps course names and credits and asks before clearing grades
  - **Semesters & courses** — add semesters and courses and edit them in place; semester GPA (SGPA) and cumulative GPA (CGPA) update as you type, weighted by credits. Courses without a grade yet count as **in progress**; **W** (withdrawn) is left out. Enter moves to the next field and adds a new course at the end of a row; deleting a course or semester can be undone
  - **Earlier record** — start from a previous GPA plus the credits it covers instead of typing every old course
  - **Target planner** — the average you need across your remaining credits to reach a target GPA (defaults to your in-progress credits), shown in letters too ("between B+ and A-"), with "already safe" / "not reachable" answers and the target marked on the progress bar
  - **Final exam** — what you need on a final to finish a course with the grade you want, plus a quick table for 90 / 80 / 70 / 60 %
  - **Portable link** (`#d=…`), copy-backup / restore, a warning when the browser won't let the embed save, and two open copies stay in sync
  - **Adapts to the device** — course rows stack on phones, bigger tap targets on touch, fields that don't trigger iPhone zoom, and a compact header so Settings stays on screen in narrow embeds at any zoom; keyboard friendly throughout
  - Accent colour, 2 or 3 decimals, zoom 70 – 140 %, sample grades for each scale; `?instance=name` keeps several copies on one page separate

- `widget-sounds.html` — Ambient sound mixer with a Notion-native base (Notion's dark grey / white, Inter) and its own mood: soft glowing tiles, each sound in its own colour, with little level bars while it plays. Features:
  - **Eight sounds** — Rain, Thunder, Wind, Waves, Fire, Café, Brown noise and Pink noise, all **made live in the browser** (Web Audio) — no audio files, nothing downloaded, works offline. Rain has drops, fire crackles and pops, thunder rolls in now and then, waves swell and break, the café has cups clinking
  - **Mix freely** — tap a sound to switch it on, each with its own volume; levels are balanced so the same slider position sounds equally loud, and a limiter keeps big mixes from distorting
  - **Play / pause** with gentle fades (or instant), **master volume**, **Space** to play / pause
  - **Sleep timer** — 15 / 30 / 45 / 60 / 90 min with a countdown in the header; the last seconds fade out, then it pauses
  - **Mixes** — Rainy café, Cozy cabin, Thunderstorm, Ocean breeze, Deep focus, Library hush, plus up to 20 of your own (save, rename by saving again, delete with undo)
  - Opens paused with your last mix ready (browsers only allow sound after a tap) and tells you if the browser blocked sound; a warning if the browser won't save your mix; two open copies share settings and saved mixes
  - **Adapts to the device** — 4 / 3 / 2 / 1 columns by width, bigger sliders and buttons on touch, keyboard friendly; accent colour, Auto / Dark / Light, zoom 70 – 140 %; `?instance=name` keeps several copies separate
  - On iPhone, the silent switch also mutes web audio — turn it off if you hear nothing
