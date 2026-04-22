# Denglish Polls Whitepaper

Version: 0.2  
Status: Draft  
Project: Denglish Polls  
Repository model: phrase-based public archive

## 1. Purpose

This project is a public archive and social-media experiment built around one recurring question:

**Which would you actually say?**

For each entry, the same meaning is presented in three variants:

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

Each phrase can generate a small content cycle.

### Step 1 — Select phrase
Choose a phrase with a clear three-way contrast:

- denglish
- en
- de

### Step 2 — Publish poll on X
Create a poll with the question:

**Which would you actually say?**

### Step 3 — Publish TikTok introduction
Publish a TikTok that introduces the phrase. This may include:

- direct on-screen text
- narration
- text-to-speech
- duet or reaction format
- commentary on why the phrase is Denglish

### Step 4 — Wait for poll to close
A 24-hour poll is a good default.

### Step 5 — Publish TikTok result post
Create a second TikTok showing:

- the phrase again
- the poll result
- a short interpretation

### Step 6 — Archive on GitHub
Store the phrase, media, and results in the public repository.

---

## 6. GitHub repository model

The repository should use **one folder per phrase**.

This is the recommended long-term format because each phrase may later contain:

- text
- metadata
- audio files
- screenshots
- poll graphics
- links to public posts

### Recommended structure

```text
README.md
LICENSE
docs/
  whitepaper.md
phrases/
  index.md
  0001-ich-habe-das-gedownloadet/
    README.md
    meta.yaml
    audio/
      denglish.mp3
      en.mp3
      de.mp3
    images/
      poll-result.png
      x-poll-screenshot.png
  0002-das-macht-keinen-sinn/
    README.md
    meta.yaml
```

---

## 7. Why one folder per phrase is the right model

A separate folder for each phrase makes the project scalable.

### Benefits

- each phrase becomes a self-contained public record
- media assets stay organized
- future automation becomes easier
- contributors can add phrases cleanly
- GitHub browsing stays readable
- the project can later grow into a website or dataset

This structure supports both a simple start and later expansion.

---

## 8. Phrase folder specification

Each phrase folder should have at least a human-readable file and may later include machine-readable metadata and media.

### Minimum version

```text
phrases/
  0001-ich-habe-das-gedownloadet/
    README.md
```

### Recommended version

```text
phrases/
  0001-ich-habe-das-gedownloadet/
    README.md
    meta.yaml
    audio/
      denglish.mp3
      en.mp3
      de.mp3
    images/
      poll-result.png
      x-poll-screenshot.png
```

---

## 9. Phrase README template

Each phrase should have a `README.md` that can be read directly on GitHub.

Suggested structure:

```md
# 0001 — Ich habe das gedownloadet.

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

## Notes

A typical example of Denglish using an English root adapted into German usage.

## Links

- X poll:
- TikTok intro:
- TikTok result:
```

---

## 10. Metadata template

Each phrase may also have a `meta.yaml` file for structured processing.

Example:

```yaml
id: 1
slug: ich-habe-das-gedownloadet
title: Ich habe das gedownloadet.
denglish: Ich habe das gedownloadet.
en: I downloaded it.
de: Ich habe das heruntergeladen.
question: Which would you actually say?
options:
  - denglish
  - en
  - de
status: published
tags:
  - verb
  - technology
  - anglicism
created: 2026-04-22
x_poll_url: ""
tiktok_intro_url: ""
tiktok_result_url: ""
```

This makes it easier to build:

- indexes
- statistics
- exports
- search tools
- websites

---

## 11. Naming convention

Each phrase folder should use:

**numeric ID + slug**

Examples:

- `0001-ich-habe-das-gedownloadet`
- `0002-das-macht-keinen-sinn`
- `0003-wir-haben-morgen-ein-meeting`

This gives the project:

- stable ordering
- readable names
- simple referencing
- room for growth

---

## 12. Central index

Even with separate phrase folders, the repository should also maintain a central index.

Example:

```text
phrases/index.md
```

This file can list all phrases in a simple table.

Example:

```md
# Phrase Index

| ID | Slug | Denglish phrase | Status |
|----|------|------------------|--------|
| 0001 | ich-habe-das-gedownloadet | Ich habe das gedownloadet. | published |
| 0002 | das-macht-keinen-sinn | Das macht keinen Sinn. | draft |
```

This helps users browse the archive quickly.

---

## 13. License approach

Because this repository is primarily a public content and documentation project, a **Creative Commons Attribution 4.0 International (CC BY 4.0)** license is a strong fit.

This allows public reuse while keeping attribution.

Suggested repository note:

> Unless otherwise noted, the content in this repository is licensed under CC BY 4.0.

---

## 14. Editorial principles

To keep the project useful and consistent, each phrase should aim for the following:

- the three versions should express the same meaning as closely as possible
- the German version should be natural German, not artificial anti-English German
- the English version should be natural English
- the Denglish version should reflect real usage, not a parody unless explicitly marked as parody
- the phrase should be short enough for polling and social-media presentation
- the distinction between categories should remain clear

---

## 15. Scope for future expansion

The project can later expand in several directions:

- pronunciation audio for each variant
- charts of poll results
- tags by topic, grammar, or setting
- office/business Denglish
- tech/internet Denglish
- regional differences
- time trends across phrases
- a public website generated from the repository
- multilingual commentary or subtitles

The phrase-folder model supports all of these.

---

## 16. Suggested first repository setup

A practical initial setup is:

```text
README.md
LICENSE
docs/
  whitepaper.md
phrases/
  index.md
  0001-ich-habe-das-gedownloadet/
    README.md
    meta.yaml
```

This is enough to launch the project while leaving room for audio and image assets later.

---

## 17. Conclusion

The project works best when **Denglish is treated as a real third category**, distinct from full English and full German.

The phrase-based folder structure is the right GitHub model because it allows each example to grow into a complete public record with text, metadata, media, and poll results.

The guiding public question remains simple and strong:

**Which would you actually say?**
