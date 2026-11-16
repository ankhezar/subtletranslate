# SubtleTranslate Privacy Policy

**Effective Date:** November 16, 2026  
**Developer:** Anton Mykhailets (`app.subtletranslate.mac`)

SubtleTranslate is designed from the ground up as a local-first, privacy-preserving macOS translation utility. We do not operate any backend proxy servers, user accounts, analytics trackers, or advertising SDKs.

## 1. Data We Collect
**None.** SubtleTranslate collects **zero** personal data, telemetry, crash analytics, usage logs, or browsing history on developer-owned servers.

## 2. How Translation Text Is Processed
Depending on the translation mode you choose in **Settings**:
- **Offline Packs (`TranslateGemma`) & Built-in macOS Translation:** All language detection and translation inference execute **100% locally on your Mac** (Apple Silicon Metal / macOS `Translation` framework). Zero text leaves your device.
- **Optional Cloud Mode (Bring-Your-Own-Key Google Gemini API):** If you choose to enter your own Google Gemini API key in **Settings → Cloud Key**, text you explicitly request to translate is sent directly from your Mac over TLS 1.3 (`https://generativelanguage.googleapis.com`) to Google's Gemini API under your own Google account and API terms. Your API key is stored exclusively inside your Mac's encrypted **macOS Keychain** (`kSecAttrAccessibleWhenUnlockedThisDeviceOnly`) and is never transmitted anywhere else.

## 3. Clipboard, Accessibility & Browser Extensions
- **Explicit Trigger Only:** SubtleTranslate reads selected or copied text **only** when you explicitly invoke translation (e.g., pressing `⌘C` twice, pressing your configured global shortcut `⌥⌘T`, choosing `Services ▸ Translate with SubtleTranslate`, or clicking `Translate with SubtleTranslate` in the Safari / Chrome browser context menu).
- **Password Manager Protection:** SubtleTranslate automatically detects and ignores concealed clipboard items (`org.nspasteboard.ConcealedType`, 1Password, Apple Passwords, Bitwarden) so sensitive credentials are never read or translated.
- **Browser Companion Extensions (Safari & Chrome/Brave/Arc):** The browser extensions use `contextMenus` and `activeTab` solely to pass the text you explicitly highlight and click to the local `SubtleTranslate.app` running on `127.0.0.1` / `subtletranslate://`. They never read background tabs, cookies, or browsing history.

## 4. Local History & Model Storage
Recent translation history and optional downloaded `.gguf` offline language models are stored locally on your Mac inside `~/Library/Application Support/SubtleTranslate/` with user-only file permissions (`0600` / `0700`). You can clear your history or remove offline models at any time from within the app.

## 5. Contact
For privacy questions or support, contact: `ankhezar@gmail.com`
