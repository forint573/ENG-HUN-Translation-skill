# English → Hungarian Translator

A Claude [Agent Skill](https://agentskills.io) that translates English into idiomatic, native-sounding Hungarian — not the grammatical-but-foreign calque that naive translation produces.

https://claude.ai/public/artifacts/ec2055e0-1060-4eed-9a39-2de83ef2e149

Hungarian is structurally very far from English: it organizes sentences around a pre-verbal focus position, drops words English makes explicit, conjugates verbs by the definiteness of their object, and has no general passive. A word-for-word rendering reads as unmistakably non-native. This skill encodes the specific structures that go wrong so the output sounds like a Hungarian speaker actually wrote it.

## What it fixes

| Failure mode | Calque (wrong) | Native |
|---|---|---|
| Trailing time/place adverbials | *Péter látott egy macskát a kertben tegnap.* | **Péter tegnap a kertben látott egy macskát.** |
| Unnecessary articles / pronouns | *Egy orvos vagyok.* | **Orvos vagyok.** ("I am a doctor") |
| The *I → you* verb form | *Szeretek téged.* | **Szeretlek.** ("I love you") |
| Eventive passive → active | *Hibák lettek elkövetve.* | **Hibákat követtek el.** ("Mistakes were made") |
| Stative passive → resultative | *Az ajtó zárva van téve.* | **Az ajtó be van zárva.** ("The door is locked") |
| Phrasal verbs → coverbs | *ad fel* | **felad** ("give up") |
| False friends | *eventuálisan* (= *possibly*) | **végül** ("eventually") |

It also covers definite vs. indefinite conjugation (including the counterintuitive rule that first/second-person object pronouns take the *indefinite* form), present-tense future, connector placement (*without / even if / for example*), possessive order, the *te* vs. *ön* register distinction, and vowel harmony.

### Before / after

> **English:** The report was finished yesterday, and I'll send it to you tomorrow.
>
> **Naive:** *A jelentés volt befejezve tegnap, és én fogom küldeni azt neked holnap.*
>
> **This skill:** *A jelentés tegnap elkészült, és holnap elküldöm neked.*

## Design

The skill is built for capable models. Rather than re-teaching Hungarian from scratch, it leans on the model's existing fluency and intervenes only on the known failure modes above — and it explicitly warns against over-correction, since mechanically forcing every rule onto already-natural sentences produces output as stilted as a calque. The grammar claims are grounded in reference grammars and linguistic sources, not vibes.

## Installation

The skill is a standard `SKILL.md` directory, so it works anywhere that supports the Agent Skills format.

**Claude Code** (filesystem-based, auto-discovered):

```bash
# Personal — available in every project
git clone https://github.com/<your-username>/translating-english-to-hungarian \
  ~/.claude/skills/translating-english-to-hungarian

# Or project-scoped — commit it to your repo to share with the team
git clone https://github.com/<your-username>/translating-english-to-hungarian \
  .claude/skills/translating-english-to-hungarian
```

Start a new session afterward. Claude loads the skill automatically when relevant; you can also invoke it directly with `/translating-english-to-hungarian`. The folder must contain `SKILL.md` at its top level.

**claude.ai / Claude apps:** enable code execution under Settings → Capabilities (or Org settings → Skills), then go to Customize → Skills and upload the skill as a ZIP.

**Claude API / Platform:** upload via the [Skills API](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) (`/v1/skills`).

**Other agents:** the same `SKILL.md` works in tools that implement the standard (e.g. Codex at `~/.codex/skills/`, Cursor, Gemini CLI). Clone the folder into that tool's skills directory.

See [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) and the [Claude Code skills docs](https://code.claude.com/docs/en/skills) for details.

## Usage

Skills are model-invoked: once installed, just ask in plain language.

```
Translate this into Hungarian: "We'll let you know once the order ships."
```

```
How do you say "I've been waiting for you all morning" in Hungarian?
```

```
Localize this signup form copy for a Hungarian audience, keeping it informal (te).
```

It triggers on requests to translate, localize, or render English in Hungarian — including a single word or phrase, and including the case where you simply paste English text and ask for the Hungarian.

## Repository structure

```
translating-english-to-hungarian/
├── SKILL.md      # the skill: instructions Claude loads
└── README.md     # this file
```

`SKILL.md` is the only file the model reads. Its YAML frontmatter (`name`, `description`) is what Claude uses to decide when the skill applies; the Markdown body is loaded when it triggers.

## Scope and limitations

- **One direction.** English → Hungarian only.
- **It's guidance, not a guarantee.** This shapes how the model translates; final quality depends on the underlying model. It's tuned for recent frontier models — on weaker models the "trust your fluency" framing may under-deliver.
- **Not for high-stakes text.** It is not a substitute for a professional human translator on legal, medical, or literary work where errors carry real cost.

## Contributing

Issues and pull requests are welcome — especially counterexamples. If you find a sentence the skill gets wrong (or over-corrects), open an issue with the English input, the Hungarian it produced, and the Hungarian you expected. Concrete failing cases are the most useful thing for improving a translation skill.

## License

MIT — use freely, modify, share.
