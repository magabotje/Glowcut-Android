GLOWCUT ANDROID BUILDER PACK
============================

This pack prepares the existing GlowCut web project for wrapping as an Android app.
It does NOT yet include an APK/AAB or live AdMob integration.

PHONE-ONLY BUILD ROUTE (free to try)
1. Download and extract this ZIP on your Android phone.
2. Create a repository on GitHub in your phone browser and upload the files, preserving:
   - package.json
   - capacitor.config.json
   - www/ (all files inside)
   - .github/workflows/android-debug.yml
3. Open the repository's Actions tab and enable GitHub Actions if asked.
4. Run the workflow named "Build Android debug APK".
5. When it finishes successfully, open the workflow run and download its artifact named
   "glowcut-debug-apk". This is a test APK for installing on your own phone, not a Play Store
   release.
6. Install only if you trust the build you triggered. Android may ask you to allow installs
   from that browser/files app.

WHY NOT PLAY STORE YET?
- Google Play generally requires a signed Android App Bundle (.aab), store listing, privacy
  disclosures, and testing/verification. New personal developer accounts have testing rules.
- Google Play Console registration costs US$25 once, so it cannot be completed with R0.
- AdMob requires an account, app/ad unit IDs, SDK integration and privacy/consent handling.
  This starter does not show real ads. Do not use real ads while testing; use Google's test IDs.
- The browser editor's camera and video export behavior must be tested inside the Android
  wrapper; browser APIs may behave differently in WebView.

This workflow creates a debug APK only. It intentionally does not generate a Play Store AAB
or embed signing credentials.
