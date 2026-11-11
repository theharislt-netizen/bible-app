# Bible App

Live site: https://theharislt-netizen.github.io/bible-app/ (GitHub Pages, branch `main`). Single-file `index.html` plus `lt.js` (Lithuanian) and `bible/*.json` (reader versions).
To edit text/photos: open the site with `?admin` on the end, tap the pencil, edit, press Save.

**READ THIS FILE FIRST in every new chat, and before any task on this app.** These are Haris's standing rules. Follow them without being asked again. The original rules document (Claude doc "Bible App Rules: How We Build Everything") is kept in sync with this file; this README is the one to follow.

## 0. Rule for ALL new content: every language

Every new or edited article, evidence entry, news item, timeline entry, quiz, label, button text or other page text must be written in ALL languages the website offers (currently English and Lithuanian) before it is published. When a language is added, all new content is written in it too, and the reader version follows the site language.

- English strings live in `index.html`; Lithuanian versions live in `lt.js` (English text -> Lithuanian text, exact-match dictionary). Any new or changed English string needs a matching `lt.js` entry, and bump `lt.js?v=N` in `index.html` when `lt.js` changes.
- Lithuanian Bible verse references use Lithuanian book abbreviations (Mt, Mk, Lk, Jn, Apd, Apr, Pr, Iš ...).
- **Never translate scripture yourself.** Bible quotes in Lithuanian must be the exact text of the Lithuanian Bible in the reader (Lietuvos Biblijos draugija, Rubšys–Kavaliauskas, `bible/lbd.*.json`). English uses the World English Bible (WEB).
- Reader version follows site language by default (Lithuanian -> LBD, English -> WEB); the user can still pick any version.

## 1. How to talk to Haris

- Answer exactly what he asked. No extra background, no unrequested info, no ending with "do you want me to...?" questions. Decide and do. Short answers.
- He often uses voice typing, so messages can be garbled. Read for intent, not wording.
- If he is only thinking out loud with no question, do not reply.
- Never assume he is upset. He is friendly and blunt, swears and banters. Correct him when he is wrong and say so when you disagree.
- Metric units only (centimetres, metres, km). Money in euros.
- For factual questions, look it up first. Never guess.
- "Finish" means finish. Do not hand back a half-done version and call it done. If something truly cannot be sourced, apply the fallback rules below instead of leaving a gap.
- When he says "do it", start working immediately. Do not repeat the plan back.
- When you must ask, ask one question at a time (he is sometimes driving; questions should work by voice).
- No unrequested changes.

## 2. What is being built

A Bible-explainer app (phone-first) on GitHub Pages: Return Timeline, News, Evidence, Passages Explained, Bible reader, quizzes. Evidence entries are built from Expedition Bible (Joel Kramer) video transcripts. Each new video means: build the entry (in all languages), test it, push it, and update the Photos Needed doc. The old Claude artifact is only a backup.

## 3. The source standard (the golden standard)

Every claim, anywhere in the app, needs a source a reader can open with one tap. This covers Evidence entries, older cards and news articles. If someone broke an arm, a king died or a city burned, that claim has a source.

Order of sources, best first:
1. The real document: excavation report, museum page, ancient text translation, journal article, official site.
2. If no real document can be found online, a Wikipedia page about the subject.
3. If there is no Wikipedia page either, the Expedition Bible video. That is the only time the video is the source.

Never link the video as a shortcut when a real source exists. Never link a page that only points back to the Bible. Never use a retracted paper (the 2021 Tall el-Hammam airburst paper was retracted in April 2025; the text says so).

- **Bible and outside sources together:** when the Bible says something and an outside source also backs it, show both: the verse and the outside source, checkable in one tap.
- **One source covering several events gets one marker.**

## 4. How sources look in the app

- **Bible references: red**, dotted underline. Tapping opens the bottom panel with the verse text (WEB in English, LBD in Lithuanian), word for word. Every verse reference anywhere in the app is tappable.
- **Outside sources: small blue numbers** at the end of a paragraph or bullet, not highlighted phrases. Tapping opens the source in a new tab. Two sources = two numbers side by side.
- **The same source keeps the same number** throughout a card. Each card ends with a numbered **References** list showing every source once.
- **Video-only claims** carry a small "▶ video" marker linking to the video, used only where the video is the only source (e.g. Kramer's own eyewitness moments, the geologist's remark).
- **The Antichrist article** (News: "Is the Antichrist / Jewish Messiah here?", red heifer and Yeshua ben David) is Haris's own work. Never touch it. It carries its own video links.
- The separate parked "Ben David" news story is a different thing. Decide later.
- Photo captions and credits are required; photo credit label is "Credit" (English) / "Nuotrauka" (Lithuanian).

## 5. How to write the text

