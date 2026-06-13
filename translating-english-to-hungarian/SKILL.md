---
name: translating-english-to-hungarian
description: Translates English into idiomatic, native-sounding Hungarian rather than literal calque. Use whenever the user asks to translate, localize, or render English text in Hungarian (emails, documents, UI strings, marketing copy, subtitles, or a single word or phrase), and also when the user simply pastes English and asks for the Hungarian version. Covers the structures naive translation gets wrong, including topic–focus word order, definite vs. indefinite conjugation, dropped pronouns and copula, English passives, phrasal verbs and coverb aspect, English prepositions vs. Hungarian case suffixes and postpositions, articles, numerals, possession and have-constructions, comparison, modality and the conditional, register (te/ön), false friends, and Hungarian punctuation, date, number and capitalization conventions.
---

# English → Hungarian Translation

Produce idiomatic, native Hungarian — never a word-for-word calque of the English. Hungarian organizes information around a pre-verbal focus position, drops what English makes explicit, conjugates verbs by the definiteness of their object, and glues onto the noun (as case suffixes) most of what English puts in front of it (as prepositions). A literal rendering looks grammatical but reads unmistakably foreign.

## Operating principle (read first)

You already translate English→Hungarian competently. Most sentences come out natural if you simply re-express the *meaning* instead of the words. So:

- **Default to your own fluent Hungarian.** Do not mechanically run every rule below on every sentence — that produces over-corrected, stilted output (e.g. forcing focus-movement, a coverb, or a dative-possessor construction where the plain version was already idiomatic). Over-application is as much a failure as calquing.
- **Reach for the rules as a diagnostic** when the English structure is actively pulling you toward a calque: passives, dummy *it*, *there is/are*, rigid SVO order, trailing adverbials, phrasal verbs, prepositions, English punctuation, or ambiguous register.
- **The self-check at the end is a safety net**, not a per-sentence checklist. Apply it when a draft sentence still "feels English-shaped."
- **Depth on demand.** This file is the diagnostic core and is self-sufficient. Full paradigm tables (every conjugation, the complete case and postposition inventory) live in `reference/grammar-tables.md`, and the complete style, formatting, and false-friend lists in `reference/style-lexicon.md`. Consult them when you need an exhaustive table; you usually won't.

## Method

1. Read the whole passage for meaning, tone, register, and intent.
2. Hold the meaning; drop the English wording.
3. Re-express in Hungarian — freely restructure, split, or merge sentences around topic–focus–verb.
4. Read your Hungarian aloud; fix anything a native would not say.

---

## Word order and information structure

Neutral sentences — no special emphasis — are often the *same* order as English (subject–verb–object): *Éva szereti a virágokat.* (Eve likes the flowers.) · *Tamás eszi az almát.* (Tamás is eating the apple.) Don't reorder a sentence that is already neutral and natural. What breaks the English parallel:

**Trailing time/place adverbials.** English tacks them onto the end; Hungarian normally places them *before* the verb (and time before place). This is the single most common calque.
- Peter saw a cat in the garden yesterday.
- calque: *Péter látott egy macskát a kertben tegnap.*
- natural: **Péter tegnap a kertben látott egy macskát.**

**The pre-verbal focus slot.** Whatever is emphasized — the answer to an implicit *who/what/where?*, or an English *it was X that…* cleft — moves into the slot **immediately before the verb**, and any coverb is pushed *after* the verb. Hungarian has no *it*-cleft; don't translate "it was…that" literally.
- It was PÉTER who ate the apple. → **PÉTER ette meg az almát.** (neutral: *Péter megette az almát.*)
- It was the BOOK I read (not the paper). → **A könyvet olvastam el.**

**Bare (article-less) object → S–O–V.** A non-specific object with no article often sits right before the verb and forms a unit with it: *Peter is writing a letter.* → **Péter levelet ír.** (vs. *Péter ír egy levelet*, which counts "a [single] letter").

**Quantifiers are not focus.** *minden* (every), *mindenki* (everyone), *mindig* (always), *sok* (many) sit pre-verbally but **keep the coverb attached** — unlike focus, they do not invert it.
- Everyone watched the film. → **Mindenki megnézte a filmet.** (not *…nézte meg…*)

