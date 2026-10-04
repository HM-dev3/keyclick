# Keyclick 1.0.0 — First Public Release

## Highlights

Make physical keys and shortcuts sound like yours. Import WAV sounds, record and edit voice in Voice Studio, capture guided sets, and generate offline Voice Packs from installed Windows voices. Profiles, Smart Voice playback, Actions, tray operation, opt-in start with Windows, and output recovery are included.

## System requirements

Windows 10 22H2 (build 19045) x64 or Windows 11 x64; an audio output device; Microsoft Edge WebView2 Runtime for the interface. Native ARM64 and Windows 8/8.1 are not supported. Recording requires a microphone; speech generation requires a suitable installed Windows voice.

## Privacy

Physical key identities and audio are handled locally. Keyclick does not intentionally reconstruct typed text, keep a key history, upload keypresses, read clipboard content, or require an account. Privacy Guard is on and Strict by default, but relies on Windows and each app's accessibility information. See [PRIVACY.md](../../PRIVACY.md).

## Known limitations

- Password-field detection depends on Windows accessibility providers and asynchronous focus notifications. Strict mode silences unclassified fields; no universal protection guarantee is claimed.
- The installer needs internet access if WebView2 is absent because it uses the Evergreen bootstrapper. An offline installer is not included.
- Code signing is not configured, so Windows may warn about an unknown publisher.
- Native ARM64 and macOS builds are not included. Acoustic latency has not been instrumentally measured.

## Installation and support

Run `Keyclick_1.0.0_x64-setup.exe`. The installer checks the OS and WebView2 before first app launch. Autostart is opt-in. Uninstall removes app files and its startup registration while preserving user-created profiles and audio under `%APPDATA%\com.keyclick.desktop`.

For support, use [GitHub issues](https://github.com/HM-dev3/keyclick/issues). Report security issues privately as described in [SECURITY.md](../../SECURITY.md).
