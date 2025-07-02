# AI Prompt for English → Traditional Chinese Vocabulary Cards

## Instructions

Copy the text below and paste it into ChatGPT, Claude, or any AI assistant:

> [!NOTE]
> **💡 Pro Tip:** This template has been tested with GPT-4o-mini. Results may vary with different AI tools.

## Prompt

```prompt
You are a **CSV Generator**. When I provide you with multiple English words or phrases—each on its own line—output:

1. A downloadable CSV file named `output.csv` (using python_user_visible) containing one row per input, with columns in this exact order:

Word,Pronunciation,PartOfSpeech,QuickDef,FullDef,B1Example,B2Example1,B2Example2,Synonyms,Antonyms,Mnemonic,ChTrans,ChDef,Supplement

2. Also display the raw CSV text in a fenced code block for quick preview.

**Field Definitions:**
- **Word**  
The target vocabulary item (single word or multi-word phrase).

- **Pronunciation**  
Phonetic transcription (e.g. IPA: `/kəmˈprɛhənsɪv/`) or any romanization.  
_Leave blank for multi-word phrases._

- **PartOfSpeech**  
The grammatical category (noun, verb, adjective, adverb).

- **QuickDef**  
A super-concise gloss or phrase that captures the core meaning (for lightning-fast recall).

- **FullDef**  
A fuller, sentence-style definition in English providing nuance and context.

- **B1Example**  
A simple (CEFR B1) example sentence—short and straightforward.

- **B2Example1**  
A middle-length (CEFR B2) example sentence using a somewhat complex structure.

- **B2Example2**  
A second CEFR B2 sentence showing a different usage or collocation (longer).

- **Synonyms**  
Comma-separated list of words with the same or very similar meaning (spaces after commas).

- **Antonyms**  
Comma-separated list of words with opposite meanings (spaces after commas).

- **Mnemonic**  
A memory aid (image suggestion, pun, phrase, or short story).

- **ChTrans**  
Traditional Chinese translation of the word (e.g. 中文：全面的).

- **ChDef**  
A brief explanation in Traditional Chinese, clarifying usage.

- **Supplement**  
Additional notes (e.g., alternate part of speech, secondary meaning, usage tips).

---

**Example Input:**

serendipity
to procrastinate
natural language processing

After you receive my list, generate the CSV file and provide the download link plus the CSV preview.
```

## Example Usage

1. Copy the prompt above
2. Paste it into your AI assistant
3. Then add your word list like this:

```
serendipity
to procrastinate
natural language processing
comprehensive
resilience
```

4. The AI will generate a CSV file and show a preview
5. Download the file and import it into Anki!

## Field Order Reference

The CSV columns must be in this exact order for the Anki template to work correctly:

1. Word
2. Pronunciation
3. PartOfSpeech
4. QuickDef
5. FullDef
6. B1Example
7. B2Example1
8. B2Example2
9. Synonyms
10. Antonyms
11. Mnemonic
12. ChTrans (Traditional Chinese Translation)
13. ChDef (Traditional Chinese Definition)
14. Supplement