**Questions take no do-support and no auxiliary inversion.**
- *Wh*-questions put the question word in the focus slot (coverb inverts): What is the boy eating? → **Mit eszik a fiú?** · Where are you going? → **Hová mész?**
- *Yes/no* questions keep statement order, marked by intonation; in formal/embedded use, the enclitic **-e** on the verb = "whether/if": Is he reading? → **Olvas?** · I don't know if he's coming. → **Nem tudom, hogy jön-e.**

## Negation, and the particles *is* / *sem*

- ***nem*** immediately precedes the verb (or the focus it negates) and, like focus, **pushes the coverb after the verb**: I didn't read it. → **Nem olvastam el.** (not *Nem elolvastam.*)
- **Negative concord is obligatory** — the "double negative" is correct. An n-word (*senki* nobody, *semmi* nothing, *soha* never, *sehol* nowhere) **must** co-occur with *nem*/*sem*: Nobody helps me. → **Senki nem segít nekem.** / **Senki sem segít nekem.** · I see nothing. → **Nem látok semmit.**
- ***nem* + 3rd-person *van*/*vannak* merges into *nincs* / *nincsenek*** (and *sincs* under *sem*): There is no coffee. → **Nincs kávé.** (never *nem van*).
- The negative imperative uses **ne**, not *nem*: Don't go! → **Ne menj!**
- ***is*** ("too/also") is an enclitic that **hugs the word it adds**, never floating to the clause end like English: I saw Peter too. → **Pétert is láttam.** · Me too. → **Én is.**
- Under negation, *is* → ***sem*** ("either/neither"): I'm not coming either. → **Én sem jövök.** Scalar "even" = **még … is**: Even Peter came. → **Még Péter is eljött.**

## Drop what Hungarian does not need

- **Subject pronouns** — omit unless emphatic/contrastive: *It is raining.* → **Esik.** · *I love it.* → **Imádom.** · *She loves her job.* → **Szereti a munkáját.** (not *Ő szereti az ő munkáját*).
- **Copula *van/vannak*** — omit with predicate adjectives/nouns in the 3rd-person present: *The house is big.* → **A ház nagy.** (never *…nagy van.*) But **keep it for location and existence**: *The cup is on the table.* → **A csésze az asztalon van.** And it is **never dropped in the future**: *He will be a doctor.* → **Orvos lesz.** (not *Ő fog orvos lenni*).
- **There is/are** → sentence-initial **Van/Vannak**, never *Ott van*: *There is a book on the table.* → **Van egy könyv az asztalon.**
- **Indefinite article *egy*** — drop far more often than English *a/an*, especially before a predicate noun/profession: *I am a doctor.* → **Orvos vagyok.** (not *Egy orvos vagyok.*) Keep *egy* only when it genuinely means "one / a certain": *I saw only one man.* → **Csak egy embert láttam.**
- **Redundant possessives** — the possessive suffix already marks the owner: *I washed my hands.* → **Megmostam a kezem.** (not *az én kezeimet*).

## Definite vs. indefinite conjugation

Match the verb to the **grammatical form** of its object (not its meaning). This is one of the most audible non-native errors.

| Object is… | Conjugation | Example |
|---|---|---|
| absent, or indefinite: *egy*, bare noun/plural, *sok/néhány/két*, **minden + N**, *valamit/valakit*, *mit/kit*, *semmit/senkit*, **and 1st/2nd-person pronoun objects** (*engem, téged, minket, titeket*) | **indefinite** | *Látok egy fát.* · *Fákat látok.* · *Mit látsz?* · *Látok valamit.* · *Ismerek minden titkot.* · *Látsz engem.* |
| definite: *a/az* + N, proper name, possessive-suffixed N, demonstrative (*ezt/azt a…*), 3rd-person pronoun (*őt, azt, őket*), reflexive (*magát*), *melyiket / mindegyiket / valamennyit / mind*, **a *hogy*-clause**, and **formal *önt*** | **definite** | *Látom a fát.* · *Látom őt.* · *Ismerem a titkodat.* · *Melyiket kéred?* · *Tudom, hogy jössz.* · *Látom Önt.* |

