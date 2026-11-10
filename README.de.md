🌐 [English](README.md) · [Español](README.es.md) · [Italiano](README.it.md) · [Português](README.pt.md) · [Français](README.fr.md) · **Deutsch** · [Ελληνικά](README.el.md) · [Български](README.bg.md) · [Українська](README.uk.md)

# 🏍️ SmartZT, inoffizielle App für Zontes-Motorräder

[![Neueste Version](https://img.shields.io/github/v/release/drkbcn/SmartZT)](https://github.com/drkbcn/SmartZT/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/drkbcn/SmartZT/total)](https://github.com/drkbcn/SmartZT/releases)

Eine inoffizielle App für Zontes-Motorräder, gebaut, um die App des
Herstellers durch etwas Schnelleres und Zuverlässigeres zu ersetzen. Sie
spricht per WLAN mit der Bordkamera (DVR) des Motorrads und per Bluetooth Low
Energy mit seinem Keyless-Modul PKE. Sie läuft auf Android und seit 2.1 als
erste **iOS-Version im Test** auch auf iPhone und iPad (siehe
[iOS (im Test)](#ios-im-test)).

| Motorrad | Kamera | Tanken | Bildschirm | Einstellungen | Über |
|:-:|:-:|:-:|:-:|:-:|:-:|
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-about.png" width="130"> |
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-about.png" width="130"> |

Helles, dunkles oder System-Design wählst du unter **Einstellungen › Design**.

## Was sie kann

- **Motorrad**: zuerst dein Motorrad und sein Verbindungsstatus, mit einem
  einzigen Button **Mit Motorrad verbinden**. Sperren, Entsperren, Tankdeckel
  und Sitzbank zeigen den Fortschritt, während der Befehl gesendet wird, und
  das Ambientelicht wird über das PKE-Modul gesteuert, mit demselben
  AES-Challenge-Response-Verfahren wie die Original-App.
- **Kamera**: listet die Videos und Fotos der Front- und Heckkamera des DVR
  auf, lädt sie herunter und spielt sie in der App ab.
- **Tanken**: ein Tankbuch mit Verbrauchsstatistiken und Diagrammen über die
  Zeit.
- **Bildschirm**: der Status des Cockpits (TFT) und zwei Arten, es zu nutzen:
  - **Bildschirmspiegelung**: überträgt den Handybildschirm per Wi-Fi Direct
    auf das Cockpit des Motorrads, mit einstellbarer Bildrate und Bitrate.
  - **Android Auto** *(experimentell)*: zeigt Android Auto im Cockpit an, für
    Karten- und Musik-Apps wie Waze oder Spotify. Details weiter unten.
- **Fahrzeugeinstellungen**: liest und ändert Parameter, die in der MCU des
  Motorrads gespeichert sind (Schlüsselmethode, Zeit bis zur automatischen
  Sperre, ESS-Alarm, Handbremsalarm usw.).
- **Garage**: verwalte mehr als ein Motorrad und wechsle zwischen ihnen.
- **Einrichtung per QR**: Kopplung und WLAN-Zugangsdaten werden durch das
  Scannen eines QR-Codes eingerichtet, so wie bei der Konfiguration des
  Motorrads oder beim Händler.
- **Konfiguration exportieren/importieren**: Sicherung und Wiederherstellung
  der App-Konfiguration über einen verschlüsselten QR-Code.
- **Updates**: die App prüft diese Seite auf neue Versionen (höchstens einmal
  am Tag) und lässt dich eine Version herunterladen, verschieben oder
  überspringen. **Einstellungen › Über** zeigt auch die Versionshinweise.
  Android-Versionen laufen nie ab.

## Android Auto (experimentell)

Das Handy übernimmt die Rolle des Autoradios: das Bild von Android Auto wird
für das Cockpit neu kodiert, und Berührungen im Cockpit werden zurückgeschickt.
Navigationsansagen und Musik kommen weiterhin aus dem Handy (zum Beispiel über
ein Bluetooth-Headset im Helm).

- Android Auto muss installiert sein, und sein *Head Unit Server* für
  Entwickler muss von Hand gestartet werden: öffne die Einstellungen von
  Android Auto, tippe etwa zehnmal auf **Version** und wähle dann im Menü ⋮ ›
  **Start head unit server**. Die App hat eine Verknüpfung zu diesen
  Einstellungen. Android erlaubt keiner anderen App, ihn für dich zu starten.
- Der Android-Auto-Bildschirm öffnet sich auch auf dem Handy, wo du ihn
  antippen kannst, um Apps und Menüs zu öffnen. Ein ✕-Button bringt dich zu
  SmartZT zurück, ohne die Projektion zu beenden.
- **Android Auto auf diesem Handy testen** startet es ohne verbundenes
  Motorrad.
- Die Bildgröße (800×480, 1280×720 oder 1920×1080) wählst du im Tab
  Bildschirm. Größere Auflösungen kosten mehr CPU und Akku.
- Lenkertasten werden nicht unterstützt: diese Motorräder senden sie nicht.

Es wurde nicht mit jedem Handy und jeder Android-Auto-Version getestet, also
rechne mit kleinen Macken.

## iOS (im Test)

SmartZT 2.1 ist die erste Version für iPhone und iPad. Sie ist **im Test**:
rechne mit kleinen Macken und melde bitte, was nicht funktioniert.

- **Die Bildschirmspiegelung auf iOS ist noch in einem sehr frühen Stadium.**
  Auf manchen Handys und Cockpits startet sie eventuell nicht oder zeigt kein
  Bild. Wenn sie fehlschlägt, teile das Spiegelungsprotokoll (Teilen-Button auf
  der Cockpit-Karte im Tab Bildschirm) und hänge es an ein
  [Issue](https://github.com/drkbcn/SmartZT/issues) an.
- **Funktioniert auf iOS:** Motorrad (Sperren, Entsperren, Sitzbank,
  Tankdeckel, Ambientelicht, Batteriespannung), Kamera (Videos und Fotos des
  DVR), Tanken, Garage, Fahrzeugeinstellungen, Einrichtung per QR und
  Export/Import der Konfiguration.
- **Auf iOS nicht verfügbar:** Android Auto, das Navigations-HUD, die
  Bildschirmschutz-Ebene und Widgets auf dem Home-Bildschirm. Wi-Fi Direct
  gibt es auf iOS nicht, deshalb verbindest du dich in der Einstellungen-App
  von iOS von Hand mit dem WLAN des DVR; SmartZT zeigt dir Name und Passwort.
- **Voraussetzungen:** iOS 15 oder neuer (die Bildschirmspiegelung braucht
  iOS 16 oder neuer), eine Apple-ID (eine kostenlose reicht) und ein Computer
  mit Windows, macOS oder Linux, um die App zu installieren.

### Installation auf iPhone oder iPad (Sideloading)

SmartZT ist nicht im App Store. Die `.ipa` von der Seite
[Releases](https://github.com/drkbcn/SmartZT/releases) installierst du mit
deiner eigenen Apple-ID über
**[Impactor](https://github.com/claration/Impactor)**, ein kostenloses
Open-Source-Tool für Sideloading:

1. Lade `SmartZT-<Version>.ipa` aus der neuesten Version herunter.
2. Installiere Impactor von seiner
   [Release-Seite](https://github.com/claration/Impactor/releases):
   - **Windows:** installiere zuerst [iTunes](https://support.apple.com/en-us/106372);
     Impactor nutzt dessen Treiber, um mit dem iPhone zu sprechen.
   - **macOS:** `brew install --cask impactor`, oder lade es herunter.
   - **Linux:**
     [Flathub](https://flathub.org/apps/dev.khcrysalis.PlumeImpactor). Es
     braucht `usbmuxd`, das die meisten Distributionen schon mitbringen.
3. Schließe das iPhone per USB an, entsperre es und tippe auf **Vertrauen**,
   wenn es nach dem Computer fragt.
4. Öffne Impactor, melde dich mit deiner Apple-ID an, wähle die `.ipa` von
   SmartZT und installiere sie.
5. Ab iOS 16 aktivierst du **Einstellungen › Datenschutz & Sicherheit ›
   Entwicklermodus** (*Settings › Privacy & Security › Developer Mode*) und
   startest das Handy neu, wenn es danach fragt.
6. Wenn iOS meldet, dass dem Entwickler nicht vertraut wird, öffne
   **Einstellungen › Allgemein › VPN & Geräteverwaltung** (*Settings ›
   General › VPN & Device Management*), tippe auf deine Apple-ID und vertraue
   ihr.

**Mit einer kostenlosen Apple-ID:**

- Apple sorgt dafür, dass sich die App nach **7 Tagen** nicht mehr öffnen
  lässt. Installiere sie mit Impactor erneut (Impactor kann sie auch für dich
  erneuern); Garage, Einstellungen und Tankbuch bleiben erhalten.
- Es können höchstens 3 per Sideloading installierte Apps gleichzeitig
  vorhanden sein, und pro Woche lassen sich nur 10 App-IDs registrieren.
  SmartZT braucht 2: die App und ihre Erweiterung für die
  Bildschirmübertragung.

**Wenn Impactor** `An Application Group with Identifier
'group.com.vitapps.smartzt.…' is not available` **anzeigt**, installiere sie
einfach noch einmal: das kann bei der ersten Installation passieren, und beim
zweiten Versuch ist die Gruppe schon angelegt.

AltStore, SideStore und Sideloadly sollten auch funktionieren, getestet wurde
bisher aber nur Impactor.

**Zum Aktualisieren** lädst du die neue `.ipa` herunter und installierst sie
auf dieselbe Weise über die aktuelle.

### Bildschirmspiegelung auf iOS

1. Verbinde dich in der Einstellungen-App von iOS mit dem WLAN des Motorrads
   (SmartZT zeigt dir Name und Passwort) und kehre dann zu SmartZT zurück.
2. Starte im Tab **Bildschirm** die Spiegelung.
3. Wähle im Bildschirmübertragungs-Fenster von iOS **SmartZT** und tippe auf
   den Button, um die Übertragung zu starten.
4. Lass das Handy entsperrt. Solange es gesperrt ist, zeigt das Cockpit ein
   Bild „Handy gesperrt“. **Keep running when locked** (die Option ist in der
   App noch auf Englisch) spielt unhörbaren Ton ab, damit iOS die Spiegelung
   am Leben hält; das kostet mehr Akku.

## Bevor du loslegst

Die BLE-Steuerung (Sperren/Entsperren, Sitzbank, Tankdeckel, Ambientelicht)
braucht einen 16-stelligen Zontes-Schlüssel, um sich beim PKE-Modul zu
authentifizieren. Dieser Schlüssel wird **nicht mit der App verteilt**: ohne
ihn funktioniert die BLE-Steuerung nicht.

## Status

Dies ist ein per Reverse Engineering entstandener Client: die BLE-Frames, die
Verschlüsselung und die HTTP-API des DVR wurden aus der Original-App
abgeleitet, nicht aus offizieller Dokumentation. Bei selteneren Kombinationen
aus Motorrad und Firmware kann es Macken geben.

## Installation

Dieses Repository enthält nicht den Quellcode, sondern nur signierte Builds.

- **Android:** lade das neueste APK von der Seite
  [Releases](https://github.com/drkbcn/SmartZT/releases) herunter und
  installiere es über deine aktuelle Version; Garage, Einstellungen und
  Tankbuch bleiben erhalten. Als *Pre-release* markierte Versionen sind Betas
  und werden von der Update-Prüfung der App nicht angeboten.
- **iPhone und iPad:** siehe
  [Installation auf iPhone oder iPad](#installation-auf-iphone-oder-ipad-sideloading).

## Sprachen

Englisch, Spanisch, Italienisch, Portugiesisch, Französisch, Deutsch,
Griechisch, Bulgarisch und Ukrainisch. (Griechisch, Ukrainisch und Bulgarisch
nutzen die Systemschrift.)

## Haftungsausschluss

Dieses Projekt steht in keiner Verbindung zu Zontes und wird von Zontes weder
unterstützt noch empfohlen. Die Nutzung erfolgt auf eigene Gefahr.
