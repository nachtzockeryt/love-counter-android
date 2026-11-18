# Love Counter

A small Android relationship counter written in Rust with [egui](https://github.com/emilk/egui). It shows how long you have been together and can switch each value to its total count.

## Features

- English interface
- Live counter for years, months, days, hours, minutes, and seconds
- Tap a value to show its total
- Change the relationship start date and time
- Uses the phone's local time zone
- Saves the start date on the device; no account or network connection is used

On first launch, the counter starts from today. Tap **Startdatum ändern** to enter your actual date.

## Install

Download `LoveCounter.apk` from the latest GitHub Release, open it on your Android phone, and allow installation from that source when Android asks.

## Build from source

You need Rust, the Android SDK and NDK, and `cargo-apk`.

```powershell
cargo install cargo-apk
rustup target add aarch64-linux-android
cargo apk build
```

The debug APK is written to `target/debug/apk/LoveCounter.apk`.

For a release build, create and configure a private Android signing keystore, then run:

```powershell
cargo apk build --release
```

Keep the signing keystore and its password private and backed up. Do not commit them to this repository. Android updates must be signed with the same key as the installed app.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).

---

# Love Counter (Deutsch)

Ein kleiner Beziehungszähler für Android, geschrieben in Rust mit [egui](https://github.com/emilk/egui). Die App zeigt, wie lange ihr zusammen seid, und kann für jeden Wert die Gesamtzahl anzeigen.

## Funktionen

- Englische Benutzeroberfläche
- Live-Zähler für Jahre, Monate, Tage, Stunden, Minuten und Sekunden
- Tippen auf einen Wert zeigt die Gesamtzahl
- Startdatum und Uhrzeit lassen sich ändern
- Verwendet die lokale Zeitzone des Handys
- Speichert das Startdatum lokal auf dem Gerät; kein Konto und keine Internetverbindung nötig

Beim ersten Start zählt die App ab heute. Tippe auf **Startdatum ändern**, um euer echtes Datum einzutragen.

## Installation

Lade `LoveCounter.apk` aus dem neuesten GitHub-Release herunter, öffne die Datei auf deinem Android-Handy und erlaube bei Nachfrage die Installation aus dieser Quelle.

## Aus dem Quellcode bauen

Benötigt werden Rust, Android SDK und NDK sowie `cargo-apk`.

```powershell
cargo install cargo-apk
rustup target add aarch64-linux-android
cargo apk build
```

Die Debug-APK liegt anschließend unter `target/debug/apk/LoveCounter.apk`.

Für einen Release-Build muss zuerst ein privater Android-Signierschlüssel eingerichtet werden. Danach:

```powershell
cargo apk build --release
```

Bewahre Signierschlüssel und Passwort sicher und getrennt vom öffentlichen Repository auf. Android-Updates müssen mit demselben Schlüssel signiert sein wie die installierte App.

## Lizenz

Dieses Projekt steht unter der MIT-Lizenz. Siehe [LICENSE](LICENSE).
