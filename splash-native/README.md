# Splash Native

App macOS nativa (SwiftUI, app + barra dei menu) per gestire [Splash](https://github.com/incoai/splash): modelli, configurazioni, caricamento con stima della memoria, server su una porta sola, chat, statistiche.

## Requisiti
- macOS 26.4 o successivo, Apple Silicon
- Swift 6.2 (Xcode 26)
- Splash installato: `brew install incoai/tap/splash`

## Compilare e avviare
Dalla cartella `splash-native/` di questo ramo:
```sh
swift build -c release
.build/release/SplashNative
```

## Test
```sh
swift test
```
I test leggono le schede dei modelli in `Tests/Fixtures/hub/readme` (vedi `NOTICE.md` lì dentro).

## Struttura
- `Sources/NativeCore`: dati, lettura di Splash, stime di memoria, processi
- `Sources/NativeUI`: interfaccia e design system (italiano e inglese)
- `Sources/SplashNative`: l'app e gli adattatori fra i due

## Contributi
Il codice è pubblicato da leggere, scaricare e riusare: pull request e issue non sono accettate.

## Licenze
Il codice in `splash-native/` è sotto licenza MIT (`splash-native/LICENSE`). Il resto del repository è Splash (Apache 2.0, `LICENSE` alla radice). I file in `Sources/NativeCore/Upstream` sono collegamenti ai file dell'app di Splash in `app/Sources/Splash`.
