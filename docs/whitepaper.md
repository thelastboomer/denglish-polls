# Denglish Polls Whitepaper

Version: 0.3  
Status: Draft  
Project: Denglish Polls  
Repository model: entry-based public archive

## 1. Purpose

This project is a public archive and social-media experiment built around one recurring question:

**Which would you actually say?**

For each poll, the same meaning is presented in three variants:

- **denglish** — a mixed German-English form
- **en** — a natural English sentence
- **de** — a natural German sentence

The project collects phrase examples, poll results, media assets, and public discussion around real language preference.

The main distribution format is:

- an **X poll**
- a **TikTok post** introducing the phrase
- a **follow-up TikTok post** showing the result after the poll closes

The long-term archive lives publicly on GitHub.

---

## 2. Core idea

A poll only makes sense if the three options are genuinely different.

Example:

- **denglish:** Ich habe das gedownloadet.
- **en:** I downloaded it.
- **de:** Ich habe das heruntergeladen.

Poll question:

**Which would you actually say?**

Poll options:

- denglish
- en
- de

This format treats Denglish as a category distinct from both full English and full German.

---

## 3. Working definition of Denglish

For this project, **Denglish is defined narrowly**.

### Denglish
A sentence or expression that mixes German and English within the phrase itself, or uses a clearly English-influenced construction inside German.

Examples:

- Ich habe das gedownloadet.
- Wir haben morgen ein Meeting.
- Das macht für mich keinen Sinn.

### English
A natural sentence in English.

Example:

- I downloaded it.

### German
A natural sentence in standard German.

Example:

- Ich habe das heruntergeladen.

### Not included as Denglish
This project does **not** treat the following as Denglish for classification purposes:

- one full sentence in German followed by one full sentence in English
- general bilingual conversation
- alternating complete sentences between languages

That phenomenon is better described as **code-switching**.

This distinction is important because the poll format requires three parallel sentence categories:
**denglish vs en vs de**.

---

## 4. Why this project may work

This format has several strengths:

- it is easy to understand
- it invites participation
- it is repeatable
- it works well for short-form social content
- it produces public data over time
- it can grow into a searchable phrase archive

It combines entertainment, language observation, and lightweight public documentation.

---

## 5. Content workflow

Each entry can generate one or more poll cycles.

### Step 1 — Select entry
Choose a Denglish entry with a clear three-way contrast.

### Step 2 — Select sentence instance
Choose a specific example sentence for that entry.

Example entry:
- `gedownloadet`

Example sentence instance:
- Ich habe das gedownloadet.

### Step 3 — Publish poll on X
Create a poll with the question:

**Which would you actually say?**

### Step 4 — Publish TikTok introduction
Publish a TikTok that introduces the phrase. This may include:

- direct on-screen text
- narration
- text-to-speech
- duet or reaction format
- commentary on why the phrase is Denglish

### Step 5 — Wait for poll to close
A 24-hour poll is a good default.

### Step 6 — Publish TikTok result post
Create a second TikTok showing:

- the phrase again
- the poll result
- a short interpretation

### Step 7 — Archive on GitHub
Store the entry, sentence instance, media, and results in the public repository.

---

## 6. GitHub repository model

The repository should use **one folder per Denglish entry**, not one folder per full sentence.

This is the recommended long-term format because one Denglish phenomenon often appears in multiple sentence variants.

### Good example

Use:

- `0001-gedownloadet`

instead of:

- `0001-ich-habe-das-gedownloadet`

Why this is better:

- it avoids duplicate folders for near-identical sentence variants
- it groups related examples under one stable concept
- it makes the archive cleaner
- it allows multiple polls and media files for the same Denglish item

For example, these can all belong under the same entry:

- Ich habe das gedownloadet.
- Wir haben das gestern gedownloadet.
- Hast du das schon gedownloadet?

All of them represent the same core Denglish item:
**gedownloadet**

---

## 7. Entry-based structure

The repository should therefore distinguish between two levels:

### 1. Entry
The core Denglish unit or phenomenon.

Examples:

- `gedownloadet`
- `meeting`
- `sinn-machen`
- `updaten`

### 2. Sentence instance
A specific sentence used in a poll or example.

Examples:

- Ich habe das gedownloadet.
- Wir haben morgen ein Meeting.
- Das macht für mich keinen Sinn.

This distinction is important. The folder should represent the **entry**, while the files inside it can store one or more sentence instances.

---

## 8. Recommended structure

```text
README.md
LICENSE
docs/
  whitepaper.md
entries/
  index.md
  0001-gedownloadet/
    README.md
    meta.yaml
    examples.yaml
    polls/
      2026-04-22-01/
        poll.md
        result.yaml
        images/
          poll-result.png
          x-poll-screenshot.png
        audio/
          denglish.mp3
          en.mp3
          de.mp3
  0002-sinn-machen/
    README.md
    meta.yaml
    examples.yaml
```

This model is more scalable than one folder per sentence.

---

## 9. Why one folder per entry is the right model

A separate folder for each entry makes the project scalable.

### Benefits

- one concept can contain many sentence variants
- duplicate sentence folders are avoided
- media assets stay organized
- future automation becomes easier
- contributors can add examples cleanly
- GitHub browsing stays readable
- the project can later grow into a website or dataset

This structure supports both a simple start and later expansion.

---

## 10. Entry folder specification

Each entry folder should have at least a human-readable file and may later include machine-readable metadata, examples, and poll artifacts.

### Minimum version

```text
entries/
  0001-gedownloadet/
    README.md
```