- Reads like a professional article, not a transcript of the video.
- Where a real source backs a claim, state it as fact. Do not write "Kramer says" or "he said".
- Use "Kramer" or "in the video" only for his opinions, conclusions and personal observations, or where the video is the only source.
- Write in your own words. Expedition Bible is the ultimate source: do not cross-check it or call anything debated, but still attribute and link.
- Transcript oddities (numbers, names) are caption errors: use standard spellings, convert miles to km and feet to metres.

## 6. How an Evidence entry is built

- **One story is one entry**, however long. Split only genuinely separate stories. Several videos about one story (David's tomb parts 1 and 2) are one entry with all videos as sources.
- Each entry has: a collapsed Bible verse box (tappable, in the order the explanation mentions the verses, with a play button that reads them aloud in the bottom player), a short explanation, and the evidence as a full understandable story.
- **Pictures at the exact spot.** Anything that can be shown is a photo at the paragraph it proves. Rhythm: text, photo, text, photo. Never two photos back to back. Minimum number of photos that still carries each step.
- Where a diagram or map can be drawn, draw a labelled schematic.
- Decide categories, length and photo spots yourself.
- Categories: Archaeology, History and writings, Prophecies (in that order). An entry can sit in more than one.
- **Photo placeholders stay.** Haris sources photos himself; empty placeholders show where each goes. Do not remove or hide them.
- Photos Needed doc ("Expedition Bible: Photos Needed"): a section per video, table of Status and What-it-must-show per photo, plus a section for older cards. Update whenever photo spots change.

## 7. Standing rules for the whole app

- **Bible text:** exact, word for word, never paraphrased, plain modern English (World English Bible), zero mistakes.
- **Share and read-aloud:** every News story, Evidence entry, Timeline entry and Passages Explained entry has a universal share icon (an icon, not the word) and a read-aloud play button.
  - Share copies the real GitHub Pages link to that exact item.
  - The bottom player bar appears only while reading and disappears fully on stop. It hides only when the user scrolls down by hand and returns on scroll up. When the page scrolls itself during read-aloud, the player buttons (pause, skip, speed, voice cog, stop) stay visible. Changing speed never restarts the reading.
  - Tap chip "Read from here" shows its label only the first time on a device, then only ▶. The label is translated.
  - Voice: the app auto-picks the best available voice (prefers natural/neural); the cog lets the user override voice and speed. No pre-recorded audio and no in-browser neural models (phone-first).
  - Reading behaves like a music player: silent audio holds the audio session (stops other music), Media Session shows lock-screen controls (play/pause/next/previous), reading continues when the app is minimised or the tab changes, and on a call or interruption it pauses and keeps its exact place.
- **Home screen:** News first, then Evidence, then the rest. All cards same size with a one-line description. Buttons that do not work yet are grayed out showing only their name, never "coming soon".

## 8. News rules

- Strictly Bible news: archaeology finds and manuscript discoveries. Ongoing topics are one entry with dated updates added over time. Stories are added manually.
- Each update names its source with a link and says plainly what is claimed and by whom.
- Articles read like professional journalism, one flowing line: no AI-voice commentary about sources or what could not be verified, no repeated "he said", no repeated facts, no hedging notes aimed at the reader. Facts and sources are laid out and readers judge.
- Confirmed items that bear on the Bible also go into Evidence, with photos. Unconfirmed ones (e.g. Noah's Ark) stay out of Evidence.
- Each story has a Follow (bell) button that does nothing for now.
- Dates use the site language's format.

## 9. Evidence page rules

- Three categories in order: Archaeology, History and writings, Prophecies.
- Entries read like a book: Next and Back within the category, swipe, read entries marked, "Continue reading" button inside each category list.
- Every entry resting on a prophecy shows its Bible verses in an expandable box, collapsed by default with a clear expand cue, followed by how it turned out.
- Line charts only for fact data with long real series (wars since 1946, internet use, Jewish population). No charts for trends the data does not show.
- Entries are named after the evidence itself (e.g. "The Cyrus Cylinder"), not combined names and not timeline event names.

## 10. Publishing and testing

- Work in this repo; push to `main` (GitHub Pages rebuilds in ~2 min). Before pushing: `git fetch && git rebase origin/main`. Several chats work in this repo, so pull the latest before every push and only touch what your task covers (e.g. the photo chat only touches photos/evidence content).
- Always test before pushing: open every route in English and Lithuanian, no script errors, no "undefined", no empty links, no broken images, every red verse opens, photo order has no adjacent photos.
- After pushing, say plainly what is done and what is not. Do not claim finished when it is not.

## 11. Completed entries (reference)

Pishon river, Nineveh and Sennacherib (with Lachish), Sodom and Gomorrah, Tomb of Amenhotep II, Silver scrolls of Ketef Hinnom, Tomb of Jesus, Jericho, Babylon Today, Burning Sulfur, King David's tomb, standing stone of Shechem, Tower of Babel. Older cards: Cyrus, Pilate, Jeremiah, Dia, Ophel, Aqueduct, plus the teaching cards. Open item: the "third rock" in the Pishon story has no real name.
