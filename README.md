# Scrap Platoon

A tactical run-and-gun game. The whole game is the single file `index.html` (it needs no internet connection).
This repository also builds an **Android APK** of the game automatically with GitHub Actions.

## Get the APK

1. Open the **Actions** tab of this repository and wait for the run called **Build Android APK** to finish (green tick, about 3-5 minutes).
2. Open **Releases** (right side of the repository page) and download **Scrap-Platoon.apk**.
3. Open the file on an Android phone and allow "install unknown apps" when asked.

A new APK is built every time `index.html` or the `android` folder changes. You can also start a build by hand:
**Actions -> Build Android APK -> Run workflow**.

## What is in here

| Path | What it is |
|---|---|
| `index.html` | the game |
| `android/` | a small Android app that shows the game full screen, in landscape |
| `android/keystore.jks` | the key the APK is signed with, so a new APK installs over the old one |
| `.github/workflows/build-apk.yml` | tells GitHub how to build the APK |
| `manifest.webmanifest`, `icon-*.png` | only used when the game is opened as a web page |

## Updating the game

Replace `index.html` with the new version. GitHub builds a new APK by itself.

## Note

The signing key is stored in this public repository. That is fine for installing the APK yourself, but make a private key before publishing the game on Google Play.
