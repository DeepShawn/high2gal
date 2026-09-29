# The Last Class — v3.10: Classroom in Four Languages

Open `index.html` in a browser. It contains the complete game, styles, question bank, offline translations and generated scenes. No game dependencies, online translation service or CDN is required. Desktop layout is the default; Settings → Phone layout reflows the interface for smaller screens. Fullscreen: the button or `Alt + Enter`; pause: `Esc`.

## Language and speech

Choose Simplified Chinese, Traditional Chinese, English or Japanese from Language on the main menu or Settings. This release replaces the old English-core presentation: complete dialogue, questions and explanations, tutorials, character profiles, records, endings and system text use the new catalogue.

English sentences and vocabulary that are the actual material being tested remain in English. Question instructions and explanations follow the chosen language. Formulae, numbers, keyboard controls, identifiers and correct-answer positions remain unchanged. Switching languages does not redraw questions or refill timers. Dialogue is translated as a complete line before the typewriter reveals it.

Speech is **off by default**. Enable Dialogue speech in the four-language panel. Four availability cards let you preview local Mandarin (`zh-CN`), Taiwan Mandarin (`zh-TW` preferred), English and Japanese voices. Voices come from the device/browser, not bundled recordings. If a matching local voice is missing, the game keeps the complete text and shows a notice. It does not substitute another language, download a voice, imitate a real person or access your microphone.

Changing language, advancing dialogue, pausing or leaving the page cancels old speech. Late voice availability cannot resurrect a cancelled line. Device voice quality and availability vary; local matching and utterance routing are tested with voice doubles, not a guarantee that every device has all four voices installed.

## Realistic Mode English lessons

In a run started with Realistic Mode enabled, the English lesson's opening, classroom interface, questions and dialogue temporarily use English. Speech follows English **only if already enabled**. This does not overwrite your preferred language. Changing the language selector during the lesson chooses the language to return to afterward.

Other lessons, breaks, offices, homecoming, escape and menus restore your preference. Loading a save inside a Realistic English lesson resumes the same override. Ordinary-mode English lessons still respect your preference, aside from the English-language material being examined.

## Saves and existing game

The 1,036 academic entries (including parameter variants and 75 number grids), 48 endings and 174 achievements are retained. Study/Casual, difficulty, seven-day campaigns, homecoming, confiscation, chess, sports, relationships and reaction mechanics are unchanged.

Export a JSON backup in the previous release and import it here. Existing question text, option order, answer index, remaining time and campaign state stay canonical. The new Japanese preference can be saved and exported. Browser storage is not cloud storage; keep a JSON backup before changing browsers or files.

## Development and verification

`tools/build.py` rebuilds the self-contained HTML offline from the preserved v3.9 base, authored English/Japanese TSV catalogue, extra translations and ICU Traditional Chinese conversion. Building requires Python, BeautifulSoup4 and ICU `uconv`; playing does not. Tests require Playwright and Chromium.

See the Chinese test report and JSON results for exact checks. Automated structural coverage is not native-editor proofreading or teacher review of every question. Mobile hardware, browser-specific speech quality and other untested platforms are not represented as verified.
