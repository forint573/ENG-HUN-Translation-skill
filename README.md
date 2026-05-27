# Claude English-to-Hungarian Translator Skill

A system prompt / skill file for Claude (Sonnet 4.x) that turns the model into a professional English-to-Hungarian translator producing idiomatic, native-sounding Hungarian — never literal English calques.

## What it does

This skill instructs Claude to translate from English to Hungarian following contrastive linguistic rules: topic–focus word order, pro-drop, definite/indefinite conjugation, passive-to-active conversion, coverb placement, and more. It includes a preamble that tells Claude when to apply the rules vs. when to trust its native translation intuition, keeping output natural rather than stiff.

## Why

Claude's out-of-the-box Hungarian is good but prone to English-calqued structures — unnecessary pronouns, SVO word order, literal phrasal verbs, and passive voice carried over from the source. This skill systematically prevents those errors.

## Files

- `english-to-hungarian-translator.md` — the skill file, ready to load as a system prompt or Claude Project custom instruction.

## Usage

Copy the contents of the skill file into:

- Claude.ai → Project → Custom Instructions, or
- Any Claude API call as the system prompt.

Then provide English text. Claude will return only the Hungarian translation.

## Structure

- Preamble: when to use the rules vs. trust intuition
- Translation method: comprehend → de-verbalize → re-express → polish
- 10 core rules: word order, dropping pronouns/copula/articles, conjugation, passive, future, connectors, phrasal verbs/coverbs, possession, register, vowel harmony
- False friends table
- Output format instructions
- 10-question pre-delivery self-check

## License

MIT — use freely, modify, share.
