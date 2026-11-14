# QUANTIX

QUANTIX is a modular Android application foundation for intelligent market analysis. The project follows a layered architecture with app, domain, analytics, data, network, database, and UI modules, and it keeps local-first analysis and future server compatibility in mind.

## Tech stack

- Kotlin
- Jetpack Compose
- Material 3
- MVVM + Flow + coroutines
- Retrofit
- Room
- Gradle
- Android Studio / Android SDK

## Quick start

1. Open the project in Android Studio.
2. Let Gradle sync.
3. Run `:app:assembleDebug`.
4. Install the generated APK from `app/build/outputs/apk/debug/`.

## Project structure

- `app` — Android app entry point and app bootstrap.
- `core` — shared configuration and cross-cutting utilities.
- `domain` — core models and repository contracts.
- `analytics` — technical analysis engine.
- `machinelearning` — future model interfaces and training hooks.
- `network` — public market-data interfaces and Retrofit adapters.
- `database` — Room persistence layer.
- `data` — repository implementation and local storage coordination.
- `ui` — Compose screens, theme, and dashboard state.

## Status

The project currently includes a real local-first dashboard, a real public market-data source using Kraken OHLC endpoints, local analysis history storage, and a transparent technical-analysis engine based on reusable market candles.

The app does not fabricate results and does not use paid APIs or cloud AI services.

## Build check

CI is configured in `.github/workflows/android.yml` and runs a debug build on pushes and pull requests.
