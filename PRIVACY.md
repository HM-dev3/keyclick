# Keyclick privacy

Keyclick processes physical keyboard events locally to trigger the sounds and Actions you configure. It does not intentionally reconstruct typed text, store a keystroke history, upload keypresses, inspect clipboard contents, or require an account. Profiles and managed audio files stay in the user's application-data directory. No analytics or cloud TTS is used.

Voice Studio opens a microphone stream only after you explicitly start recording. Unsaved takes are kept in memory while you edit them; saved recordings become local audio files. Voice Pack generation uses speech voices installed in Windows and runs locally.

Privacy Guard is on by default. It asks Windows whether the focused field is a password field and suppresses keyboard-triggered sounds when Windows reports a protected field. It also silences unclassified fields under the default Strict policy. Windows accessibility providers can omit or misreport this property, and focus notifications are asynchronous, so Keyclick cannot guarantee protection in every application. You can choose Standard mode or turn Guard off in Settings; both choices reduce protection. Deliberate in-app previews are separate from global typing feedback.

Keyclick does not send telemetry. The optional startup benchmark writes local timing and machine-resource measurements only when explicitly invoked by a tester. See [the technical privacy model](docs/privacy-model.md) for implementation details.