### Recommended version

```text
entries/
  0001-gedownloadet/
    README.md
    meta.yaml
    examples.yaml
    polls/
      2026-04-22-01/
        poll.md
        result.yaml
        audio/
          denglish.mp3
          en.mp3
          de.mp3
        images/
          poll-result.png
          x-poll-screenshot.png
```

---

## 11. Entry README template

Each entry should have a `README.md` that can be read directly on GitHub.

Suggested structure:

```md
# 0001 — gedownloadet

## Entry

Core Denglish item: **gedownloadet**

## Description

English verb root adapted into German usage.

## Example sentences

- Ich habe das gedownloadet.
- Wir haben das gestern gedownloadet.
- Hast du das schon gedownloadet?

## Related German alternatives

- heruntergeladen
- runtergeladen
```

---

## 12. Metadata template

Each entry may also have a `meta.yaml` file for structured processing.

Example:

```yaml
id: 1
slug: gedownloadet
title: gedownloadet
category: verb
type: borrowed-verb
status: published
tags:
  - technology
  - anglicism
created: 2026-04-22
```

This makes it easier to build:

- indexes
- statistics
- exports
- search tools
- websites

---

## 13. Examples template

Each entry may have an `examples.yaml` file containing sentence variants.

Example:

```yaml
entry: gedownloadet
examples:
  - id: ex1
    denglish: Ich habe das gedownloadet.
    en: I downloaded it.
    de: Ich habe das heruntergeladen.
    notes: Basic past-tense example.
  - id: ex2
    denglish: Wir haben das gestern gedownloadet.
    en: We downloaded it yesterday.
    de: Wir haben das gestern heruntergeladen.
    notes: Same entry in a plural sentence.
```

This allows one entry to support multiple poll-ready examples.

---

## 14. Poll record template

Each specific poll can be stored in its own subfolder.

Example:

```text
entries/
  0001-gedownloadet/
    polls/
      2026-04-22-01/
        poll.md
        result.yaml
```

Suggested `poll.md` structure:

```md
# Poll 2026-04-22-01

## Phrase variants

- **denglish:** Ich habe das gedownloadet.
- **en:** I downloaded it.
- **de:** Ich habe das heruntergeladen.

## Poll question

Which would you actually say?

## Poll options

- denglish
- en
- de

## Links

- X poll:
- TikTok intro:
- TikTok result:
```

Suggested `result.yaml` structure:

```yaml
poll_id: 2026-04-22-01
entry: gedownloadet
example_id: ex1
status: closed
winner: ""
votes:
  denglish: 0
  en: 0
  de: 0
x_poll_url: ""
tiktok_intro_url: ""
tiktok_result_url: ""
closed_at: ""
```

---

## 15. Naming convention

Each entry folder should use:

**numeric ID + short stable slug**

Examples:

- `0001-gedownloadet`
- `0002-sinn-machen`
- `0003-meeting`

The folder name should represent the **smallest stable Denglish unit** that identifies the phenomenon, not necessarily the full sentence.

This gives the project:

- stable ordering
- readable names
- simple referencing
- room for growth

### Rule of thumb

Use the shortest stable slug that names the Denglish phenomenon.

Good:

- `0001-gedownloadet`
- `0002-meeting`
- `0003-sinn-machen`

Less suitable:

- `0001-ich-habe-das-gedownloadet`
- `0002-wir-haben-das-gedownloadet`

---

## 16. Central index

Even with separate entry folders, the repository should also maintain a central index.

Example:

```text
entries/index.md
```

This file can list all entries in a simple table.

Example:

```md
# Entry Index

| ID | Slug | Type | Status |
|----|------|------|--------|
| 0001 | gedownloadet | verb | published |
| 0002 | sinn-machen | expression | draft |
```

This helps users browse the archive quickly.

---

## 17. License approach

Because this repository is primarily a public content and documentation project, a **Creative Commons Attribution 4.0 International (CC BY 4.0)** license is a strong fit.

This allows public reuse while keeping attribution.

Suggested repository note:

> Unless otherwise noted, the content in this repository is licensed under CC BY 4.0.

---

## 18. Editorial principles

To keep the project useful and consistent, each poll should aim for the following:

- the three versions should express the same meaning as closely as possible
- the German version should be natural German, not artificial anti-English German
- the English version should be natural English
- the Denglish version should reflect real usage, not a parody unless explicitly marked as parody
- the sentence should be short enough for polling and social-media presentation
- the distinction between categories should remain clear
- multiple sentence examples may belong to the same entry

---

## 19. Scope for future expansion

The project can later expand in several directions:

- pronunciation audio for each variant
- charts of poll results
- tags by topic, grammar, or setting
- office/business Denglish
- tech/internet Denglish
- regional differences
- time trends across entries
- a public website generated from the repository
- multilingual commentary or subtitles

The entry-based folder model supports all of these.

---

## 20. Suggested first repository setup

A practical initial setup is:

```text
README.md
LICENSE
docs/
  whitepaper.md
entries/
  index.md
  0001-gedownloadet/
    README.md
    meta.yaml
    examples.yaml
```

This is enough to launch the project while leaving room for audio and image assets later.

---

## 21. Conclusion

The project works best when **Denglish is treated as a real third category**, distinct from full English and full German.

The GitHub structure should be **entry-based rather than sentence-based**. One folder should represent one stable Denglish phenomenon, while multiple sentence examples and poll records can live inside that folder.

The guiding public question remains simple and strong:

**Which would you actually say?**
