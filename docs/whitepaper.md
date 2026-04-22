# Denglish Preference Project
## Whitepaper v0.1

**Working title:** German, English, or Denglish — what would you actually say?

**Status:** Initial concept draft for the first public GitHub commit  
**Author:** Matthias Ludwig  
**License suggestion:** MIT for code / CC BY 4.0 for content

---

## 1. Executive Summary

The **Denglish Preference Project** is a public language experiment built around a simple recurring question:

> **Which would you actually say?**

For each phrase or sentence, users are presented with three alternatives:

- **Denglish** — a hybrid form mixing German and English in one expression or sentence
- **EN** — a natural full English version
- **DE** — a natural full German version

The goal is not to declare one form objectively correct, but to document **real preference, real usage, and real language drift** in public digital culture.

The project combines:

- short-form social content on **TikTok**
- public voting on **X polls**
- a transparent, growing **GitHub archive** of phrases and results

Over time, the project can become a structured public dataset showing where modern German speakers prefer:

- pure German,
- pure English,
- or hybrid Denglish.

---

## 2. Core Idea

Modern German speech, especially online, in offices, in tech, in media, and among younger speakers, often contains English elements. Some of these expressions are obvious borrowings, some are literal translations from English, and some are full mixed sentences.

Examples:

- *Ich habe das gedownloadet.*
- *Das macht für mich keinen Sinn.*
- *Wir sollten das nochmal challengen.*
- *Das ist weird.*

At the same time, full English alternatives and full German alternatives usually also exist:

- *I downloaded it.*
- *Ich habe das heruntergeladen.*

This creates an interesting three-way comparison:

1. **Hybrid expression**
2. **Natural English expression**
3. **Natural German expression**

The project turns that comparison into a repeatable public format.

---

## 3. Definition of Denglish

For this project, **Denglish is defined narrowly**.

### 3.1 Operational Definition

A phrase counts as **Denglish** if it is **not fully German and not fully English**, but instead contains one or more of the following:

- English vocabulary embedded in German sentence structure
- Germanized English verbs or nouns
- English-influenced literal translations that feel imported from English usage
- mixed syntax or wording that reflects hybrid speech habits

### 3.2 Examples That Qualify as Denglish

- *Ich habe das gedownloadet.*
- *Das macht Sinn.*
- *Wir müssen das nochmal challengen.*
- *Ich bin heute im Homeoffice.*
- *Das ist awkward.*

### 3.3 What Does **Not** Count as Denglish in This Project

The following do **not** count as Denglish for classification purposes:

- one full sentence in German followed by one full sentence in English
- a complete switch from one language to the other without internal mixing
- direct translation exercises without real-world usage value

That broader phenomenon is better described as **code-switching**, not Denglish.

### 3.4 Why This Narrow Definition Matters

The project only works as a meaningful three-option poll if:

- **Denglish** is a distinct third category,
- separate from **EN**,
- and separate from **DE**.

If full English or full German sentences were also labeled “Denglish,” the comparison would collapse.

---

## 4. Poll Format

Each phrase entry is built around one public question:

> **Which would you actually say?**

### 4.1 Standard Poll Template

```text
Denglish
Ich habe das gedownloadet.

EN
I downloaded it.

DE
Ich habe das heruntergeladen.

Which would you actually say?
- Denglish
- EN
- DE
```

### 4.2 Why This Prompt Works

The wording avoids abstract debates about correctness and instead asks for:

- actual usage,
- natural preference,
- spoken instinct,
- identity and style.

This makes the result more interesting than a school-style “Which is correct?” poll.

---

## 5. Platform Strategy

### 5.1 X

X is used for:

- public polls
- final vote counts
- audience interaction
- quote replies and discussion

### 5.2 TikTok

TikTok is used for:

- source examples
- reaction videos
- duets where allowed
- short commentary before the vote
- follow-up videos showing the result after the poll closes

### 5.3 GitHub

GitHub is used for:

- public phrase archive
- transparent methodology
- result history
- version control
- possible future dataset exports and analysis

GitHub is the permanent memory layer of the project.

---

## 6. Content Workflow

### 6.1 Step 1 — Detect a Candidate Phrase

Find a phrase that clearly fits one of these patterns:

- mixed German-English sentence
- German phrase strongly influenced by English
- widely used hybrid expression in digital culture
- controversial or funny “Denglish” construction

### 6.2 Step 2 — Normalize the Three Variants

Create three versions:

- **Denglish** version
- **EN** version
- **DE** version

Important rule: all three should express **the same intended meaning** as closely as possible.

### 6.3 Step 3 — Publish Social Post

Create:

- one X poll
- optionally one TikTok introducing the phrase

### 6.4 Step 4 — Wait for Poll Close

Recommended initial duration:

- **24 hours**

### 6.5 Step 5 — Publish Result Video

Create a short TikTok or X follow-up showing:

- the phrase
- the three options
- the winner
- optional commentary

### 6.6 Step 6 — Archive on GitHub

Add the entry to the public archive with:

- phrase ID
- date
- wording
- classification notes
- poll result
- platform links if still available

---

## 7. Data Model

Each phrase should have a stable public record.

### 7.1 Suggested Fields

