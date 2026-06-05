# English to Hungarian Translation Skill for Claude

Translate English into idiomatic, native-sounding Hungarian instead of a literal, word-for-word calque. This is a drop-in [Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for Claude and Claude Code that fixes the Hungarian-specific structures generic AI translation gets wrong.

![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)
![Claude Skill](https://img.shields.io/badge/Claude-Agent%20Skill-7C3AED)
![Language pair](https://img.shields.io/badge/EN%20%E2%86%92%20HU-translation-success)
![Platform](https://img.shields.io/badge/Claude%20Code%20%7C%20API%20%7C%20Desktop-supported-informational)

## TL;DR

A skill that teaches Claude to translate English to Hungarian the way a native speaker writes, not the way a dictionary maps words. It encodes the error patterns that make English to Hungarian translation read as foreign: trailing time and place adverbials, definite vs. indefinite conjugation, English passives, false friends, and broken vowel harmony. Install in one line, then ask Claude to translate.

## Install in one line

```bash
curl -fsSL https://raw.githubusercontent.com/forint573/ENG-HUN-Translation-skill/main/translating-english-to-hungarian/SKILL.md --create-dirs -o ~/.claude/skills/translating-english-to-hungarian/SKILL.md
```

That drops the skill into your personal skills folder, so it works across every project. Restart Claude Code and it loads automatically. Windows PowerShell and manual options are in [Install](#install) below.

## What it does

Ask in plain language and you get back Hungarian, no commentary:

```
Translate to Hungarian: "The door is locked and the screen is broken."
→ Az ajtó be van zárva, és a képernyő be van törve.
```

It handles full documents, emails, UI strings, marketing copy, subtitles, or a single word. Paste English, get Hungarian. Claude picks up the skill on its own whenever a request looks like English to Hungarian translation, so you do not have to invoke anything by hand.

## Why this exists

Modern models already produce *grammatical* Hungarian. The problem is that grammatical and native are not the same thing. A sentence can parse cleanly and still read as obviously translated, because Hungarian organizes a sentence differently from English: it puts the emphasized word right before the verb, drops pronouns and the copula English insists on, and conjugates the verb based on whether its object is definite.

This skill is built on the recurring mistakes that show up when English becomes Hungarian, the kind that survive even careful human translation. Each rule targets one documented failure pattern and tells the model what a native speaker would write instead. The grammar behind those rules comes from reference grammars and real translation errors, not guesswork. The result is Hungarian that reads the way a native writes it, not Hungarian that merely parses.

A few of the patterns it corrects:

| English | Common calque | Native Hungarian |
|---------|---------------|------------------|
| Peter saw a cat in the garden yesterday. | Péter látott egy macskát a kertben tegnap. | **Péter tegnap a kertben látott egy macskát.** |
| The house is big. | A ház nagy van. | **A ház nagy.** |
| Mistakes were made. | Hibák voltak csinálva. | **Hibákat követtek el.** |
| I love you. | Szeretlek téged. | **Szeretlek.** |
| She is very sympathetic. | Nagyon szimpatikus. | **Nagyon együttérző.** |

The middle column is the trap: each one is the answer you get when you translate word by word. The right column is what the skill steers Claude toward.

### A full sentence, before and after

> **English:** The report was finished yesterday, and I'll send it to you tomorrow.
>
> **Word-for-word:** *A jelentés volt befejezve tegnap, és én fogom küldeni azt neked holnap.*
>
> **With this skill:** *A jelentés tegnap elkészült, és holnap elküldöm neked.*

Same meaning, but the second version moves the time word ahead of the verb, drops the unnecessary pronoun and the clumsy passive, and uses the present tense for a certain future. That is the gap between a translation that parses and one a Hungarian would actually write.

## What it covers

The skill works as a diagnostic, not a checklist, so it does not over-correct sentences that were already natural. It reaches for a rule only when the English structure is pulling the translation toward a calque. The areas it watches:

- **Topic and focus word order.** Trailing time and place adverbials move in front of the verb. The emphasized word takes the slot right before the verb.
- **Definite vs. indefinite conjugation.** Including the cases that catch non-natives: first and second person object pronouns, the special `I → you` form (*szeretlek*, *látlak*), and verbs of liking that take a generic definite object.
- **Dropped words.** Subject pronouns, the copula *van*, and the indefinite article *egy* come out far more often than English drops them.
- **English passives.** Rendered as a third-person-plural active (*kinyitották az ajtót*) or, for a resulting state, the *-va/-ve van* resultative (*be van zárva*).
- **Phrasal verbs and idioms.** Turned into coverb constructions (*give up* → *felad*), never translated piece by piece.
- **Register.** Consistent *te* or *ön* throughout, chosen to fit the context.
- **Vowel harmony.** Every suffix harmonizes with its stem, including the neutral-vowel stems that still take back suffixes.
- **False friends.** *sympathetic*, *eventually*, *actually*, *sensitive*, *realise*, and the rest of the words that look obvious and translate wrong.

## Usage

Once installed, use it the way you already talk to Claude:

- `Translate this email to Hungarian: ...`
- `How do you say "I am waiting for you" in Hungarian?`
- `Localize this landing page copy for a Hungarian audience.`
- Paste a block of English and ask for the Hungarian version.

It returns only the Hungarian translation, preserves paragraph breaks, lists, and bold or italic formatting, and leaves brand names, code, URLs, and placeholders untouched.

### Register: te vs. ön

Hungarian forces a formality choice English does not have. The skill keeps it consistent within a text and defaults to the formal *ön* when the context is genuinely ambiguous. If you want a specific register, say so: `translate to Hungarian, informal (te)`.

## Install

### One line (macOS, Linux, WSL, Git Bash)

```bash
curl -fsSL https://raw.githubusercontent.com/forint573/ENG-HUN-Translation-skill/main/translating-english-to-hungarian/SKILL.md --create-dirs -o ~/.claude/skills/translating-english-to-hungarian/SKILL.md
```

### Windows PowerShell

```powershell
$dir = "$HOME\.claude\skills\translating-english-to-hungarian"
New-Item -ItemType Directory -Force -Path $dir | Out-Null
Invoke-WebRequest -Uri "https://raw.githubusercontent.com/forint573/ENG-HUN-Translation-skill/main/translating-english-to-hungarian/SKILL.md" -OutFile "$dir\SKILL.md"
```

### Git clone

```bash
git clone https://github.com/forint573/ENG-HUN-Translation-skill.git
cp -r ENG-HUN-Translation-skill/translating-english-to-hungarian ~/.claude/skills/
```

### Per project instead of global

Swap `~/.claude/skills/` for `.claude/skills/` inside a project to scope the skill to that repo only.

### Claude API

Drop the contents of [`translating-english-to-hungarian/SKILL.md`](translating-english-to-hungarian/SKILL.md) into your system prompt, or load it as an Agent Skill if you run the Claude Agent SDK.

### Claude apps and other agents

In the Claude desktop and web apps, zip the `translating-english-to-hungarian` folder and upload it under Settings, Capabilities, Skills. The same `SKILL.md` layout works in any tool that follows the Agent Skills format, including Codex (`~/.codex/skills/`), Cursor, and the Gemini CLI: clone the folder into that tool's skills directory.

After installing, a new Claude Code session discovers the skill automatically. Claude loads it on its own when a request looks like English to Hungarian translation, and you can also call it by name with `/translating-english-to-hungarian`. To confirm it loaded, ask for a translation and check that the Hungarian reads naturally.

## FAQ

**How do I translate English to Hungarian with Claude Code?**
Install this skill with the one-line curl command above, then ask Claude to translate. It loads automatically whenever a request looks like English to Hungarian translation. No flags, no API key.

**How do I get Hungarian translations that sound native instead of machine-translated?**
Use this skill. It targets the structures generic translation gets wrong (topic-focus word order, definite vs. indefinite conjugation, dropped pronouns and copula, English passives, and false friends) so the output reads like a Hungarian wrote it.

**Why not just use a generic translation engine?**
General engines tend to produce Hungarian that is grammatical but foreign-shaped: English word order kept intact, the copula and pronouns left in, passives translated literally. This skill targets exactly those structures so the output reads like a Hungarian wrote it.

**Does it work for a single word or short phrase?**
Yes. For an ambiguous word it adds a short label to disambiguate, for example *asztal (bútor) / tábla (iskolai)* for "table."

**Which tools support it?**
Claude Code and the Claude desktop and web apps load it as an Agent Skill from your skills folder. For the Claude API, paste the skill into your system prompt or load it through the Agent SDK.

**Does it change how Claude handles other languages?**
No. The skill only activates for English to Hungarian translation requests.

**Is it free?**
Yes, released under the Apache License 2.0. Use it, fork it, ship it.

## How it works under the hood

The skill is a single `SKILL.md` file with YAML frontmatter. The `description` field tells Claude when to reach for it, and the body holds the translation rules. Claude reads the file, applies the relevant rules to your text, and returns the Hungarian. Nothing runs locally, there is no API key, and no data leaves your Claude session.

## License

Released under the [Apache License 2.0](LICENSE).

Copyright 2026 Virág Làzár Csaba ✸☽

## Keywords

English to Hungarian translation, translate English to Hungarian, AI Hungarian translation, idiomatic Hungarian, native Hungarian translation, magyar fordítás, angol-magyar fordító, angol magyar fordító, angol magyar fordito, magyar fordító, magyar fordito, Hungarian localization, Claude skill, Claude Code skill, Claude Agent Skill, machine translation Hungarian, English Hungarian translator.
