# AI Prompt Template for [Target Language] → [Native Language]

## Instructions

This is a template for creating AI prompts for new language pairs. Customize the sections below for your specific language combination.

## Customization Steps

1. Replace `[Target Language]` with your target language (e.g., "English", "Spanish", "French")
2. Replace `[Native Language]` with your native language (e.g., "Traditional Chinese", "German", "Japanese")
3. Update field names to match your `fields.json` configuration
4. Add language-specific instructions and examples
5. Modify the CSV column order to match your template

## AI Prompt Template

Copy and customize the text below:

```prompt
You are a **CSV Generator** for [Target Language] vocabulary cards with [Native Language] translations. When I provide you with multiple [Target Language] words or phrases—each on its own line—output:

1. A downloadable CSV file named `output.csv` containing one row per input, with columns in this exact order:

[Insert your CSV column order here - copy from fields.json]

2. Also display the raw CSV text in a fenced code block for quick preview.

**Field Definitions:**

- **Word**  
The [Target Language] vocabulary item (single word or multi-word phrase).

- **Pronunciation**  
[Add language-specific pronunciation guide - IPA, romanization, etc.]
[Example: "IPA phonetic transcription for English" or "Pinyin for Chinese" or "Romaji for Japanese"]

- **PartOfSpeech**  
The grammatical category appropriate for [Target Language].
[Add language-specific parts of speech if needed]

- **QuickDef**  
A brief definition in [Target Language] for quick recall.

- **FullDef**  
A complete definition in [Target Language] with context and nuance.

- **Example1**  
A simple example sentence in [Target Language].
[Add proficiency level if relevant - CEFR for European languages, JLPT for Japanese, etc.]

- **Example2**  
An additional example sentence showing different usage.

- **Synonyms**  
Comma-separated list of [Target Language] words with similar meanings.

- **Antonyms**  
Comma-separated list of [Target Language] words with opposite meanings.

- **Mnemonic**  
A memory aid that works for [Native Language] speakers learning [Target Language].

- **[NativeLanguage]Trans**  
Translation of the word into [Native Language].
[Add specific formatting requirements, e.g., "Include traditional characters for Chinese"]

- **[NativeLanguage]Def**  
Brief explanation in [Native Language] to clarify usage and context.

- **Supplement**  
Additional notes relevant to [Target Language] learners.
[Add language-specific notes - cultural context, formal/informal usage, etc.]

---

**Example Input:**
[Add 3-5 example words in your target language]

**Example Output:**
[Show expected CSV format with real examples]

After you receive my list, generate the CSV file and provide the download link plus the CSV preview.
```

## Language-Specific Customizations

### For Tonal Languages (Chinese, Vietnamese, Thai):
- Add tone information to pronunciation field
- Include tone practice in examples
- Mention tone pairs in mnemonics

### For Inflected Languages (German, Russian, Latin):
- Include grammatical case information
- Add declension/conjugation patterns
- Specify gender for nouns

### For Logographic Systems (Chinese, Japanese):
- Include character composition
- Add stroke order or radical information
- Specify reading variations

### For RTL Languages (Arabic, Hebrew):
- Specify text direction handling
- Include diacritical marks
- Add root system information

### For Agglutinative Languages (Turkish, Finnish, Hungarian):
- Include morphological breakdown
- Add suffix/prefix information
- Explain compound word formation

## Example Prompts

Look at existing templates for reference:
- `templates/english-zh-tw/prompt.md` - English to Traditional Chinese
- Add more examples as they become available

## Testing Your Prompt

1. Test with 5-10 words from your target language
2. Verify the AI generates correct CSV format
3. Check that all fields are populated appropriately
4. Import into Anki to test the complete workflow
5. Refine based on results

## Troubleshooting

**AI doesn't generate CSV file:**
- Make sure to explicitly request downloadable CSV
- Try different AI models (GPT-4, Claude, etc.)
- Simplify complex instructions

**Missing or incorrect fields:**
- Verify field names match your template exactly
- Check CSV column order matches fields.json
- Ensure examples are clear and specific

**Language-specific issues:**
- Add explicit encoding instructions (UTF-8)
- Specify character sets for special scripts
- Include formatting requirements for complex scripts