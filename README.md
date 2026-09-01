# NDT User-Agent Data

Automated User-Agent profile data mirror for NDT User-Agent Manager.

This repository is data-only. The browser extension source is maintained separately.

## What is synced

- `data/popup/map.json` — available browsers and operating systems.
- `data/popup/browsers/*.json` — User-Agent profiles grouped by Browser and OS.
- `upstream.json` — source and last synchronization metadata.

## Automatic updates

GitHub Actions synchronizes the upstream data once daily and can also be run manually from the **Actions** tab. A commit is created only when the data changes.

The extension should use jsDelivr as its update-feed base URL:

```text
https://cdn.jsdelivr.net/gh/nguyenduytan/NDT-Useragent-Manager@main/data/popup
```

For example, Chrome on Windows is available at:

```text
https://cdn.jsdelivr.net/gh/nguyenduytan/NDT-Useragent-Manager@main/data/popup/browsers/chrome-windows.json
```

## Data source and attribution

Profile data is synchronized from [ray-lothian/UserAgent-Switcher](https://github.com/ray-lothian/UserAgent-Switcher). Its MPL-2.0 license is copied into this repository during each synchronization as `UPSTREAM-LICENSE-MPL-2.0.txt`.

## Maintainer

Tony Nguyễn — [nguyenduytan.com](https://nguyenduytan.com)
A modern Chrome extension to manage, validate, and switch User-Agent profiles per tab, all tabs, or domain rules.
