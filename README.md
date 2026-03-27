# 🇨🇭 Swiss Humanizer — Claude Skill

A Claude skill that removes AI writing patterns from text and adapts it to Swiss conventions. Think of it as a two-in-one editor: it strips the tell-tale signs of generated content *and* makes the result feel like it was written by someone who actually lives in Switzerland.

---

## What it does

**Swiss conventions applied:**

- Currency → `CHF 1'500.–` (apostrophe thousands separator, dash for round amounts)
- Quotation marks → `«guillemets»` instead of `"English quotes"` or `„German quotes"`
- No ß → `ss` throughout (`Strasse`, `gross`, `heissen`) — the hard Swiss rule
- Date/time → `27.03.2026`, `14:30 Uhr`
- Geography → Zürich, Bern, Basel, Luzern as example cities, not London or New York
- Swiss vocabulary → Velo, Trottoir, Coiffeur, parkieren, Glacé, etc.
- Address and phone format → `PLZ Ort`, `+41 44 123 45 67`

**AI patterns removed:**

- Significance inflation: *testament, pivotal, underscores, evolving landscape*
- Promotional language: *nestled, vibrant, breathtaking, boasts, state-of-the-art*
- Swiss-specific clichés: *nestled in the Alps, land of chocolate and watches, precision engineering, heart of Europe*
- Vague attributions: *Experts argue, Studies show, Industry observers note*
- Em dash (Gedankenstrich) overuse — replaced with commas or restructured sentences
- Emojis — removed entirely
- Rule of three, negative parallelism, filler phrases, bold overuse
- Chatbot artifacts: *Of course!, I hope this helps, Let me know if...*

---

## Before / After

**Before (AI-generated):**

> Nestled at the heart of Europe, Switzerland — with its breathtaking landscapes and world-renowned precision — stands as a testament to what a nation can achieve. The Swiss financial sector, boasting assets of over $2,000,000,000,000 💰, is a pivotal player in the global economy, highlighting Switzerland's crucial role as a hub for international capital flows. Experts argue that growth will continue, contributing to Switzerland's evolving economic landscape.

**After (Swiss Humanizer):**

> Der Schweizer Finanzsektor verwaltete 2023 rund CHF 7'900 Milliarden an Kundenvermögen, mehr als das Zehnfache des Schweizer BIP. Das macht ihn zu einem der grössten Finanzzentren der Welt. Die wichtigsten Standorte sind Zürich und Genf: Zürich dominiert bei Vermögensverwaltung und Versicherungen; Genf konzentriert sich auf Private Banking und internationale Kunden.

---

## Installation

### Claude (Cowork / Claude Code)

1. Download or clone this repository
2. Copy the `swiss-humanizer` folder into your `.claude/skills/` directory:

```
.claude/
└── skills/
    └── swiss-humanizer/
        └── SKILL.md
```

3. The skill will be available automatically in your next session. Just ask Claude to «humanize this for a Swiss audience» or «remove AI patterns and apply Swiss style».

### ChatGPT / Manus / other AI tools

The skill is written as a Claude skill, but the rules work with any AI. Copy the contents of `SKILL.md` and paste them into:

- **ChatGPT** → *Customize ChatGPT* → *Custom Instructions*
- **Manus** → System prompt or task instructions
- **Any other LLM** → Paste as a system prompt before your request

The Swiss conventions section, the AI pattern list, and the before/after examples all transfer directly.

---

## Usage examples

Once installed in Claude, you can trigger it with natural language:

- *«Humanize this text for a Swiss audience»*
- *«Remove the AI writing patterns and make this sound Swiss»*
- *«Apply Swiss style to this — CHF, guillemets, no emojis»*
- *«Clean up this press release for a Swiss reader»*
- *«Swissify this»*

---

## What's in the repo

```
swiss-humanizer/
├── SKILL.md      # The full skill — conventions, patterns, examples, process
└── README.md     # This file
```

---

## Contributing

Spotted a Swiss convention that's missing? A typical AI cliché about Switzerland that should be added? Pull requests are welcome. Particularly useful additions would be:

- French-speaking Switzerland (Romandie) conventions
- Italian-speaking Switzerland (Ticino) conventions
- Industry-specific Swiss terminology (finance, pharma, medtech)
- Additional Swiss vocabulary entries

---

## Background

This skill is inspired by and builds on the English humanizer skill pattern, adding a Swiss-specific layer on top. The base humanizer approach was developed by the Claude community to remove the telltale patterns that make AI-generated text recognisable.

Swiss typography and writing conventions referenced: SN 040001, Schweizer Schreibweise (no ß, apostrophe thousands separator), Duden Schweiz.

---

## License

MIT — free to use, share, and adapt.

---

## Author

Created by **Daniel Stump** & AI — [Studio Quark](https://www.quark.ch).
