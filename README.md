# Hypertask for Android

The official Android app for [Hypertask](https://hypertask.ai), open-source project and task management.

This app is a Trusted Web Activity (TWA) wrapper: it ships the Hypertask web app ([app.hypertask.ai](https://app.hypertask.ai)) as a native Android app with its own launcher icon, splash screen, shortcuts, and push notification support. The wrapper was generated with [Bubblewrap](https://github.com/GoogleChromeLabs/bubblewrap) and hand-tuned from there.

## Get the app

Download the latest APK from [Releases](https://github.com/hypertask-ai/android/releases).

## Build it yourself

Requirements: JDK 17, Android SDK.

```bash
./gradlew assembleRelease
```

The unsigned APK lands in `app/build/outputs/apk/release/`. Sign it with your own keystore (`apksigner sign --ks your.keystore ...`). If you self-host Hypertask, point `twa-manifest.json` and `app/src/main/res/values/strings.xml` at your own domain and regenerate with Bubblewrap; your domain must serve a matching `.well-known/assetlinks.json`.

Release signing keys are not part of this repository and never will be.

## License

[AGPL-3.0](LICENSE)
