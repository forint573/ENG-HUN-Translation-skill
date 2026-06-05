---
name: translating-english-to-hungarian
description: Translates English into idiomatic, native-sounding Hungarian rather than literal calque. Use whenever the user asks to translate, localize, or render English text in Hungarian (emails, documents, UI strings, marketing copy, subtitles, or a single word or phrase), and also when the user simply pastes English and asks for the Hungarian version. Covers the structures naive translation gets wrong, including topic-focus word order, definite vs. indefinite conjugation, dropped pronouns and copula, English passives, phrasal verbs, register (te/ön), and false friends.
---

# English → Hungarian Translation

Produce idiomatic, native Hungarian — never a word-for-word calque of the English. Hungarian organizes information around a pre-verbal focus position, drops what English makes explicit, and conjugates verbs by the definiteness of their object. A literal rendering looks grammatical but reads unmistakably foreign.

## Operating principle (read first)

You already translate English→Hungarian competently. Most sentences come out natural if you simply re-express the *meaning* instead of the words. So:

- **Default to your own fluent Hungarian.** Do not mechanically run every rule below on every sentence — that produces over-corrected, stilted output (e.g. forcing focus-movement or a coverb construction where the plain version was already idiomatic). Over-application is as much a failure as calquing.
- **Reach for the rules as a diagnostic** when the English structure is actively pulling you toward a calque: passives, dummy *it*, *there is/are*, rigid SVO order, phrasal verbs, or ambiguous register.
- **The self-check at the end is a safety net**, not a per-sentence checklist. Apply it when a draft sentence still "feels English-shaped."

## Method

1. Read the whole passage for meaning, tone, and intent.
2. Hold the meaning; drop the English wording.
3. Re-express in Hungarian — freely restructure, split, or merge sentences around topic–focus–verb.
4. Read your Hungarian aloud; fix anything a native would not say.

## Failure modes to catch

### Word order: neutral order vs. the pre-verbal focus slot
Neutral sentences — no special emphasis — are often the *same* order as English (subject–verb–object): *Tamás eszi az almát.* (Tamás is eating the apple.) Don't reorder a sentence that is already neutral and natural. Two things break the English parallel:

- **Trailing time/place adverbials.** English tacks them onto the end; Hungarian normally places them *before* the verb. This is the single most common calque.
  - Peter saw a cat in the garden yesterday.
  - calque: *Péter látott egy macskát a kertben tegnap.*
  - natural: **Péter tegnap a kertben látott egy macskát.**
- **Emphasis / contrast.** Whatever is emphasized — the answer to an implicit *who/what/where?*, or an English *it was X that…* cleft — moves into the slot **immediately before the verb**, and any coverb is pushed after the verb.
  - It was PÉTER who ate the apple. → **PÉTER ette meg az almát.** (neutral: *Péter megette az almát.*)

### Drop what Hungarian does not need
- **Subject pronouns** — omit unless emphatic: *It is raining.* → **Esik.** (never *Az esik.*); *I love it.* → **Imádom.** (drop *azt* unless it is emphatic or contrastive)
- **Copula van/vannak** — omit with predicate adjectives or nouns in 3rd-person present: *The house is big.* → **A ház nagy.** (never *…nagy van.*). Keep it for **location** and **existence**: *The cup is on the table.* → **A csésze az asztalon van.**
- **There is/are** → sentence-initial **Van/Vannak**, never *Ott van*: *There is a book on the table.* → **Van egy könyv az asztalon.**
- **Indefinite article egy** — drop far more often than English uses *a/an*: *I am a doctor.* → **Orvos vagyok.** (not *Egy orvos vagyok.*)

### Definite vs. indefinite conjugation
Match the verb to its object. This is one of the most audible non-native errors.

| Object | Conjugation | Example |
|--------|-------------|---------|
| none, or indefinite (*egy*, *valami*, *valaki*, bare plural) | indefinite | *Látok egy fát.* (I see a tree) · *Fákat látok.* (I see trees) |
| definite article / proper name / possessive / demonstrative / 3rd-person pronoun (*őt, azt, őket*) | definite | *Látom a fát.* (I see the tree) · *Látom őt.* (I see her) |

Three cases a literal approach gets wrong:
- **1st/2nd person object pronouns take the *indefinite* conjugation**, even though *me/you/us* feel definite: *Látsz engem.* (You see me.) · *Ők látnak titeket.* (They see you all.)
- **But "I → you" has its own special definite form, *-lak/-lek*** — extremely common, so don't miss it: *Szeretlek.* (I love you.) · *Látlak.* (I see you.) · *Várlak.* (I'm waiting for you.) Used only when the subject is *I* and the object is *you* (singular or plural).
- **Verbs of liking/knowing take a generic object with the definite article + definite conjugation**, where English uses a bare noun: *Szeretem a kávét.* (I like coffee.) — not *Szeretek kávét.*

### English passive → Hungarian active or resultative
Hungarian has no generalized syntactic passive. Choose by what the English passive actually describes:

