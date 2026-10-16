# Campus Escape — Android APK project

This is a minimal Android Studio project that wraps the self-contained Campus Escape V6 HTML game in an Android WebView. The V6 game file is bundled under `app/src/main/assets/campus_escape_v4.html` (the filename is retained for compatibility with the launcher), so gameplay itself needs no internet connection and no API keys.

## Build an APK with Android Studio

1. Install Android Studio on a computer.
2. Extract this ZIP.
3. In Android Studio choose **Open** and select the extracted `CampusEscapeAndroid` folder.
4. Allow Android Studio to sync Gradle and install Android SDK Platform 35 if prompted. The first Gradle sync may need internet to download Android build tools/dependencies.
5. To build a test APK, choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
6. When finished, click **locate** in the notification. The debug APK is usually at:
   `app/build/outputs/apk/debug/app-debug.apk`
7. Transfer `app-debug.apk` to your Android phone, tap it, and allow installation from that source if Android asks.

## Make a shareable release APK

In Android Studio, choose **Build > Generate Signed Bundle / APK > APK**, create a signing key, and complete the wizard. Keep the key safe; it is needed for future updates signed as the same app.

## Offline notes

- The game HTML and its JavaScript are stored inside the APK.
- No Internet permission is declared in the manifest.
- Audio effects are synthesized by the game's Web Audio code. Android WebView/device audio settings can affect sound.
- The campus layout and gameplay are the current V6 prototype; this wrapper does not alter them.

## Troubleshooting

- If Gradle sync fails, install a compatible JDK (Android Studio's bundled JDK is recommended) and Android SDK Platform 35 from SDK Manager.
- If the APK installs but audio is silent, tap the in-game **Sound: ON** control once and check the phone's media volume.


## V6 additions

- Moving security patrols near all three exits.
- Shortcut behind C Block blocked by a solid boundary wall.
- Extra named staff by level: Rakesh Sir, PT Sir, Venkat Sir, Principal Sir, and Discipline Sir.
- Original synthesized looping theme, whistle/caught sound, win fanfare, and meme captions.
- Sound toggle controls all synthesized audio.

Note: the Telugu meme lines are displayed as captions; the sound effects/theme are synthesized tones, not original spoken meme recordings.
