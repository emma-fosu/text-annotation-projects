# Part-of-Speech (POS) Tagging Annotation Project
<img src="./assets/POS Tagging.gif" />

## Project Summary

The project demonstrates my ability to design annotation schemas, guide annotators, enforce quality controls, and deliver production-ready linguistic datasets for NLP model development.

The dataset produced from this project is suitable for training and evaluating models for syntactic parsing, named entity recognition, and other downstream NLP tasks.

---

## Objectives

* Produce a high-quality POS-tagged English corpus
* Apply a standardized and industry-recognized POS schema
* Achieve high inter-annotator agreement and annotation accuracy
* Demonstrate end-to-end annotation project ownership

---

## Dataset Description

* **Language:** English
* **Domains:** Conversational text, formal written text, semi-structured content
* **Unit of Annotation:** Token-level
* **Average Sentence Length:** 10–25 tokens
* **Data Sensitivity:** Fully anonymized; no PII

Each data sample consists of a single sentence or short paragraph.

---

## Annotation Schema

The project uses the **Penn Treebank POS Tagset**, a widely adopted standard in both academic research and industrial NLP pipelines.

Each token is assigned **exactly one POS tag** based on its syntactic role within context.

Examples of core tags include:

* NN / NNS – Common nouns
* NNP / NNPS – Proper nouns
* VB, VBD, VBG, VBN, VBP, VBZ – Verb forms
* JJ – Adjectives
* RB – Adverbs
* DT – Determiners
* IN – Prepositions
* PRP / PRP$ – Pronouns
* CD – Numbers
* . – Sentence-final punctuation

The full schema and annotation rules are documented in the [annotation guidelines](./annotation_guideline.md).

## Tokenization Rules

* Punctuation is tokenized separately
* Contractions are split (e.g., *don't* → *do* + *n't*)
* Hyphenated words are kept as a single token when meaning is preserved
* URLs and email addresses are treated as single tokens

Tokenization was verified prior to POS labeling to ensure consistency across the dataset.

---

## Annotation Process

1. Read the full sentence to establish context
2. Verify or correct tokenization
3. Assign POS tags sequentially at the token level
4. Review the sentence holistically for consistency
5. Submit annotation for quality review

Ambiguous or corrupted samples were flagged for review rather than guessed.

---

## Tools Used

* **Annotation Platform:** Label Studio (configured for token-level POS tagging)
* **Formats:**

  * JSON (Label Studio export)
---

## Repository Structure

```bash
pos-tagging-project/
│── README.md # Annotation documentation
│── annotation_guidelines.md # Annotation guidelines
│── dialydialog.train.csv # Raw, unannotated dataset
│── annotated_dataset.json # Annotated dataset
│── labelstudio_task.json # Input dataset for Label Studio
```

## Example Annotation

**Sentence:**

> She is running fast.

| Token   | POS |
| ------- | --- |
| She     | PRP |
| is      | VBZ |
| running | VBG |
| fast    | RB  |
| .       | .   |

---

## Results

* High annotation consistency across domains
* Minimal schema violations
* Strong agreement scores indicating reliable labels

The resulting dataset is suitable for direct use in NLP model training pipelines.

---

## Skills Demonstrated

* Linguistic annotation using industry-standard POS schemas
* Annotation guideline development and documentation
* Quality assurance and agreement analysis
* Practical NLP data preparation
* Enterprise-style annotation workflow execution

---

## Use Cases

This dataset can be used for:

* Training POS taggers
* Evaluating syntactic parsers
* Preprocessing pipelines for NER and IE tasks
* Educational demonstrations of linguistic annotation

---

## License

This project uses synthetic or publicly permissible text for demonstration purposes. No proprietary or sensitive data is included.

---