- **An action or event** (something happened; the agent is unstated) → **3rd-person-plural active**:
  - Mistakes were made. → **Hibákat követtek el.**
  - The door was opened. → **Kinyitották az ajtót.**
  - The newspaper was already read. → **Az újságot már elolvasták.**
- **A resulting state** (English is/are + participle, describing a condition) → the ***-va/-ve van* resultative**, the closest Hungarian equivalent of the English passive:
  - The door is locked. → **Az ajtó be van zárva.**
  - The window is closed. → **Az ablak be van csukva.**
  - The screen is broken. → **A képernyő be van törve.**

Note the contrast: *the door was opened* (event) → **kinyitották**, but *the door is locked* (state) → **be van zárva**. Cautions: *-va/-ve van* only works with certain telic transitive verbs — when it sounds off, use the 3rd-plural active instead (*A könyvet megírták*, not *A könyv meg van írva*). Use a lexical middle/anticausative only where idiomatic for that verb (*eltörik* — breaks, *elromlik* — breaks down, *kinyílik* — opens); don't manufacture *-ódik/-ődik* forms as a generic passive. Avoid the archaic *-tatik/-tetik* passive (*megméretik*) outside deliberately literary or legal text.

### Future tense
Hungarian commonly uses the **present** for scheduled or certain future; reserve **fog + infinitive** for emphasis or uncertainty.
- I will call you tomorrow. → **Holnap hívlak.** (present)
- It will probably rain. → **Valószínűleg esni fog.**

### Connector placement — do not calque English position
| English | calque | natural |
|---------|--------|---------|
| without commuting | *…anélkül, hogy ingázna* | **Anélkül, hogy ingázna, …** (front) |
| even if it rains | *Elmegyek, még ha esik is* | **Még ha esik is, elmegyek.** |
| for example | *…, for example, …* | move early, often no comma: **Amikor például otthonról dolgozol…** |

Always: *not only … but also* → **nemcsak … hanem … is** (never *de … is*).

### Phrasal verbs and idioms → coverb constructions, never word-for-word
| English | calque | native |
|---------|--------|--------|
| look for | *néz …-ért* | **keres** |
| give up | *ad fel* | **felad** |
| it's raining heavily | *esik keményen* | **szakad az eső** |

Coverb placement carries aspect and direction: **pre-verbal** in neutral sentences, **post-verbal** under negation or focus.
- I found it. → **Megtaláltam.**  ·  I didn't find it. → **Nem találtam meg.**

### Possession: possessor first
- Peter's book → **Péter könyve**
- the window of the house → **a ház ablaka**
- I have a book → **Van egy könyvem.** (dative possessor + *van* + possessed noun with suffix)

### Register: te vs. ön
| Context | Choice |
|---------|--------|
| casual, friends, peers | *te / ti* |
| professional, public, formal | *ön / önök* (verb in 3rd person) |

Keep it consistent within a single text. When context is genuinely ambiguous, default to **ön/önök**.

### Vowel harmony
Every suffix must harmonize with its stem: back-vowel stems take back suffixes (*ház-ban*), front-vowel stems take front (*kert-ben*), with front-rounded variants where they exist (*-hoz / -hez / -höz*). The vowels *i, í, e, é* are neutral — some stems containing only these still take **back** suffixes (*híd → hidak*, *férfi → férfiak*), so follow the attested form rather than guessing. A single disharmonic suffix marks the text as non-native.

## False friends
| English | wrong | correct |
|---------|-------|---------|
| sympathetic | *szimpatikus* (means *likeable*) | **együttérző** |
| eventually | *eventuálisan* (means *possibly / contingently*) | **végül / végül is** (*idővel* only for the "over time" sense) |
| actually | *aktuálisan* (means *currently*) | **valójában / tulajdonképpen** |
| sensitive | *szenzitív* | **érzékeny** |
| realise | *realizál* (means *implement / realize a profit*) | **rájön / felismer** |

## Output format
- Return **only** the Hungarian translation — no commentary, no notes.
- **Single word / short phrase:** give the equivalent; if ambiguous, add a short disambiguating label in parentheses, e.g. *asztal (bútor) / tábla (iskolai).*
- **Longer text:** preserve paragraph breaks, lists, bold, and italics.
- Leave brand names, code, URLs, and placeholders unchanged.

## Self-check (run when a sentence still feels English-shaped)
1. Would a native say this, unprompted?
2. Removed unnecessary *azt / őt / egy / van*?
3. Emphasized element immediately before the verb? Time/place adverbials moved off the end?
4. *without / even if / for example* moved to their natural positions?
5. Phrasal verbs and idioms rendered as coverb constructions, not calqued?
6. Conjugation correct for every verb — including 1st/2nd-person objects (*indefinite*) and the I→you *-lak/-lek* form?
7. English passives rendered as 3rd-plural active, or as *-va/-ve van* where they describe a state?
8. Register (te/ön) consistent and appropriate?
9. Vowel harmony correct on every suffix?