Cases a literal approach gets wrong:
- **1st/2nd-person object pronouns take the *indefinite* conjugation**, even though *me/you/us* feel definite: *You see me.* → **Látsz engem.**
- **But "I → you" has its own special form, *-lak/-lek*** — extremely common: *I love you.* → **Szeretlek.** · *I'm waiting for you.* → **Várlak.** · past: *I saw you.* → **Láttalak.** Used only when the subject is *I* and the object is *you*.
- **The quantifier trap:** *minden* (every), *mindenki* (everyone), *mindent* (everything) take the **indefinite** conjugation — *I know everyone here.* → **Mindenkit ismerek.** (not *ismerem*) — whereas *mindegyik / valamennyi / mind / az összes* (each/all) take the **definite**: *I'll take all of them.* → **Mindegyiket kérem.** A possessive suffix overrides this and forces **definite**: *I know your every secret.* → **Ismerem minden titkodat.**
- **Verbs of liking/knowing take a generic object with the definite article + definite conjugation**, where English uses a bare noun: *I like coffee.* → **Szeretem a kávét.** (not *Szeretek kávét.*)

Full paradigms (present/past, definite/indefinite, *-lak/-lek*): see `reference/grammar-tables.md`.

## Coverbs and aspect

Coverbs (*igekötők*: *meg, el, fel, le, be, ki, át, oda, vissza, rá, össze, szét*…) carry **direction** and **aspect**. A bare verb is imperfective/atelic (a process); a coverb usually makes it perfective/telic (completed, with a result). English often packs that completion into a particle ("eat **up**", "read **through**") or a result verb ("find", "kill") — Hungarian needs an explicit coverb, or it reads as unfinished.

| English (result/completion) | bare = wrong/atelic | native (coverb) |
|---|---|---|
| I read the (whole) book. | *Olvastam a könyvet.* ("was reading") | **Elolvastam a könyvet.** |
| I ate the apple (up). | *Ettem az almát.* | **Megettem az almát.** |
| I found my coat. | *Találtam a kabátomat.* (stumbled on) | **Megtaláltam a kabátomat.** |
| I passed the exam. | *Elmentem a vizsgán.* (= left) | **Átmentem a vizsgán.** |

Also turn phrasal verbs and idioms into coverb constructions, never word-for-word: *give up* → **felad** (not *ad fel* as two words in the neutral form); *look for* → **keres**; *it's raining heavily* → **szakad az eső**.

**Placement carries aspect and is the load-bearing rule:** the coverb is **pre-verbal (attached)** in neutral affirmatives and plain yes/no questions, and **post-verbal (separated)** under negation, focus, *wh*-questions, and the imperative.
- I found it. → **Megtaláltam.** · I didn't find it. → **Nem találtam meg.** · Find it! → **Találd meg!**

## English passive → Hungarian active or resultative

Hungarian has no generalized syntactic passive. Choose by what the English passive actually describes:

- **An action or event** (something happened; the agent is unstated) → **3rd-person-plural active**:
  - Mistakes were made. → **Hibákat követtek el.**
  - The door was opened. → **Kinyitották az ajtót.**
  - The newspaper was already read. → **Az újságot már elolvasták.**
- **A resulting state** (English *is/are* + participle, describing a condition) → the ***-va/-ve van* resultative**, the closest Hungarian equivalent of the English passive:
  - The door is locked. → **Az ajtó be van zárva.**
  - The screen is broken. → **A képernyő be van törve.**

Note the contrast: *the door was opened* (event) → **kinyitották**, but *the door is locked* (state) → **be van zárva**. Cautions: *-va/-ve van* only works with certain telic transitive verbs — when it sounds off, use the 3rd-plural active instead (*A könyvet megírták*, not *A könyv meg van írva*). Use a lexical middle/anticausative only where idiomatic (*eltörik* — breaks, *elromlik* — breaks down, *kinyílik* — opens); don't manufacture *-ódik/-ődik* forms as a generic passive. Avoid the archaic *-tatik/-tetik* passive (*megméretik*) outside deliberately literary or legal text.

## English prepositions → Hungarian case suffixes and postpositions

English uses separate words *before* the noun (in, on, to, from, with, for); Hungarian uses **suffixes glued after** the noun, or **postpositions placed after** it. There is almost never a separate word for "in/on/to/from". Reaching for one is a major calque. Location is a **3×3 system**: interior / surface / proximity, each crossed with static / motion-to / motion-from.

