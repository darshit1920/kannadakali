# KannadaKali (ಕನ್ನಡ ಕಲಿ) — Learn Kannada by living it

Built for the **Kannada Digital Innovation Hackathon 2026** (theme: *Code. Create. Celebrate Kannada.*)
**Problem statement:** Kannada for Everyone

KannadaKali helps non-Kannada speakers learn practical Kannada through everyday situations instead of textbook lists.

## Features
- **6 real-life scenes, 30 phrases:** Auto & Travel, Market, Restaurant, Hospital, Bus & Metro, Workplace
- **Kannada script + easy pronunciation + English meaning** for every phrase (pronunciation can be toggled off)
- **Voice playback** using the browser's speech synthesis (`kn-IN`), slowed down for learners
- **Quiz mode:** 5 questions per run, by scene or mixed across all scenes
- **Speak mode:** say the phrase into the mic; speech recognition (`kn-IN`) scores how close you were
- **Progress:** XP, daily streak, and learned-phrase progress bars saved in `localStorage`
- Mobile-first, light/dark theme, no login, no backend, no data leaves your device

## Tech stack
Vanilla HTML, CSS and JavaScript in a single file (`index.html`), Web Speech API (SpeechSynthesis and SpeechRecognition), `localStorage`.

## Run locally
```bash
git clone https://github.com/<your-username>/kannadakali.git
cd kannadakali
python3 -m http.server 8000   # or just open index.html
```
Open http://localhost:8000. Voice recognition works best in Chrome or Edge. For audio, install a Kannada text-to-speech voice in your OS if none is present.

## Deploy
- **Vercel:** import the repo, framework preset "Other", no build command.
- **Netlify:** drag and drop the folder at app.netlify.com/drop, or connect the repo.

## Add or fix phrases
Phrases live in the `S` array at the top of the script in `index.html`. Each phrase is `[kannadaScript, pronunciation, english]`. Pull requests that add scenes, regional variants, or corrections from native speakers are very welcome.

## Roadmap
- More scenes (banking, schools, government offices)
- Regional dialect packs contributed by the community
- AI-generated adaptive lessons and multilingual dataset support
- Installable offline PWA

## License
MIT
