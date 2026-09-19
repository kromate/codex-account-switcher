# Codex Account Switcher

Codex Account Switcher is a small macOS menu bar utility for switching between your Codex accounts. You need the Codex desktop app installed and accounts that you already own.

This repository contains the macOS download and installation guide. Application source code is not included in this release.

## Release

- Release: `v3.0.0`
- Artifact: `Codex-Account-Switcher-macOS-Apple-Silicon.zip`
- Bundle version: `3.0` (build `11`)
- Architecture: Apple Silicon (`arm64`)
- Minimum macOS: `14.0`

The app is an independent utility. It is not affiliated with or endorsed by OpenAI.

## Install

1. Download `Codex-Account-Switcher-macOS-Apple-Silicon.zip` from the [v3.0.0 release](https://github.com/kromate/codex-account-switcher/releases/tag/v3.0.0).
2. Open the ZIP file.
3. Drag **Codex Account Switcher.app** to **Applications**.
4. Open the app from **Applications**.

The distributed app is ad hoc signed and is not Apple-notarized. macOS may block the first launch. If that happens, open **System Settings**, choose **Privacy & Security**, and approve the app there.

## Use the app

The utility adds a menu bar control for switching between Codex accounts. Finish active Codex work before you switch accounts because changing accounts may interrupt that work.

Keep the Codex desktop app installed while you use the utility. The utility does not replace Codex or provide a Codex account.

## Privacy and support

The distributed app bundle contains no saved accounts. Your accounts and authentication data are sensitive. Do not upload logs, `auth.json`, tokens, or other files that contain credentials when reporting a problem.

Open an issue in the [GitHub repository](https://github.com/kromate/codex-account-switcher/issues) with a short description and the macOS version. You can also find the project portfolio at [kromate.dev/#apps](https://kromate.dev/#apps).

## Verify the download

Download `SHA256SUMS.txt` beside the ZIP and run this command in that directory:

```bash
shasum -a 256 -c SHA256SUMS.txt
```

A matching download prints `OK`.