| | in/at (static) | to/into (motion to) | from (motion from) |
|---|---|---|---|
| **interior** (inside) | -ban/-ben | -ba/-be | -ból/-ből |
| **surface** (on) | -on/-en/-ön | -ra/-re | -ról/-ről |
| **proximity** (by / at a person) | -nál/-nél | -hoz/-hez/-höz | -tól/-től |

Where Hungarian's choice **defies English intuition** (high-value traps):
- on the bus/train → **a buszon / a vonaton** (surface, not *-ban*); getting on → **felszállok a buszra**; getting off → **leszállok a buszról**.
- at the doctor's → **az orvosnál**; (going) to the doctor's → **az orvoshoz**; from the doctor's → **az orvostól** (a *person* takes the proximity series).
- in the picture → **a képen**; at the university → **az egyetemen**; in the street → **az utcán** (surface).
- Hungarian towns and "Hungary" take the **surface** series — in/to/from Budapest → **Budapesten / Budapestre / Budapestről**; in Hungary → **Magyarországon** — but foreign places take **interior**: in London / in Germany → **Londonban / Németországban**.

Other high-frequency mappings: object **-t** (*almát*); "to/for" + possessor **-nak/-nek** (*Péternek*); "with / by (means)" **-val/-vel** (*késsel, vonattal*); "about (a topic)" **-ról/-ről** (*a háborúról*); "for the sake of" **-ért** (*pénzért*); "until/for (duration)" **-ig** (*hat óráig*); "as (in the role of)" **-ként** (*tanárként*); "at (clock time)" **-kor** (*ötkor*). Note "for" splits (**-ért** / **-nak,-nek** / verb-governed **-ra,-re**: *várok rád*), and "with" splits into instrumental **-val/-vel** vs. the postposition **együtt**.

**Postpositions follow the noun** (most take the bare nominative): *az asztal alatt* (under the table), *a ház mögött* (behind the house), *ebéd után* (after lunch), *szerinted* (according to you), *nélküled* (without you). With a pronoun they take personal endings — **alattam** (under me), **szerintem** (in my opinion), **miatta** (because of it) — never *alatt én*.

**Demonstrative agreement** (very common error): in *this/that + noun*, the demonstrative takes the **same case** as the noun **and** the article *a/az* stays between them. The *-z* assimilates.
- in this house → **ebben a házban** (not *ez a házban*) · to that city → **abba a városba** · on this table → **ezen az asztalon** · about that film → **arról a filmről**.

**Time expressions** split four ways: clock time **-kor** (*ötkor*); days take superessive **-n** (*hétfőn*, *pénteken*; but *vasárnap* bare); months/years take inessive (*januárban*, *2020-ban*); parts of day are bare adverbs (*reggel*, *este*).

The full case inventory, place-name rules, and complete postposition tables (directional triples, case-governing ones, personal forms): see `reference/grammar-tables.md`.

## Tense and the future

Hungarian has only **past** and **present**. For the future, use the **present** for scheduled or certain events; reserve **fog + infinitive** for emphasis or uncertainty.
- I'll call you tomorrow. → **Holnap hívlak.** (present)
- It will probably rain. → **Valószínűleg esni fog.**

There is **no progressive aspect** — one present form covers "I read" and "I am reading"; mark ongoing action with **éppen/most** if needed: *I'm reading right now.* → **Éppen olvasok.** (never a *van* + participle construction).

## Conditional, "if"-clauses, and English "would"

- Present conditional = **-na/-ne/-ná/-né** (1sg indefinite is always **-nék**, never *-nák*). Past conditional = **past tense + invariant *volna***: I would have written. → **Írtam volna.**
- ***ha* ("if") puts the conditional in BOTH clauses** (English uses past in the *if*-clause, conditional only in the main one):
  - If I had money, I'd buy a car. → **Ha lenne pénzem, vennék egy autót.** (not *Ha volt pénzem…*)
  - If I had had money, I'd have bought a car. → **Ha lett volna pénzem, vettem volna egy autót.**
- English "would" is often **not** the Hungarian conditional:
  - past habit ("we would go every summer" = used to) → **past tense** or *szokott*: **Nyaranta a tengerhez jártunk.**
  - reported speech ("he said he would come") → **present**, no backshift: **Azt mondta, hogy jön.**
  - polite "I would like" → fixed **szeretnék**: *I'd like a coffee.* → **Szeretnék egy kávét.**

