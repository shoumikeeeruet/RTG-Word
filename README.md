# RTG Word - Android APK & PWA Package

Since compiling a binary `.apk` requires the Android SDK and Gradle build toolchain, this package includes:
1. **`www/index.html`** — The standalone mobile-optimized **RTG Word** app.
2. **GitHub Actions Automated APK Builder (`.github/workflows/build-apk.yml`)** — Push this folder to your GitHub repository and GitHub will automatically compile the downloadable `RTG-Word-APK` binary for you in ~2 minutes!

## Option 1: Build APK Automatically on GitHub (No Android Studio Needed)
1. Upload the contents of this ZIP to your GitHub repository.
2. Go to the **Actions** tab in your GitHub repository.
3. Click **Build RTG Word Android APK** -> **Run workflow**.
4. Once complete, download **`RTG-Word-APK`** (`app-debug.apk`) directly from the Artifacts section and install it on your Android phone.

## Option 2: Build APK Instantly via PWABuilder
1. If your repository has GitHub Pages enabled, copy your GitHub Pages URL.
2. Go to [https://www.pwabuilder.com](https://www.pwabuilder.com), paste your URL, and click **Package for Stores -> Android -> Download APK**.

## Option 3: Build Locally with Node.js & Android SDK
```bash
npm install
npx cap add android
npx cap sync
cd android && ./gradlew assembleDebug
```
Your APK will be located at `android/app/build/outputs/apk/debug/app-debug.apk`.
