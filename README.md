# YASMIN AI – Setup (beginner friendly)

## A. Build the APK with GitHub (no Android Studio needed)
1. Create a free account on github.com → **New repository** → name it `YasminAI` → Create.
2. On your computer, unzip this project. In the repo click **Add file → Upload files**, drag ALL
   contents of the unzipped folder (including the hidden `.github` folder) and **Commit**.
   (If `.github` does not upload by drag & drop: Add file → Create new file → type
   `.github/workflows/build.yml` and paste the file's content.)
3. Open the **Actions** tab → "Build APK" → wait ~5–8 min for a green tick
   (or click **Run workflow** if it didn't start).
4. Click the finished run → **Artifacts → yasmin-debug-apk** → download, unzip → `app-debug.apk`.
5. Send the APK to your phone, tap it, allow "Install unknown apps".

## B. First run
1. Get a free key: https://aistudio.google.com/apikey → paste in Settings → Gemini API Key.
2. Settings → Permissions → Microphone → Allow.
3. Settings → Accessibility → Open → Installed apps → YASMIN AI → ON.
   If greyed out: phone Settings → Apps → YASMIN AI → ⋮ → **Allow restricted settings**, retry.
4. Settings → Voice: tap Voice 1, 2, 3… to find a female voice. Raise pitch for a softer voice.
5. Say "Hey Yasmin, Instagram kholo" (app open, screen on) or tap the 🎤 for continuous talk.

## C. If the build fails (red cross)
Open the failed run → click the red step → copy the first lines containing `error:` or `e: ` and
send them to Claude. It will give you the exact fix.

## D. Honest limitations
- Wake word works only while the app is open on screen (Android blocks silent background mic for normal apps).
  When YASMIN opens another app, listening pauses until you return.
- Interrupting by voice while she speaks is not implemented (her own voice would trigger the mic).
  Tap the orb to stop her.
- "Close apps" = Home/Back only; Android does not let apps kill other apps.
- YouTube "play": opens search results and taps the first video (best effort; may need retry).
  Pause/next use media keys.
- Instagram: scroll/like/search work through accessibility taps on visible text; UI changes can break them.
- WhatsApp sending, email, smart home, camera vision, PC sync: NOT implemented yet.
- Web search opens Google in the browser; weather uses wttr.in; news uses Google News RSS.
- Calculator/translation/coding are done by Gemini itself.
- Notifications permission is requestable but the app doesn't post notifications yet.
- Not compiled in my sandbox (no internet there). If GitHub shows a compile error, send it to me.
