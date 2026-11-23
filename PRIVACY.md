# Subtle Privacy Policy

**Effective Date:** November 20, 2026  
**Application:** Subtle — Instant Translator (`SubtleTranslate.app`, `app.subtletranslate.mac`)  
**Developer:** Anton Mykhailets

**Subtle** is designed from the ground up as a local-first, privacy-preserving macOS translation utility. We do not operate any translation proxy servers, user accounts, analytics trackers, or advertising SDKs.

## 1. Data We Collect
**None.** Subtle collects **zero** personal data, translation text, telemetry, crash analytics, usage logs, or browsing history on developer-owned servers.

## 2. How Translation Text & Speech Are Processed
Depending on the translation mode you choose in **Settings**:
- **Offline Packs (`TranslateGemma` & `Supertonic-3`), Built-in macOS Translation & Local Speech (`Core ML` / `AVSpeechSynthesizer`):** All language detection (`FastText lid.176.ftz` + `NaturalLanguage`), local translation inference (Apple Silicon Metal / macOS `Translation` framework), and offline `🔊` text-to-speech playback (`Supertonic-3 Core ML` or macOS `AVSpeechSynthesizer`) execute **100% locally on your Mac**. Zero text or audio leaves your device.
- **Optional Cloud Mode (Bring-Your-Own-Key Cloud Translation & Voice Providers):** Only after you explicitly configure an API key and grant in-app permission in **Settings → Cloud** (or Onboarding), text you explicitly request to translate—or click `🔊` to pronounce—in Cloud or Hybrid mode is sent directly from your Mac over TLS 1.2+ / TLS 1.3 to the provider(s) you selected and authorized—such as **Google Gemini** (`generativelanguage.googleapis.com`), **DeepL API** (`api-free.deepl.com` / `api.deepl.com`), **Microsoft Azure Translator** (`api.cognitive.microsofttranslator.com`), **Groq** (`api.groq.com`), **Mistral AI** (`api.mistral.ai`), **OpenRouter** (`openrouter.ai`), or your custom **OpenAI-Compatible** endpoint (`api.openai.com`)—under your own account and that provider's terms and privacy policy. Your API keys are stored exclusively inside your Mac's encrypted **macOS Keychain** (`kSecAttrAccessibleWhenUnlockedThisDeviceOnly`), never pass through developer servers, and can be revoked/removed with one click at any time.

## 3. Clipboard, Accessibility & Browser Extensions
- **Explicit Trigger Only:** Subtle reads selected or copied text **only** when you explicitly invoke translation (e.g., pressing `⌘C` twice, pressing your configured global shortcut `⌥⌘T`, choosing `Services ▸ Translate with Subtle`, or clicking `Translate with Subtle` in the Safari / Chrome browser context menu).
- **Password Manager Protection:** Subtle automatically detects and ignores concealed clipboard items (`org.nspasteboard.ConcealedType`, 1Password, Apple Passwords, Bitwarden) so sensitive credentials are never read or translated.
- **Browser Companion Extensions (Safari & Chrome/Brave/Arc):** The browser extensions use `contextMenus`, `activeTab`, `scripting`, `storage`, `alarms`, and `nativeMessaging` on Safari (encrypted locally via `AES-256-GCM` Keychain-authenticated IPC; loopback `http://127.0.0.1:49178/*` on Chrome), with optional per-site `optional_host_permissions` requested strictly if you enable the opt-in `[S]` selection pill, solely to pass webpage text or images you explicitly select or toggle (`Bilingual Page` / `Translate Image Text`) to the local `SubtleTranslate.app` on your Mac. They never read background tabs, cookies, or browsing history.

## 4. Optional Offline Model Downloads & Software Updates
- **Offline AI & Neural Voice Model Downloads (`Settings → Offline`):** Only when you click **Download** on an optional `TranslateGemma` offline translation pack or the optional `Supertonic-3 v2 CoreML` Natural Voice Pack, your Mac downloads SHA-256-verified model weights over HTTPS from static CDN mirrors (**Cloudflare R2** `models.subtletranslate.app` or **Hugging Face** `huggingface.co`). No translation text or personal identifiers are transmitted.
- **Standalone App Updates (`Sparkle 2`, Direct Download Only):** The direct-download Standalone edition periodically fetches the static signed `appcast.xml` feed from **GitHub Releases** (`github.com/ankhezar/subtletranslate`) to check for new versions; standard HTTPS request metadata is processed by GitHub under GitHub's Privacy Statement. The **Mac App Store** edition contains zero Sparkle update code and updates exclusively through Apple's Mac App Store.

- **Mac App Store Purchases (`StoreKit 2`):** On the Mac App Store edition, the 14-day `Subtle Pro` trial and optional one-time `Subtle Pro` unlock (`app.subtletranslate.mac.pro`) are verified on-device through Apple's signed `StoreKit 2` framework without developer receipt servers.

## 5. Local History & Model Storage
Recent translation history (`history.json`, bounded to `5,000` items / `10 MB`) and optional downloaded offline translation (`.gguf`) and neural voice (`CoreML`) models are stored locally on your Mac inside `~/Library/Application Support/SubtleTranslate/` with user-only file permissions (`0600` / `0700`) and excluded from unencrypted backups where supported. You can pause recent history logging (`Keep Recent History`), clear individual or all unpinned history items, or remove offline models at any time from within the app.

## 6. Contact
For privacy questions or support, contact: `support@subtletranslate.app`
