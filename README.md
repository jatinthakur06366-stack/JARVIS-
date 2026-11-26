# JARVIS Mobile Prototype

## Phone-only setup
1. Extract this ZIP into a folder named `JARVIS`.
2. Host the folder on an HTTPS static host (for example, a private GitHub Pages project or another static host). A local `file://` preview may not allow microphone access or service workers.
3. Open the HTTPS site in Chrome on your Samsung Galaxy M15.
4. Expand **Settings & Connection**, paste your Gemini API key, and tap **Connect Gemini**.
5. Tap **Install app** / Chrome menu > **Install app** (or **Add to Home screen**, depending on Chrome).
6. Open JARVIS from the home screen and grant microphone permission.

## Gemini key
Create/manage a key in Google AI Studio: https://aistudio.google.com/app/apikey

This starter calls Gemini `gemini-3.8-flash` from the browser for a personal prototype. This is NOT safe for a public app: browser code and requests can expose the key. Do not publish the project with a real key in it, share the key, or commit it to a public repository. Use a server-side proxy or Firebase AI Logic before public release. Review usage and billing controls in AI Studio.

## Voice notes
Speech recognition availability depends on the browser/device and may use the device's configured recognition service. The app requests `en-IN`. Android text-to-speech uses installed system voices; a male-sounding voice may not exist on every phone. Install/configure an English voice in Android Settings > General management > Text-to-speech output if needed.

## Current limitations
- Tap-to-talk, not always-on wake-word listening.
- The browser app can speak answers and open supported web links, but cannot freely control Android settings or launch every installed app.
- For deeper Android integration, build a native Android app with Kotlin and explicit Android permissions.
