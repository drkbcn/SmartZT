# 🏍️ SmartZT, Unofficial Zontes companion app

[![Latest release](https://img.shields.io/github/v/release/drkbcn/SmartZT)](https://github.com/drkbcn/SmartZT/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/drkbcn/SmartZT/total)](https://github.com/drkbcn/SmartZT/releases)

An unofficial companion app for Zontes motorcycles, built to replace the
manufacturer's own app with something faster and more reliable. It talks to the
bike's onboard DVR over Wi-Fi and to its PKE keyless module over Bluetooth Low
Energy.

## What it does

- **DVR browsing** — lists and downloads front/rear camera videos and photos
  from the bike's DVR, and plays them back in-app.
- **Screen mirroring** — casts the phone's screen to the bike's dashboard
  display over Wi-Fi Direct, with adjustable frame rate and bitrate.
- **BLE keyless control** — locks/unlocks the bike, opens the seat and fuel
  cap, and controls ambient lighting through the PKE module, using the same
  AES challenge-response scheme as the original app.
- **Fuel log** — track fill-ups and get consumption stats over time.
- **Vehicle settings** — reads and writes parameters stored on the bike's MCU
  (key method, auto-lock timeout, ESS alarm, handbrake alarm, etc.).
- **Garage** — manage more than one motorcycle and switch between them.
- **QR-based setup** — pairing and Wi-Fi credentials are provisioned by
  scanning a QR code, matching how the bike/dealer configuration works.
- **Config export/import** — back up and restore app configuration via an
  encrypted QR code.

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
page and install it on Android. iOS is not currently distributed.

## Supported languages

English, Spanish, Italian, Portuguese, French, German, Greek, Bulgarian and
Ukrainian.

## Disclaimer

This project is not affiliated with, endorsed by, or supported by Zontes. Use
it at your own risk.