```yaml
id: 0001
slug: ich-habe-das-gedownloadet
status: published
category: lexical-mix
question: Which would you actually say?
denglish: Ich habe das gedownloadet.
en: I downloaded it.
de: Ich habe das heruntergeladen.
notes: Hybrid German sentence with English loan verb adapted into German morphology.
source_context: common online/offline usage
poll_platform: x
poll_opened: 2026-04-22
poll_duration_hours: 24
result_denglish_percent: null
result_en_percent: null
result_de_percent: null
winner: null
```

### 7.2 Possible Classification Types

Each phrase can optionally be tagged with one or more categories:

- `lexical-mix`
- `literal-translation`
- `office-language`
- `tech-language`
- `internet-slang`
- `pseudo-anglicism`
- `morphological-germanization`
- `syntax-influence`
- `youth-speech`
- `media-language`

---

## 8. GitHub Repository Structure

Suggested initial repository structure:

```text
/
├─ README.md
├─ LICENSE
├─ whitepaper.md
├─ data/
│  ├─ phrases/
│  │  ├─ 0001-ich-habe-das-gedownloadet.md
│  │  ├─ 0002-das-macht-sinn.md
│  │  └─ ...
│  └─ phrases.yaml
├─ docs/
│  ├─ methodology.md
│  ├─ classification.md
│  └─ faq.md
└─ media/
   └─ thumbnails/
```

### 8.1 Minimal First Commit

For the first commit, the following is enough:

- `README.md`
- `whitepaper.md`
- `data/phrases/0001-ich-habe-das-gedownloadet.md`

---

## 9. Example Entry

```md
# 0001 — Ich habe das gedownloadet.

**Status:** planned  
**Category:** lexical-mix, morphological-germanization  
**Question:** Which would you actually say?

## Variants

- **Denglish:** Ich habe das gedownloadet.
- **EN:** I downloaded it.
- **DE:** Ich habe das heruntergeladen.

## Notes

This is a classic Denglish pattern: an English verb root is inserted into a German sentence and adapted to German grammar.

## Result

- Denglish: pending
- EN: pending
- DE: pending

## Commentary

A good starter phrase because the three options are cleanly separated and easy to understand.
```

---

## 10. Methodological Principles

### 10.1 Descriptive, Not Prescriptive

The project documents what people actually prefer to say.
It does not act as a language academy.

### 10.2 Transparent Classification

Every phrase should be explainable:

- Why is it Denglish?
- Why is the DE version considered natural German?
- Why is the EN version considered natural English?

### 10.3 Same Meaning Across Versions

The three alternatives must be semantically as close as possible.

### 10.4 Public Traceability

Whenever possible, archive:

- poll date
- platform used
- result snapshot
- notes on source context

### 10.5 Real-World Relevance

Only include phrases that people plausibly say, write, or encounter in real life.

---

## 11. Why This Could Become Interesting

Over time, the archive may reveal patterns such as:

- which domains generate the most Denglish
- whether tech phrases favor Denglish more strongly than daily-life phrases
- whether some literal translations are accepted more than others
- whether users prefer pure German in writing but Denglish in speech
- how online language habits drift over time

The project can evolve from entertainment into a small public linguistic dataset.

---

## 12. Risks and Weaknesses

### 12.1 Informal Audience Bias

Polls on X and TikTok do not produce representative scientific samples.

### 12.2 Ambiguity of “Natural” German

Some phrases have several acceptable German equivalents.

### 12.3 Audience Irony

Users may vote for the funniest option rather than the one they truly use.

### 12.4 Platform Dependency

Visibility, engagement, and poll participation depend on platform algorithms.

### 12.5 Borderline Cases

Some phrases may sit between borrowing, Anglicism, Denglish, and ordinary modern German.

These limitations do not invalidate the project, but they should remain visible.

---

## 13. Future Expansion

Potential later additions:

- searchable website or GitHub Pages frontend
- CSV/JSON export of all phrases
- tag-based browsing
- “most voted Denglish phrases” page
- time-series tracking
- German vs English speaking audience splits
- comments archive
- YouTube Shorts adaptation
- public contribution guidelines
- crowdsourced phrase submission form

---

## 14. Suggested Positioning

### 14.1 One-Line Version

**A public experiment tracking whether people would actually say it in Denglish, English, or German.**

### 14.2 Slightly Longer Version

**The Denglish Preference Project is a public archive of hybrid German-English phrases, paired with natural English and natural German alternatives, and voted on by real users.**

### 14.3 Creator Voice

Tone should be:

- curious
- sharp
- slightly humorous
- not academic in style
- but methodical in structure

---

## 15. Recommended First Phrase Set

A possible first batch:

1. *Ich habe das gedownloadet.*
2. *Das macht Sinn.*
3. *Ich bin im Homeoffice.*
4. *Wir müssen das nochmal challengen.*
5. *Das ist awkward.*
6. *Kannst du mir ein Update geben?*
7. *Wir haben ein Meeting.*
8. *Das ist weird.*
9. *Ich habe heute einen Call.*
10. *Lass uns das final besprechen.*

These should later be reviewed one by one to ensure the DE and EN alternatives are both natural and fair.

---

## 16. Conclusion

This project is simple, repeatable, public, and expandable.

Its strength lies in the clean recurring question:

> **Which would you actually say?**

By defining Denglish narrowly and archiving every phrase transparently, the project can grow from a social-media format into a living public record of bilingual language preference.

---

## 17. First Commit Note

Suggested first commit message:

```text
Initial whitepaper for the Denglish Preference Project
```

Suggested repository description:

```text
Public archive of Denglish vs English vs German phrase preferences.
```