## Imperative / subjunctive and "want someone to…"

The imperative and subjunctive share the **-j-** form. The coverb goes **after** the verb (*Ülj le!* — Sit down!; *Ne ülj le!* — Don't sit down!). The big structural pitfall: English "want/ask/tell someone **to** do X" is **not** an infinitive in Hungarian when the subjects differ — it is **azt + hogy + subjunctive**:
- I want you to go. → **Azt akarom, hogy menj.** (not *Akarlak menni*)
- Tell him to come. → **Mondd meg neki, hogy jöjjön.**

(When the subject is the *same*, the infinitive is correct: *I want to go.* → **El akarok menni.**) "Let me/him…" = **hadd** + subjunctive (*Hadd lássam!*); "let's…" = the 1st-person-plural form (*Menjünk!*). Assimilation and irregular imperatives: see `reference/grammar-tables.md`.

## Modality (can / must / may / should / would like)

- **must / have to** = **kell** + **dative** + **inflected infinitive** (the infinitive itself takes a personal ending; *kell* stays invariant): I have to go. → **(Nekem) el kell mennem.** · Ági has to go. → **Áginak el kell mennie.** · past: **El kellett mennem.**
- **should / ought to** = **kellene / kéne** (+ inflected infinitive): You should study. → **Tanulnod kellene.**
- English "can" splits: **tud** = learned ability / "know how" (*I can swim.* → **Tudok úszni.**); **-hat/-het** = possibility or **permission** (*May I sit down?* → **Leülhetek?**, not *Tudok leülni?*); **képes** = capable of (*Képes vagyok rá.*).
- **may / might / it's possible** → **-hat/-het** or **lehet (, hogy)**; **be allowed/forbidden** → **szabad / tilos** (*Szabad bejönni?* · *Tilos dohányozni.*).

## The noun phrase

**Articles.** Hungarian uses the definite article *a/az* where English drops "the", and drops *egy* where English keeps "a":
- generic/abstract nouns take *a/az*: *I like music.* → **Szeretem a zenét.** · *Love is wonderful.* → **A szerelem csodálatos.**
- possessed nouns and body parts take *a/az*: *my book* → **a könyvem**; *My head hurts.* → **Fáj a fejem.**
- superlatives take *a/az*: *the best* → **a legjobb**.
- a demonstrative requires the article: *this chair* → **ez a szék** (not *ez szék*).
- rivers/lakes/mountains take it: **a Duna, a Balaton, a Kárpátok**; most countries/towns/people do **not**: *Magyarország, Budapest, Károly* — but plural/compound country names do: **az Egyesült Államok, a Cseh Köztársaság, a Fülöp-szigetek**.
- *a/az* is chosen by **sound**, not spelling: *a ház*, *az alma*, *az USA* (read with an initial vowel).

**Number.** After a numeral or quantifier the noun stays **singular** (the quantity is already marked): two cats → **két macska** (not *macskák*); many people → **sok ember** (not *emberek*); every child → **minden gyerek**.

**Adjectives.** An attributive adjective (before the noun) does **not** agree; a predicative one (after "to be") **does**: *red apples* → **piros almák** (singular *piros*) but *The apples are red.* → **Az almák pirosak.** Adjectives from place names are lowercase: *budapesti, vidéki*.

**Comparison.** Comparative = **-bb/-abb/-ebb**, superlative = **leg-** + comparative (with *a/az*): *faster* → **gyorsabb**; *the fastest* → **a leggyorsabb**. Irregulars: *jó→jobb, nagy→nagyobb, sok→több, kicsi→kisebb, szép→szebb*. "Than" = **-nál/-nél** *or* **mint + nominative** (never accusative): *taller than me* → **magasabb nálam** / **magasabb, mint én** (not *mint engem*). "As…as" = **olyan … mint**. Never calque "more X" as two words — it is one suffixed word (*szebb*, not *több szép*).

**Possession.** Possessor first, with the possessive suffix on the *possessed* noun: *Peter's book* → **Péter könyve**; *the window of the house* → **a ház ablaka**. The emphatic/disambiguating form uses the **dative**: **Péternek a könyve** (obligatory with demonstratives: *annak a háznak az ablaka*).

**"Have"** — there is **no verb "to have"**. Possession = **dative possessor + *van/nincs* + possessed noun with a possessive suffix**:
- I have a dog. → **Van egy kutyám.** · I have no money. → **Nincs pénzem.** · Peter has a car. → **Péternek van autója.** · I have friends. → **Vannak barátaim.**

Possessive suffix paradigms and the *-é* form (*Ez a könyv Péteré.*): see `reference/grammar-tables.md`.

## Register: te / ön / maga / tetszik

Hungarian forces a formality choice English lacks. Keep it **consistent** across the whole text (pronouns, verbs, possessives, imperatives).

| Context | Choice | Verb agreement |
|---|---|---|
| casual: friends, peers, children, family | *te / ti* | 2nd person |
| professional, public, formal — the safe default | *ön / önök* | **3rd person** (*Ön tudja*) |
| *maga / maguk* | **avoid in formal writing** — can sound cold or rude; never to an elder/superior | 3rd person |
| warm deference (to elders) | *tetszik* + infinitive | *Hogy tetszik lenni?* |

A formal pronoun therefore takes a 3rd-person verb: *You (formal) speak Hungarian.* → **Ön beszél magyarul.** (not *Ön beszélsz*). Soften commands to *ön* with the conditional or *legyen szíves*: *Close the window.* → **Becsukná az ablakot?** / **Legyen szíves becsukni az ablakot.** When the register is genuinely ambiguous, default to **ön/önök**. Greetings and sign-offs by register, and salutation punctuation (*Tisztelt Kovács Úr!* — with "!"): see `reference/style-lexicon.md`.

## Punctuation, capitalization, dates, and numbers

These are absent from English source text and are a major tell of machine translation. Apply them in prose; leave code, URLs, and placeholders untouched.

- **Quotation marks:** Hungarian uses **„low-opening and high-closing”** — **„idézet”**, not English "…". Nested quotes use reversed guillemets: **„kint »bent« kint”**.
- **Decimal comma, space thousands:** `1,234.56` → **1 234,56**; `3.5%` → **3,5%**. Currency unit follows, after a space: **1 000 Ft**, **20 €**.
- **Dates are descending with periods:** *June 13, 2026* → **2026. június 13.** (lowercase month, trailing period). "On [date]" attaches a suffix and drops the period: **2026. június 13-án**; "on the 1st" → **1-jén**.
- **Capitalization is far lighter than English** — lowercase for months, days, languages, nationalities, holidays, and "I": *I speak English and German.* → **Beszélek angolul és németül.** Headings use sentence case: *Privacy Policy* → **Adatvédelmi irányelvek**. In letters, the polite **Ön** is capitalized as a courtesy.
- **Commas:** always put a comma before **hogy** and before clause-introducers **aki/ami/amely/mert/ha/mint** (even where English omits it): *I think that it's good.* → **Azt gondolom, hogy jó.** Do **not** put a comma before **és/vagy** joining a simple list: **kenyér, tej és tojás**.
- **Suffix on a numeral/acronym/foreign word via a hyphen:** **5-kor** (at 5), **EU-ban** (in the EU), **20%-kal** (by 20%).
- **"Billion" = *milliárd* (10⁹), not *billió*** (which is 10¹², i.e. "trillion") — a catastrophic error in finance: *$5 billion* → **5 milliárd dollár**. Use the **24-hour clock** (*14.30*; colloquial *fél 8* = 7:30).

Full formatting rules and worked examples: see `reference/style-lexicon.md`.

## Vowel harmony

Every suffix must harmonize with its stem: back-vowel stems take back suffixes (*ház-ban*), front-vowel stems take front (*kert-ben*), with front-rounded variants where they exist (*-hoz / -hez / -höz*, *-on / -en / -ön*). The vowels *i, í, e, é* are neutral — some stems containing only these still take **back** suffixes (*híd → hidak*, *férfi → férfiak*, *cél → célok*), so follow the attested form rather than guessing. Note also the **-val/-vel** assimilation: after a consonant the *v* assimilates and the consonant doubles (*busz → busszal*, *kés → késsel*, *vonat → vonattal*). A single disharmonic suffix marks the text as non-native.

## False friends

| English | wrong (what the cognate means) | correct |
|---|---|---|
| sympathetic | *szimpatikus* (likeable) | **együttérző** |
| actually | *aktuálisan* (currently) | **valójában / tulajdonképpen** |
| actual | *aktuális* (current, topical) | **tényleges / valódi** |
| eventually | *eventuálisan* (possibly, contingently) | **végül / végül is** |
| sensitive | *szenzitív* is OK; beware *szenzibilis* | **érzékeny** |
| sensible | *szenzibilis* | **értelmes / ésszerű** |
| realise | *realizál* (implement / book a profit) | **rájön / felismer** |
| novel (book) | *novella* (short story) | **regény** |
| concrete (material) | *konkrét* (specific) | **beton** |
| map | *mappa* (folder) | **térkép** |
| solid | *szolid* (modest, restrained) | **szilárd / masszív** |
| simple | *szimpla* (single, plain) | **egyszerű** |
| receipt | *recept* (recipe) | **nyugta / blokk** |
| sodium | *szóda* (soda water) | **nátrium** |
| **billion** | *billió* (= 10¹², trillion) | **milliárd** |

Extended list (transparent/transzparens, massive/masszív, gimnázium, konfekció, etc.): see `reference/style-lexicon.md`.

## Light-verb collocations and calqued clichés

English "make/take/do + noun" rarely maps to *csinál*. Use the Hungarian light verb:
- make a decision → **döntést hoz** / **dönt** (not *döntést csinál*)
- take a photo → **fényképet készít** / **fotót csinál** (not *fotót vesz*)
- make a mistake → **hibát követ el** · ask a question → **kérdést tesz fel** · make a promise → **ígéretet tesz**
- spend time → **időt tölt** (but spend money → **pénzt költ**) · make sense → **van értelme** (not *értelmet csinál*)

And fixed social formulas, not literal calques: *Have a nice day!* → **Szép napot (kívánok)!** · *Please find attached…* → **Mellékelten küldöm…** · *I look forward to your reply.* → **Várom a válaszát.**

## Output format

- Return **only** the Hungarian translation — no commentary, no notes, unless the user explicitly asks for explanation.
- **Single word / short phrase:** give the equivalent; if ambiguous, add a short disambiguating label in parentheses, e.g. *asztal (bútor) / tábla (iskolai).*
- **Longer text:** preserve paragraph breaks, lists, and bold/italic formatting.
- Leave brand names, code, URLs, and placeholders unchanged.
- If the user states a register (*informal / te*, *formal / ön*), follow it; otherwise infer from context and default to **ön/önök** when formal-vs-casual is genuinely ambiguous.

## Self-check (run when a sentence still feels English-shaped)

1. Would a native say this, unprompted?
2. Removed unnecessary *azt / őt / egy / van* and redundant pronouns/possessives?
3. Emphasized element immediately before the verb? Time/place adverbials moved off the end (time before place)?
4. Coverb in the right place — attached when neutral, **after the verb** under negation/focus/question/imperative — and present at all where English implies completion (*megtaláltam*, not *találtam*)?
5. Conjugation correct for every verb — definite vs. indefinite (incl. *minden/mindenki* → indefinite, *hogy*-clause → definite, 1st/2nd-person objects → indefinite, the I→you *-lak/-lek*)?
6. English prepositions rendered as the right **case suffix or postposition** (3×3 spatial series; *a buszon*, *az orvoshoz*), with demonstrative agreement (*ebben a házban*)?
7. English passives → 3rd-plural active (*kinyitották*), or *-va/-ve van* where they describe a state (*be van zárva*)?
8. "Have" as *van/nincs* + dative + possessive suffix? Numerals + **singular** noun? Attributive adjective **not** pluralized?
9. *ha*-clauses with the conditional in **both** clauses? "Want sy to…" as *hogy* + subjunctive? "Must" as *kell* + dative + inflected infinitive?
10. Register (te/ön) consistent and appropriate, with 3rd-person verbs for *ön*?
11. Hungarian punctuation applied — „quotation marks”, decimal comma, **2026. június 13.** dates, lowercase months/days/nationalities, comma before *hogy*, *billion → milliárd*?
12. Vowel harmony correct on every suffix?
