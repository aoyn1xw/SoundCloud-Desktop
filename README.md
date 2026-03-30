<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest">
<img src="https://raw.githubusercontent.com/zxcloli666/SoundCloud-Desktop/legacy/icons/appLogo.png" width="180px" style="border-radius: 50%;" />
</a>
</p>

<h1 align="center"><a href="https://soundcloud.su/">SoundCloud Desktop</a></h1>

<p align="center">
<b>Native Desktop Application for SoundCloud</b><br>
No Ads · No Captcha · No Censorship · Available in Russia
</p>

<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest">
<img src="https://img.shields.io/github/v/release/zxcloli666/SoundCloud-Desktop?style=for-the-badge&logo=github&color=FF5500&label=VERSION" alt="Version"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/releases">
<img src="https://img.shields.io/github/downloads/zxcloli666/SoundCloud-Desktop/total?style=for-the-badge&logo=download&color=FF5500&label=Downloads" alt="Downloads"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/stargazers">
<img src="https://img.shields.io/github/stars/zxcloli666/SoundCloud-Desktop?style=for-the-badge&logo=github&color=FF5500&label=Stars" alt="Stars"/>
</a>
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/blob/main/LICENSE">
<img src="https://img.shields.io/badge/License-MIT-FF5500?style=for-the-badge" alt="License"/>
</a>
</p>

<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest">
<img src="https://img.shields.io/badge/Download-Latest_Version-FF5500?style=for-the-badge" alt="Download"/>
</a>
</p>

> [!CAUTION]
> Support the project:
>
> Boosty: https://boosty.to/lolinamide
>
> TON: UQAiVd_p6zV3iYNy0H9ZokH6_OEvzSrk-88taa7Mc2kE7pUZ
>
> LTC: LLw3Wh1eGDetjoCc76cbfEHusy1vvaupo8
>
> BTC: bc1qqjk9vy453q9jxvpwm7qa4wg3fw03rgzfa9xadf
>
> Vote for features - [#264](https://github.com/zxcloli666/SoundCloud-Desktop/discussions/264)

---

## What is this?

**SoundCloud Desktop** is a full-featured desktop application for listening to music on SoundCloud. Built with Tauri 2 + React 19 — runs natively, consumes minimal resources, and doesn't lag.

Over **100,000 downloads**. Works on Windows, Linux, and macOS.

---

## Why SoundCloud Desktop

### Available in Russia

SoundCloud is blocked by Roskomnadzor — the web version doesn't open. SoundCloud Desktop works directly without any additional software. The entire SoundCloud catalog is fully accessible.

### No Ads

Zero advertising banners, zero promo inserts between tracks, zero pop-ups saying "get a subscription". Clean interface, just music.

### No Captcha

No endless "I'm not a robot" verifications. Open it — listen.

### No Censorship

Access to the entire SoundCloud catalog without regional restrictions. All tracks, all artists, all genres.

### Native and Lightweight

Built on **Tauri 2** (Rust) instead of Electron. Result:
- Installer size **~15 MB** (not 200+ MB like Electron apps)
- RAM consumption **~80–120 MB** during playback
- Instant startup
- Smooth 60 FPS interface even on weak hardware

### Fully Localized

The interface is translated into multiple languages. Language is detected automatically from the system — no configuration needed.

### System Integration

- **System control** — media keys on keyboard, system notification center (Windows), MPRIS (Linux)
- **Discord Rich Presence** — show your friends what you're listening to
- **Tray** — the app works in the background
- **Auto-updates** — new versions install in one click

---

## Download

### Windows

Go to the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest) and download:
- **`.exe`** (NSIS installer) — recommended
- **`.msi`** — alternative installer

Requirements: Windows 10 (1809+) or Windows 11

### Linux

| Format | Architecture | Description |
|--------|------------|----------|
| `.deb` | amd64, arm64 | Ubuntu, Debian, Mint, Pop!_OS |
| `.rpm` | amd64, arm64 | Fedora, openSUSE, CentOS |
| `.AppImage` | amd64, arm64 | Universal, works everywhere |
| `.flatpak` | amd64 | Sandboxed, auto-updates |

Download the required format from the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest).

