# Arova Chrome downloads

**English** | [简体中文](README.zh-CN.md)

[Download current and previous versions](https://github.com/spencer17x/arova-releases/releases)

[Features](FEATURES.md) · [User guide](USAGE.md)

This is Arova's official public download repository. It distributes compiled Chrome extension packages, SHA256 checksums, and release information. You do not need access to the private development repository or the Chrome Web Store.

Arova brings Fomo / Pump activity to supported XXYY, GMGN, and DeBot trading pages, with private account notes, browser alerts, and Telegram notifications to multiple destinations. Configure your account in the standalone settings page; use the floating panel to view alerts and quick controls.

The extension supports English and Simplified Chinese. It follows the browser language by default, with a manual override in the settings sidebar. Each Telegram destination has its own alert language.

## Start here

| Task | Documentation |
| --- | --- |
| Explore supported platforms and capabilities | [Features](FEATURES.md) |
| Install or update | [Installation and updates](USAGE.md#installation-and-updates) |
| Set up for the first time | [Quick start](USAGE.md#quick-start) |
| Connect Fomo / Pump with server renewal | [Connect monitoring sources](USAGE.md#connect-monitoring-sources), [Renewal methods](USAGE.md#renewal-methods) |
| Send alerts to Telegram groups / channels | [Telegram alerts](USAGE.md#telegram-alerts) |
| Check paid, gifted, or permanent access | [Plans and access](USAGE.md#plans-and-access) |
| Troubleshoot loading, sign-in, or alerts | [Troubleshooting](USAGE.md#troubleshooting) |

## Installation and updates

1. Download `arova-chrome-VERSION.zip` from Releases and extract it to a folder you will keep.
2. Open `chrome://extensions` and enable **Developer mode**.
3. Click **Load unpacked** and select the extracted folder containing `manifest.json`.
4. Click the Arova toolbar icon to open settings, sign in, and configure the features you need.

To update, replace the contents of the original folder with the new package, click **Reload** for Arova in Chrome extensions, then refresh your trading pages. Do not uninstall first if you want to keep browser settings. GitHub packages do not automatically update installed extensions.

A beta may be rebuilt under the same version name. Compare the build identifier in `release-info.json` and the checksum in `SHA256SUMS` to distinguish builds.

## Release contents

- `arova-chrome-VERSION.zip`: official extension package.
- `SHA256SUMS`: SHA256 checksum of the package.
- `release-info.json`: version, build identifier, extension ID, production API, and checksum.

Fixed extension ID: `gedflalfmklfccgaabdbcnjjchlfemfo`.

Public tags represent distribution snapshots. GitHub's automatically generated **Source code** ZIP/TAR contains only this repository's documentation, publishing configuration, and build artifacts. Install `arova-chrome-VERSION.zip` instead.

This repository does not contain Arova's TypeScript / Python application source, server code, private Git history, environment configuration, or secrets. Extension packages contain the compiled JavaScript required to run.

## License

Arova uses a proprietary commercial license; see [LICENSE](LICENSE). Public downloads do not make the application open source. Third-party licenses and copyright notices remain in the package's `THIRD_PARTY_NOTICES.txt`. Account access and available plans are controlled by the Arova server.

[Illustrated walkthrough](USAGE.md#illustrated-walkthrough)
