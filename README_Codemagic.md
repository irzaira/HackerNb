# HackerNb — Build with Codemagic (Debug unsigned)

This repository is prepared to build **HackerNb** using Codemagic CI with the included `codemagic.yaml` workflow.

## Quick steps
1. Push this project to a GitHub repository.
2. Sign in to Codemagic and add a new application -> choose the GitHub repo.
3. Codemagic will detect `codemagic.yaml` and present the `build_debug` workflow.
4. Start the build. After completion, download the artifact:
   `app/build/outputs/apk/debug/app-debug.apk`
5. Install APK on device (enable Install from unknown sources).

## Notes
- The app uses EncryptedSharedPreferences for storing API key and settings.
- Use the in-app Settings (⚙️) to set your Groq API key and model.
- For Termux integration, ensure Termux & Termux:API are installed on your device.
- To prepare for release builds (signed), upload your keystore in Codemagic and change the gradle command to `./gradlew assembleRelease`.
