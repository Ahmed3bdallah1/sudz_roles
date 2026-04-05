# Sudz — Support

This document describes how to get help with the **Sudz** mobile app and how maintainers can troubleshoot common issues.

---

## For users

### How to get help

- Use the **Contact** or **About** section inside the app (if available), where support details may be loaded from the server.
- Check the app listing on the **App Store** or **Google Play** for publisher contact information.
- For account, bookings, or payments, contact support using the official channels published by the Sudz team (email, phone, or web form).  
  **Replace the placeholders below** with your real support details when you publish this file or mirror it on your website:

| Channel | Details |
|--------|---------|
| Support email | *(add your support email)* |
| Phone / WhatsApp | *(optional)* |
| Website / help center | *(optional)* |

### Privacy

See [`PRIVACY_POLICY.md`](./PRIVACY_POLICY.md) for how we handle personal data.

---

## For developers & maintainers

### Environment

- **Flutter SDK:** match `environment.sdk` in [`pubspec.yaml`](./pubspec.yaml).
- **Android:** JDK 11+ (e.g. JDK 17). Set `JAVA_HOME` so Gradle can run (`flutter build appbundle`, `flutter build apk`).
- **iOS:** Xcode with CocoaPods; run `pod install` under `ios/` when native deps change.

### Common issues

| Issue | What to try |
|-------|-------------|
| `JAVA_HOME is not set` / `java` not found | Set `JAVA_HOME` to your JDK install (e.g. `C:\Program Files\Java\jdk-17`) and add `%JAVA_HOME%\bin` to `PATH`. Restart the terminal / IDE. |
| Android release signed as **debug** | Ensure `android/key.properties` points to a real keystore file (`storeFile=...`) and that the file exists next to or as referenced from `android/`. See [`android/app/build.gradle.kts`](./android/app/build.gradle.kts). |
| App Store: missing location usage strings | Add required keys in `ios/Runner/Info.plist` (e.g. `NSLocationWhenInUseUsageDescription`, `NSLocationAlwaysAndWhenInUseUsageDescription`) with clear user-facing text. |
| API paths out of date | Regenerate endpoints per [`README.md`](./README.md) using `tool/generate_endpoints.dart` and the Postman collections. |

### Useful commands

```bash
flutter pub get
flutter analyze
flutter test
```

```bash
# Android release bundle (Play Store)
flutter build appbundle

# iOS (from macOS)
flutter build ipa
```

### Repository layout (quick reference)

- `lib/` — Flutter app source (features, core, routing).
- `android/`, `ios/` — Native project configuration and assets.
- `assets/translations/` — Localization (`en`, `ar`, etc.).

---

## Reporting bugs (internal)

When filing an issue, include:

1. App version (from **Settings** / **About** or `pubspec.yaml` `version:`).
2. OS and device model.
3. Steps to reproduce and expected vs actual behavior.
4. Screenshots or logs if possible (redact tokens and personal data).

---

*Last updated: April 2026 — adjust support contacts and dates as needed.*
