# MONOLITH — Local Privacy Vault (Android APK)

Ready-to-build Android project configured with **GitHub Actions** to compile an installable `.apk` automatically — no Android Studio required.

## How to Build Your APK on GitHub

1. **Create a new repository** on GitHub (public or private).
2. **Unzip** `monolith-vault-android-github.zip` and upload/push all files (including the hidden `.github/workflows/build-apk.yml` folder) to the root of your repository's `main` branch.
3. Open the **Actions** tab in your GitHub repository.
4. Click the **Build MONOLITH Android APK** workflow (it runs automatically on push, or click **Run workflow**).
5. Once the build finishes (~2 minutes), scroll to **Artifacts** and download **`monolith-vault-apk`**.
6. Extract `monolith-vault-debug.apk` on your Android device and install it.

## Native Android Privacy Hardening Included

- **`FLAG_SECURE` enabled**: Blocks screenshots, screen recordings, and recent-apps thumbnail previews.
- **`android:allowBackup="false"`**: Prevents Android cloud backup from copying local vault files off-device.
- **`WebViewAssetLoader`**: Serves `app/src/main/assets/index.html` locally on-device over a secure origin so Web Crypto (SHA-256) and IndexedDB run natively.
- **Native Photo & Video Picker**: Supports multi-file selection of photos and videos directly from Android storage.
