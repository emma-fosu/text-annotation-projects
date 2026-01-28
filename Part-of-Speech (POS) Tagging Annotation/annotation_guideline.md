# Annotation Guidelines

## Part-of-Speech (POS) Tagging Project

---

## 1. Purpose of This Document

This document provides **mandatory annotation instructions** for the Part-of-Speech (POS) tagging project documented in this repository. It is written for annotators, reviewers, and QA personnel and reflects the level of guidance typically provided in enterprise annotation projects.

All annotators are expected to **read, understand, and strictly follow** these guidelines before beginning annotation.

---

## 2. Task Definition

### What You Are Doing

You are labeling each **token** in a sentence with **exactly one POS tag** that represents the token’s **syntactic function in context**.

### What You Are NOT Doing

* You are not labeling meaning or sentiment
* You are not guessing intent beyond the sentence
* You are not introducing new labels

---

## 3. Annotation Unit

* **Primary unit:** Token (word or punctuation)
* **Context unit:** Sentence

Every token must receive a label, including punctuation.

---

## 4. POS Tagset (Penn Treebank)

This project uses the **Penn Treebank POS Tagset**.

### Core Tags and Usage

| Tag  | When to Use                             | Example     |
| ---- | --------------------------------------- | ----------- |
| NN   | Common noun (singular/mass)             | book, water |
| NNS  | Common noun (plural)                    | books       |
| NNP  | Proper noun (singular)                  | Ghana       |
| NNPS | Proper noun (plural)                    | Americans   |
| VB   | Verb, base form                         | run         |
| VBD  | Verb, past tense                        | ran         |
| VBG  | Verb, gerund/present participle         | running     |
| VBN  | Verb, past participle                   | eaten       |
| VBP  | Verb, non-3rd person present            | run         |
| VBZ  | Verb, 3rd person present                | runs        |
| JJ   | Adjective                               | quick       |
| RB   | Adverb                                  | quickly     |
| DT   | Determiner                              | the, a      |
| IN   | Preposition / subordinating conjunction | in, of      |
| PRP  | Personal pronoun                        | she, they   |
| PRP$ | Possessive pronoun                      | her, their  |
| CC   | Coordinating conjunction                | and, but    |
| CD   | Cardinal number                         | three, 7    |
| TO   | The word “to”                           | to          |
| MD   | Modal verb                              | can, should |
| UH   | Interjection                            | wow, oh     |
| FW   | Foreign word                            | adiós       |
| .    | Sentence-ending punctuation             | . ? !       |

---

## 5. Tokenization Rules

### General Rules

1. Punctuation is always a separate token
2. Do not merge punctuation with words
3. Preserve original casing

### Contractions

| Text  | Tokens   |
| ----- | -------- |
| don’t | do / n't |
| I’m   | I / 'm   |

* "n't" is tagged as **RB**
* Contracted verbs take their correct verb form

### Hyphenated Words

* Keep as one token if meaning is preserved (e.g., *well-known*)
* Split only if hyphen separates independent words

---

## 6. Annotation Rules (Critical)

### Rule 1: Context Is Mandatory

Always determine the POS tag **based on sentence context**, not dictionary definitions.

### Rule 2: One Token, One Tag

Each token must have exactly one POS tag. Never assign multiple tags.

### Rule 3: No Guessing

If a sentence is unclear or corrupted, **flag it** instead of guessing.

---

## 7. Common Ambiguities and How to Resolve Them

### Noun vs Verb

* *I run every day* → run = VBP
* *a long run* → run = NN

### Adjective vs Past Participle

* *a broken window* → broken = JJ
* *has broken* → broken = VBN

### Adverb vs Adjective

* *runs fast* → fast = RB
* *a fast car* → fast = JJ

---

## 8. Special Cases

### Numbers

* All numbers (written or numeric) → CD

### URLs / Emails

* Treat entire string as a single token → NN

### Emojis and Symbols

* Emojis expressing emotion → UH
* Currency symbols → NN

### Foreign Words

* If not English → FW

---

## 9. Flagging and Comments

Annotators must flag:

* Incomplete sentences
* Garbled or corrupted text
* Extremely ambiguous tokens

Use the comment field to explain why the item was flagged.

---

## 10. Quality Expectations

### Accuracy

* Minimum acceptable accuracy: **97%**

### Consistency

* Follow this document over intuition
* Prioritize consistency across the dataset

### Review

* Samples may be re-reviewed by QA
* Disagreements resolved using this guideline

---

## 11. Example (Fully Annotated)

**Sentence:**

> The quick brown fox jumps over the lazy dog.

| Token | POS |
| ----- | --- |
| The   | DT  |
| quick | JJ  |
| brown | JJ  |
| fox   | NN  |
| jumps | VBZ |
| over  | IN  |
| the   | DT  |
| lazy  | JJ  |
| dog   | NN  |
| .     | .   |

---

## 12. Final Notes to Annotators

* Read the full sentence before labeling
* Review your work before submission
* Ask questions early rather than correcting later

Failure to follow these guidelines may result in rework or rejection.

---

*End of Annotation Guidelines*
