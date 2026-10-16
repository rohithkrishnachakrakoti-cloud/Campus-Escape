# Build Campus Escape APK using only your phone

This project includes a GitHub Actions workflow that builds a debug APK in the cloud. The game HTML is bundled in the app; the installed game does not need internet access.

## Steps on an Android phone

1. Sign in at https://github.com/ and create a new repository named `CampusEscape` (a public repository is easiest for a first-time setup; do not upload secrets).
2. On the repository page, tap **Add file** > **Upload files**.
3. Extract `CampusEscapeAndroidProject_V6_GitHubBuild.zip` using your phone's Files app or a ZIP utility. Upload the *contents* of the `CampusEscapeAndroid` folder (including the hidden `.github` folder if your ZIP utility shows it) to the repository root, then commit the upload. If the mobile upload UI hides `.github`, use GitHub's web editor to create `.github/workflows/build-apk.yml` using the workflow file included in the ZIP.
4. Open the repository's **Actions** tab. Choose **Build Campus Escape APK** and tap **Run workflow** if it hasn't started automatically.
5. Wait until the workflow has a green check mark. Open that completed run, scroll to **Artifacts**, and tap `Campus-Escape-V6-APK` to download the ZIP.
6. Extract the downloaded artifact ZIP and tap `app-debug.apk` to install. If Android asks, allow your browser or Files app to install unknown apps.

The first cloud build needs internet. GitHub may require verifying your account or enabling Actions. This is a debug/test APK, not a Play Store release.
