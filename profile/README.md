<div align="center">

<img src="https://m3ue.sparkison.dev/img/logo.png" width="96" alt="M3U Editor Suite logo">

# M3U Editor Suite

**Your IPTV, fully under control.**

Self-hosted tools for managing and watching live TV, movies, series, guide data, and DVR recordings, served to every player you own from one place.

[Website](https://m3ue.sparkison.dev) · [Docs](https://m3ue.sparkison.dev/docs/intro) · [Quick Start](https://m3ue.sparkison.dev/docs/quick_start) · [Get M3U TV](https://m3ue.sparkison.dev/tv) · [Discord](https://discord.gg/rS3abJ5dz7)

[![M3U Editor stars](https://img.shields.io/github/stars/m3ue/m3u-editor?style=flat&label=M3U%20Editor&logo=github)](https://github.com/m3ue/m3u-editor)
[![M3U Proxy stars](https://img.shields.io/github/stars/m3ue/m3u-proxy?style=flat&label=M3U%20Proxy&logo=github)](https://github.com/m3ue/m3u-proxy)
[![M3U TV stars](https://img.shields.io/github/stars/m3ue/m3u-tv?style=flat&label=M3U%20TV&logo=github)](https://github.com/m3ue/m3u-tv)
[![Discord](https://img.shields.io/badge/Discord-join%20us-5865F2?style=flat&logo=discord&logoColor=white)](https://discord.gg/rS3abJ5dz7)

<img src="https://m3ue.sparkison.dev/img/social-card.jpg" width="800" alt="M3U Editor dashboard: self-hosted playlists, EPG, VOD, and DVR, served to every client from one place">

</div>

## 📺 How it fits together

Your players only ever talk to M3U Editor. Swap providers, fix channel names, or fill in missing guide data, and every device picks up the change without being reconfigured.

| Your sources | | The suite | | Your players |
| :--- | :arrow_right: | :---: | :arrow_right: | :--- |
| IPTV providers (M3U, Xtream)<br>XMLTV and Schedules Direct<br>Emby, Jellyfin, and Plex<br>Local and WebDAV media<br>AIOStreams and the \*arrs | | **M3U Editor** cleans, merges, maps, and enriches<br>**M3U Proxy** handles the streams | | **M3U TV**<br>Plex, Emby, and Jellyfin<br>TiviMate, Kodi, and VLC<br>Any Xtream or M3U app |

## 🧩 The apps

| | Project | What it does |
| :---: | :--- | :--- |
| 🎛️ | **[M3U Editor](https://github.com/m3ue/m3u-editor)**<br>[Docs](https://m3ue.sparkison.dev/docs/intro) | The web app at the center of the suite. Import M3U and Xtream sources, organize channels, VOD, and series, map guide data, record with the built-in DVR, and publish it all as M3U, Xtream Codes API, HDHomeRun, and XMLTV. |
| ⚡ | **[M3U Proxy](https://github.com/m3ue/m3u-proxy)**<br>[Docs](https://m3ue.sparkison.dev/docs/proxy/overview) | A high-performance streaming proxy. Viewers share upstream provider connections, streams fail over automatically, and you can transcode with NVIDIA, Intel, or AMD hardware acceleration, or pass streams through untouched. |
| 🍿 | **[M3U TV](https://github.com/m3ue/m3u-tv)**<br>[Get the app](https://m3ue.sparkison.dev/tv) | A free player built for M3U Editor, for Android TV, Apple TV, phones, tablets, and desktop. Live TV with a guide, movies, series, sports, DVR, and Continue Watching that follows you between devices. |

M3U Editor works with any player, so M3U TV is optional. It works best for those who want TV pairing without typing a password, push notifications, and synced watch progress.

## ✨ What you can do

- 🗂️ **Tidy up your lineup:** sort, rename, renumber, and bulk edit thousands of channels, and build custom or merged playlists.
- 🗓️ **Get a guide that works:** use XMLTV files, remote URLs, or Schedules Direct, with smart channel mapping and dummy EPGs.
- 🔀 **Stay on air:** deduplicate channels across providers and fail over automatically when a stream drops.
- 🔴 **Record anything:** schedule recordings and series rules from the guide, with Comskip, NFO output, OTA support, and disk quotas.
- 🎬 **Manage VOD and series:** generate `.strm` files for your media server, cache content locally, and pull artwork, cast, and ratings from TMDB.
- 🖥️ **Connect your libraries:** bring in Emby, Jellyfin, Plex, local folders, and WebDAV, and serve them next to your live TV.
- 📥 **Request and stream more:** request titles through Sonarr and Radarr, and stream debrid catalogs with AIOStreams.
- 🤖 **Automate it:** use plugins, webhooks, post-processing scripts, the REST API, or the in-app AI Copilot.

## 🚀 Get started

You need [Docker](https://www.docker.com/) and at least one source, such as an Xtream login or an M3U URL or file.

```bash
curl -O https://raw.githubusercontent.com/m3ue/m3u-editor/master/docker-compose.proxy.yml
docker compose -f docker-compose.proxy.yml up -d
```

Then open `http://localhost:36400` and sign in with `admin` / `admin`.

The [Quick Start](https://m3ue.sparkison.dev/docs/quick_start) covers the other setups, and the [compose wizard](https://m3ue.sparkison.dev/compose-wizard) builds a config for you. Prefer not to host it yourself? [ElfHosted](https://store.elfhosted.com/product/m3u-editor/) offers fully managed instances.

## 🔌 More from the ecosystem

| Project | What it does |
| :--- | :--- |
| [m3u-editor-docs-v2](https://github.com/m3ue/m3u-editor-docs-v2) | The source for the [documentation site](https://m3ue.sparkison.dev). Fixes are welcome. |
| [m3u-push-relay](https://github.com/m3ue/m3u-push-relay) | Stateless relay that delivers push notifications from self-hosted editors to M3U TV on phones and tablets |
| [channels-dvr-plugin](https://github.com/m3ue/channels-dvr-plugin) | Maps Gracenote station IDs from a local Channels DVR install to your playlist channels |
| [tv-logos-plugin](https://github.com/m3ue/tv-logos-plugin) | Fills in channel logos by matching names against the open-source tv-logos repository |
| [youtubearr-plugin](https://github.com/m3ue/youtubearr-plugin) | Watches YouTube channels for livestreams and creates or removes custom channels automatically |
| [m3u-editor-for-emby](https://github.com/Serph91P/m3u-editor-for-emby) | Community-maintained Emby plugin for managed library publishing |

Want to build your own? See the [plugin developer guide](https://m3ue.sparkison.dev/docs/extensions/developing-plugins).

## 🤝 Join in

- 💬 **Chat:** ask questions, help others, and try new features on [Discord](https://discord.gg/rS3abJ5dz7).
- 🐛 **Report a problem:** open an issue on the relevant repo, such as [M3U Editor](https://github.com/m3ue/m3u-editor/issues), or browse the [discussions](https://github.com/m3ue/m3u-editor/discussions).
- 🗺️ **See what's next:** follow the [project board](https://github.com/orgs/m3ue/projects/4/views/1).
- 🛠️ **Contribute:** PRs for code and docs are welcome.
- ☕ **Support the project:** buy us a coffee on [Ko-fi](https://ko-fi.com/sparkison).

---

<sub>M3U Editor, M3U Proxy, and M3U TV are licensed under <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0</a>. The suite is an independent set of tools, not an IPTV provider: it doesn't host channels or partner with streaming services. Only use content you're authorized to access.</sub>
