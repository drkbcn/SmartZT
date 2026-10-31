# 🏍️ SmartZT, Unofficial Zontes companion app

[![Latest release](https://img.shields.io/github/v/release/drkbcn/SmartZT)](https://github.com/drkbcn/SmartZT/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/drkbcn/SmartZT/total)](https://github.com/drkbcn/SmartZT/releases)

An unofficial companion app for Zontes motorcycles, built to replace the
manufacturer's own app with something faster and more reliable. It talks to the
bike's onboard DVR over Wi-Fi and to its PKE keyless module over Bluetooth Low
Energy.

| Moto | Camera | Fuel | Screen | Settings | About |
|:-:|:-:|:-:|:-:|:-:|:-:|
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-about.png" width="130"> |
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-about.png" width="130"> |

Light, dark or system theme can be chosen in **Settings › Theme**.

## What it does

- **Moto** — your bike and its connection state first, with one Connect
  button. Lock, unlock, fuel cap and seat controls show progress while a
  command is being sent, and ambient lighting is controlled through the PKE
  module, using the same AES challenge-response scheme as the original app.
- **Camera** — lists and downloads front/rear DVR videos and photos, and plays
  them back in-app.
- **Fuel** — a fill-up log with consumption stats and charts over time.
- **Screen** — the dashboard (TFT) status and two ways to use it:
  - **Screen mirroring**: casts the phone's screen to the bike's dashboard
    over Wi-Fi Direct, with adjustable frame rate and bitrate.
  - **Android Auto** *(experimental)*: runs Android Auto on the dashboard, for
    maps and music apps such as Waze or Spotify. See below.
- **Vehicle settings** — reads and writes parameters stored on the bike's MCU
  (key method, auto-lock timeout, ESS alarm, handbrake alarm, etc.).
- **Garage** — manage more than one motorcycle and switch between them.
- **QR-based setup** — pairing and Wi-Fi credentials are provisioned by
  scanning a QR code, matching how the bike/dealer configuration works.
- **Config export/import** — back up and restore app configuration via an
  encrypted QR code.
- **Updates** — the app checks this page for new releases (at most once a day)
  and lets you download, postpone or skip a version. **Settings › About** also
  shows the release notes. Builds never expire.

## Android Auto (experimental)

The phone acts as the car's head unit: Android Auto's picture is re-encoded to
the dashboard and touches on the dashboard are sent back to it. The sound of
navigation prompts and music keeps playing through the phone (for example to a
Bluetooth helmet).

- Android Auto must be installed, and its developer *head unit server* started
  by hand: open Android Auto's settings, tap **Version** about ten times, then
  use the ⋮ menu › **Start head unit server**. The app has a shortcut to those
  settings. Android does not let another app start it for you.
- The Android Auto screen also opens on the phone, where you can touch it to
  open apps and menus. A ✕ button takes you back to SmartZT without stopping
  the projection.
- **Try Android Auto on this phone** runs it with no bike connected.
- The picture size (800×480, 1280×720 or 1920×1080) is chosen on the Screen
  tab. Larger sizes cost more CPU and battery.
- Handlebar buttons are not supported: these bikes do not send them.

It has not been validated on every phone or Android Auto version, so expect
rough edges.

## Before you start

BLE control (lock/unlock, seat, fuel cap, ambient light) requires a
16-character Zontes encryption key to authenticate with the PKE module. This
key is **not distributed with the app** — without it, BLE control won't work.

## Status

This is a reverse-engineered client: the BLE frames, crypto, and DVR HTTP API
were derived from the original app rather than from official documentation.
Expect some rough edges around less common vehicle/firmware combinations.

## Installing

This repository does not host the source code — only signed builds. Grab the
latest APK from the [Releases](https://github.com/drkbcn/SmartZT/releases)
page and install it over your current version; your garage, settings and fuel
log are kept. Releases marked *Pre-release* are betas and are not offered by
the in-app update check. iOS is not currently distributed.

## Supported languages

English, Spanish, Italian, Portuguese, French, German, Greek, Bulgarian and
Ukrainian. (Greek, Ukrainian and Bulgarian use the system font.)

## Disclaimer

This project is not affiliated with, endorsed by, or supported by Zontes. Use
it at your own risk.