For AppImage:
```bash
chmod +x soundcloud-desktop-*.AppImage
./soundcloud-desktop-*.AppImage
```

### macOS

- **Apple Silicon** (M1/M2/M3/M4): `*_arm64.dmg`
- **Intel**: `*_x64.dmg`

Download from the [releases page](https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest).

> [!NOTE]
> **macOS blocking launch?** The app is not signed with an Apple Developer certificate, so Gatekeeper may show an "app is damaged" error. Fixed with one command:
> ```bash
> xattr -cr /Applications/soundcloud-desktop.app
> ```
> After that, the app will launch normally.

---

## Screenshots

<p align="center">

![home-screen](https://github.com/user-attachments/assets/66d6abb5-7ecd-493c-a0a1-19e7b22d2da5)

![liked-tracks](https://github.com/user-attachments/assets/d590bfe7-487b-4578-90fd-2c21646e262a)

</p>

---

## Feedback

| | |
|---|---|
| Suggest an idea | [Discussion #121](https://github.com/zxcloli666/SoundCloud-Desktop/discussions/121) |
| Something not working? | [Discussion #144](https://github.com/zxcloli666/SoundCloud-Desktop/discussions/144) |
| Star the project | [GitHub Stars](https://github.com/zxcloli666/SoundCloud-Desktop/stargazers) — helps with promotion! |

Pull requests are welcome. For major changes, please open an issue first.

---

## Building from Source

<details>
<summary><b>Developer Instructions</b></summary>

### Requirements

- **Node.js** 22+
- **pnpm** 10+
- **Rust** 1.77+ (stable)

### Running

```bash
git clone https://github.com/zxcloli666/SoundCloud-Desktop.git
cd SoundCloud-Desktop/desktop
pnpm install
pnpm tauri dev
```

### Production Build

```bash
pnpm tauri build
```

Artifacts will appear in `src-tauri/target/release/bundle/`.

### Checks

```bash
npx tsc --noEmit        # TypeScript types
cargo check              # Rust compilation
npx biome check src/     # linting
```

</details>

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Shell | Tauri 2 (Rust) |
| Frontend | React 19, Vite 7, Tailwind CSS 4 |
| State | Zustand, TanStack Query |
| Audio | rodio (rust) |
| UI Components | Radix UI |
| Backend | NestJS 11, TypeORM, PostgreSQL |
| CI/CD | GitHub Actions — build for all platforms |
| Linter | Biome |

---

## Statistics

<p align="center">
<img src="https://api.star-history.com/svg?repos=zxcloli666/SoundCloud-Desktop&type=Date" alt="Star History" />
</p>

<p align="center">
<img src="https://zxcloli666.github.io/download-history/zxcloli666_SoundCloud-Desktop.svg" alt="Download History" />
</p>

---

## License

MIT. Details in the [LICENSE](LICENSE) file.

SoundCloud is a trademark of SoundCloud Ltd. This application is not affiliated with SoundCloud.

---

<p align="center">
<code>soundcloud desktop</code> · <code>soundcloud приложение</code> · <code>soundcloud клиент</code> · <code>soundcloud для пк</code> · <code>soundcloud windows</code> · <code>soundcloud linux</code> · <code>soundcloud macos</code> · <code>soundcloud без рекламы</code> · <code>soundcloud россия</code> · <code>soundcloud в россии</code> · <code>soundcloud не открывается</code> · <code>soundcloud заблокирован</code> · <code>soundcloud blocked russia</code> · <code>soundcloud desktop app</code> · <code>soundcloud desktop client</code> · <code>soundcloud player</code> · <code>soundcloud app for pc</code> · <code>soundcloud без капчи</code> · <code>скачать soundcloud на компьютер</code> · <code>soundcloud desktop download</code> · <code>soundcloud alternative client</code> · <code>soundcloud no ads</code> · <code>музыкальный плеер soundcloud</code>
</p>

<p align="center">
<a href="https://github.com/zxcloli666/SoundCloud-Desktop/releases/latest">
<img src="https://img.shields.io/badge/Download_SoundCloud_Desktop-FF5500?style=for-the-badge&logoColor=white" alt="Download" height="50"/>
</a>
</p>
