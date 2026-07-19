<h1 align="center">Hi, I'm Bank 👋</h1>
<p align="center">🎮 Unity Game Developer · 🌏 Bangkok, Thailand · 🕹️ 6+ years</p>

---

### 👨‍💻 About me
- 🛠️ I build **multiplayer, mobile & WebGL games** with **Unity** and **C#**, focused on real-time networking and scalable content delivery
- 🧰 Building open-source Unity tooling under **KidzDev**
- 🎓 B.Eng. Computer Engineering — Chiang Mai University
- 🔗 Portfolio → **[knabsiraphop.github.io](https://knabsiraphop.github.io/?utm_source=github)**

### 🧩 Tech Stack
<p>
  <img src="https://skillicons.dev/icons?i=unity,cs,dotnet,git,github,visualstudio" />
</p>

![Nakama](https://img.shields.io/badge/Nakama-25A0DA?style=flat-square)
![Addressables](https://img.shields.io/badge/Unity_Addressables-222C37?style=flat-square)
![Claude Code](https://img.shields.io/badge/Claude_Code-CC785C?style=flat-square&logo=anthropic&logoColor=white)

### 🎮 Shipped Games
- **Zabb World: Secret Stories** — multiplayer virtual-life simulation (Nakama networking)
- **Rescue MeowMeow** — educational puzzle game for Thai PBS Kids (WebGL & mobile browser) · [▶ Play Demo](https://knabsiraphop.itch.io/rescue-meowmeow-portfolio-demo)
- **Pakapow: Friendship Never Ends** — bug fixes, fashion system updates, build pipeline

### 🧰 Open Source — KidzDev Unity Packages

*These packages are built with [Claude Code](https://claude.com/claude-code) — design, direction, and review by me; most implementation code written by Claude under that direction. All code is original. Some started as patterns and code I picked up working with coworkers, rebuilt into standalone packages this way; others solve a real problem I hit on a shipped title where I didn't have time to build the fix myself, so I used Claude Code to build it.*

**📦 Addressables & Asset Loading**

| Package | Description |
|---|---|
| [kidzdev-unity-addressables-toolkit](https://github.com/knabsiraphop/kidzdev-unity-addressables-toolkit) | Reference-counted async loading, prefab pooling, typed `AssetReference` wrappers, and remote-content download helpers |

**⚙️ Game Systems**

| Package | Description |
|---|---|
| [kidzdev-unity-state-machine](https://github.com/knabsiraphop/kidzdev-unity-state-machine) | Sync & async (UniTask) finite state machine — optional transition graph, `QueueLatest` policy for button-mash safety, fallback recovery, fluent builder |
| [kidzdev-unity-singleton](https://github.com/knabsiraphop/kidzdev-unity-singleton) | Generic singleton bases — thread-safe plain C# `Singleton<T>`, auto-creating `MonoSingleton<T>`, and non-creating `SceneSingleton<T>`, handling MonoBehaviour lifecycle pitfalls (quit-teardown resurrection, domain-reload staleness, duplicate detection, DDOL placement). Zero external dependencies |
| [kidzdev-unity-analytics](https://github.com/knabsiraphop/kidzdev-unity-analytics) | Minimal analytics event-logging facade — validates event/parameter names against Firebase Analytics limits before dispatch, buffers events logged before initialization, warns instead of silently dropping on violations. Zero dependencies (core); optional Firebase adapter sample |
| [kidzdev-unity-grid](https://github.com/knabsiraphop/kidzdev-unity-grid) | 2D/3D grid system — per-cell data storage (`Grid<TCell>`), synchronous A* pathfinding, multi-cell footprint placement, and nearest-available-cell search, plus a thin Unity layer for world/cell conversion and mouse/touch picking. Not a Tilemap replacement — an optional adapter aligns it to an existing `UnityEngine.Grid` when one is used for rendering. Zero external dependencies |
| [kidzdev-unity-notifications](https://github.com/knabsiraphop/kidzdev-unity-notifications) | Cross-platform local notification scheduler over `com.unity.mobile.notifications` — one facade + `INotificationScheduler` seam replaces per-platform `#if` branching, `NotificationId` derives both Android/iOS identities from a single key, typed `PermissionDenied` result (no permission-wait hangs), facade-level idempotency, cached async launch-notification inspection for deep links |

**🎵 Audio**

| Package | Description |
|---|---|
| [kidzdev-unity-audio](https://github.com/knabsiraphop/kidzdev-unity-audio) | Production-grade BGM/SFX/Ambience audio service — UniTask async, AudioMixer-backed dB conversion, cancellable crossfades, pooled sources, plug-in clip loader (Resources default, Addressables adapter), plug-in volume store |

**🎨 UI / uGUI**

| Package | Description |
|---|---|
| [kidzdev-unity-scroll-snap](https://github.com/knabsiraphop/kidzdev-unity-scroll-snap) | Snap pager — horizontal carousel, vertical picker, coverflow, dot / number / page-button indicators, focus effects, auto-play |
| [kidzdev-unity-recyclable-scroll](https://github.com/knabsiraphop/kidzdev-unity-recyclable-scroll) | High-performance recyclable `ScrollRect` — object pooling, linear & loop modes, variable sizes, sync / async (Addressables) binding |
| [kidzdev-unity-responsive-fit](https://github.com/knabsiraphop/kidzdev-unity-responsive-fit) | Responsive grid / scroll item sizing — fit by items-per-view, aspect ratio, or column count |
| [kidzdev-unity-screen-navigator](https://github.com/knabsiraphop/kidzdev-unity-screen-navigator) | Stack-based UI navigation — push/pop history with a back button, async transitions, and an injectable animation seam. UniTask-only, zero singleton coupling |
| [kidzdev-unity-popup](https://github.com/knabsiraphop/kidzdev-unity-popup) | Modal dialogs you await for a typed result — `ShowAsync<TResult>()`, reentrant stacking, async transitions, per-popup loader split (Resources / Direct / Addressables). UniTask-only, Addressables optional, zero singleton coupling |
| [kidzdev-unity-safe-area](https://github.com/knabsiraphop/kidzdev-unity-safe-area) | Notch / safe-area layout — `SafeArea` shrinks a RectTransform inside the device safe area, `SafeAreaOutsideMask` fills the region outside it, plus an Editor window for Android cutout & iOS home indicator setup |
| [kidzdev-unity-text-scroll](https://github.com/knabsiraphop/kidzdev-unity-text-scroll) | Animated text for uGUI/TMPro — marquee ticker, credits roll, auto-fit overflow scrolling, typewriter character reveal, and a count-up number roller. No third-party animation dependency |
| [kidzdev-unity-ui-overlay](https://github.com/knabsiraphop/kidzdev-unity-ui-overlay) | Loading panels (fullscreen / progress / spinner) and a ref-counted input blocker — imperative `Show()`/dispose handles plus `Execute*` wrappers for one-line show/await/hide. UniTask-only, no DOTween, no Addressables dependency |
| [kidzdev-unity-ui-animation](https://github.com/knabsiraphop/kidzdev-unity-ui-animation) | uGUI tweening toolkit — fade/scale/move/punch/shake/color extension methods, conflict-safe cancel-and-replace, a designer-facing step-sequence player, and button press feedback. No third-party animation dependency by default; optional DOTween-backed driver auto-compiles (never auto-activates) when DOTween is present |
| [kidzdev-unity-sliced-fill-image](https://github.com/knabsiraphop/kidzdev-unity-sliced-fill-image) | Fixes Unity's `Image.Type.Filled` + `Type.Sliced` clipping bug with a mesh-correct `SlicedFilledImage`, so 9-sliced borders stay fixed-size at any fill amount. Zero dependencies beyond uGUI |
| [kidzdev-unity-toast](https://github.com/knabsiraphop/kidzdev-unity-toast) | Non-blocking, auto-dismissing notification banners (snackbars) for uGUI — fire-and-forget `Show()`, capped stack with newest-evicts-oldest admission, slide + fade transition. No DOTween, no Addressables dependency |

**🛠️ Editor Tools**

| Package | Description |
|---|---|
| [kidzdev-unity-google-sheet-importer](https://github.com/knabsiraphop/kidzdev-unity-google-sheet-importer) | Import Google Sheets into Unity — maps columns to C# fields via reflection, outputs JSON or ScriptableObject assets |
| [kidzdev-unity-localization](https://github.com/knabsiraphop/kidzdev-unity-localization) | Lightweight localization — JSON / ScriptableObject sources, UniTask parallel loading, TMP auto-refresh |

**🔧 Utilities**

| Package | Description |
|---|---|
| [kidzdev-unity-extensions](https://github.com/knabsiraphop/kidzdev-unity-extensions) | Handy C# / Unity extension methods — strings, collections, numerics, date & time (`DateTimeOffset`, `TimeSpan`, relative time), GameObjects, Animators, Cameras, and ScrollRects |
| [kidzdev-unity-profanity](https://github.com/knabsiraphop/kidzdev-unity-profanity) | Production-grade multilingual profanity filter — obfuscation-aware engine (leetspeak, separators, repeat-collapse) or fast regex mode, allowlist for false-positive prevention, plug-in data loader, ships with a production-scale ~135-entry EN/TH word list out of the box |
| [kidzdev-unity-local-save](https://github.com/knabsiraphop/kidzdev-unity-local-save) | Generic on-disk persistence for any `[Serializable]` type — atomic + durable writes, automatic backup-on-corrupt recovery, optional HMAC signing / AES encryption, zero external dependencies |

### 📊 GitHub Stats
<p>
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=knabsiraphop&theme=tokyonight" />
</p>
<p>
  <img height="160" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=knabsiraphop&theme=tokyonight" />
  <img height="160" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=knabsiraphop&theme=tokyonight" />
</p>
