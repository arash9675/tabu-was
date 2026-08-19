# Tabu Wash (Android — Capacitor MVP)

A minimal Capacitor wrapper around the Tabu Wash PWA. The Android app loads
`https://laundry.qd.je/dashboard.html` inside a WebView.

## Build the APK

### 1. GitHub Actions (recommended — no local SDK needed)

Push this repo to GitHub, then run the **"Build APK"** workflow (or push to `main`).
Download the APK from the workflow's **Artifacts**.

### 2. Local build

```bash
npm install
npx cap add android
npx cap sync android
cd android && ./gradlew assembleDebug
# APK: android/app/build/outputs/apk/debug/app-debug.apk
```

## Local requirements

- Node.js 18+
- Java 17 (JDK)
- Android SDK (Android Studio)

## Next steps

- Replace the default app icon using `@capacitor/assets`
- Add plugins: `@capacitor/app`, `@capacitor/splash-screen`, `@capacitor/share`,
  `@capacitor/camera`, `@capacitor/push-notifications`
- Switch from the remote URL to bundled `static/` files for offline use
  (requires pointing the app's `API_URL` at `https://laundry.qd.je`)
