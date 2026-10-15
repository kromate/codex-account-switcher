# Codex Account Switcher

Codex Account Switcher is a small macOS menu bar utility for switching between your Codex accounts. You need the Codex desktop app installed and accounts that you already own.

This repository contains the macOS download and installation guide. Application source code is not included in this release.

## Release

- Release: `v3.3.18`
- Artifact: `Codex-Account-Switcher-macOS-Apple-Silicon.zip`
- Bundle version: `3.3` (build `18`)
- Architecture: Apple Silicon (`arm64`)
- Minimum macOS: `14.0`

The app is an independent utility. It is not affiliated with or endorsed by OpenAI.

## Install

1. Download `Codex-Account-Switcher-macOS-Apple-Silicon.zip` from the [latest release](https://github.com/kromate/codex-account-switcher/releases/latest).
2. Open the ZIP file.
3. Drag **Codex Account Switcher.app** to **Applications**.
4. Open the app from **Applications**.

**Distribution status:** this is a community build, ad hoc signed and not Apple-notarized. It is not a Developer ID-signed production release. macOS may block the first launch. If that happens, open **System Settings**, choose **Privacy & Security**, and approve the app there.

## Update an existing installation

Quit **Codex Account Switcher** from its menu bar menu, download the latest ZIP, and replace the app in **Applications**. Open the replacement app. Saved accounts stay in macOS Keychain; replacing the app does not remove them. macOS may ask you to allow the updated app to access them.

## macOS Keychain access

Saved logins stay in your Mac’s Keychain. The app requests access to **Codex Switcher — Saved account**. Enter your own Mac login Keychain password in the native macOS dialog, never in a chat or support message. Older entries may still display the original internal service identifier on their first access.

Version 3.3.18 reuses granted account credentials in memory for the current app session, rather than repeatedly requesting them during Refresh, Warm accounts, and switching. A denied request stops automatic retries; use **Reload saved accounts** when ready to try again. No plaintext credential cache is written to disk.

macOS may still ask once for each saved account, when Keychain is locked, or after an app update. **Allow** grants the requested access; **Always Allow** trusts that app for the item, if you choose to grant it. Ad hoc signing cannot guarantee that trust carries over to a new build.

## Warm accounts

Open **Accounts** and choose **Warm accounts** beside Refresh. Confirm to send one tiny request per saved ChatGPT account. The app shows each account’s result and refreshes usage afterward. You can cancel remaining requests.

This uses a small amount of each account’s Codex allowance. A successful request can start an unused usage window; OpenAI controls the actual timing. It does not reset an existing window or bypass an exhausted allowance. Expired logins and unavailable accounts are reported individually. Your active account, provider, and running Codex chats are not switched or restarted.

Warming is manual only, with no background schedule or automatic retry. It sends only a short request for an “OK” reply, with no project files, conversation history, or tools.

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
