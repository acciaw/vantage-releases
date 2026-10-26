# Vantage releases

Downloads for **Vantage**, a VALORANT companion app for iPhone and Android.

- **Vantage Link** is the small Windows app that installs Vantage on your phone and keeps it up to date (and, on an
  iPhone, renewed every week), and can hide your VALORANT status from friends. Download
  [`vantage-link.exe`](../../releases/download/desktop-latest/vantage-link.exe), run it, and plug in your phone. It
  starts with Windows and updates itself.
- The phone app itself is published here as `ios-v…` and `android-v…` releases. You don't download those by hand:
  Vantage Link fetches the newest one and installs it on your phone, and on Android the app also offers new versions
  itself.

Every file here is signed with the project's release key, and Vantage Link refuses anything that isn't.

The source code is private. This repository only holds release files and the workflows that build them:

| Workflow | Builds |
| --- | --- |
| `release-mobile.yml` | the iPhone and Android apps, released together as `ios-v<version>` and `android-v<version>` |
| `release-desktop.yml` | Vantage Link, as `desktop-v<version>` and the rolling `desktop-latest` |

Both are started from the source repository with `npm run release` and `npm run release:desktop`.
