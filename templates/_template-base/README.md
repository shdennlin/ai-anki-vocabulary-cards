# Template Base for New Language Pairs

This directory contains the base structure for creating new language pair templates.

## Creating a New Language Template

### 1. Copy This Directory

```bash
cp -r templates/_template-base templates/[target-language]-[native-language]
```

**Naming Convention:**
- Use ISO language codes where possible
- Format: `target-native` (e.g., `english-zh-tw`, `spanish-en`, `french-de`)
- Use lowercase with hyphens

### 2. Required Files

Each language template must include:

- **`README.md`** - Setup instructions in both languages
- **`front.html`** - Anki front template
- **`back.html`** - Anki back template  
- **`style.css`** - Card styling
- **`prompt.md`** - AI generation prompt
- **`fields.json`** - Field configuration
- **`preview/`** - Screenshot directory
  - `front.png` - Front card screenshot
  - `back.png` - Back card screenshot

### 3. Customization Steps

1. **Update `fields.json`**
   - Change `targetLanguage` and `nativeLanguage`
   - Modify field descriptions for your language pair
   - Add language-specific examples

2. **Modify HTML Templates**
   - Update field references to match your language
   - Adjust layout for different writing systems (RTL, vertical text, etc.)
   - Add language-specific elements (e.g., furigana for Japanese)

3. **Customize Styling**
   - Adjust fonts for your language's script
   - Modify layout for text direction
   - Update colors if needed

4. **Create AI Prompt**
   - Adapt the prompt for your target/native language pair
   - Include language-specific instructions
   - Specify output format requirements

5. **Write Documentation**
   - Translate setup instructions
   - Add language-specific tips
   - Include examples in both languages

### 4. Field Naming Conventions

Use descriptive field names that indicate the language:

**English Templates:**
- `Word`, `Pronunciation`, `Definition`

**With Native Language:**
- `[LangCode]Trans` (e.g., `ZhTrans`, `EsTrans`)
- `[LangCode]Def` (e.g., `ZhDef`, `EsDef`)

**Examples by Language:**
- **Chinese:** `ChTrans`, `ChDef`
- **Japanese:** `JaTrans`, `JaDef`, `JaReading`
- **Korean:** `KoTrans`, `KoDef`
- **Spanish:** `EsTrans`, `EsDef`
- **German:** `DeTrans`, `DeDef`

### 5. Testing Your Template

Before submitting:

1. Create a test CSV with 5-10 words
2. Import into Anki using your template
3. Verify all fields display correctly
4. Test on mobile and desktop
5. Check text rendering and fonts
6. Validate HTML and CSS

### 6. Language-Specific Considerations

**Chinese (Simplified/Traditional):**
- Include pinyin pronunciation
- Handle simplified/traditional character differences
- Consider stroke order information

**Japanese:**
- Add furigana support
- Include kanji, hiragana, katakana fields
- Consider JLPT levels

**Korean:**
- Include hangul pronunciation
- Add hanja information if relevant
- Consider TOPIK levels

**Arabic/Hebrew (RTL languages):**
- Adjust CSS for right-to-left text
- Handle mixed LTR/RTL content
- Consider diacritics and vowel marks

**European Languages:**
- Include grammatical information (gender, cases)
- Add conjugation/declension notes
- Consider CEFR levels

### 7. Submission Checklist

- [ ] All required files present
- [ ] Documentation in both languages
- [ ] Working Anki import tested
- [ ] Screenshots included
- [ ] Field configuration complete
- [ ] AI prompt functional
- [ ] Code follows project standards

## Example Templates

Look at existing templates for reference:

- **`english-zh-tw/`** - English to Traditional Chinese
- **`english-zh-cn/`** - English to Simplified Chinese (if available)
- **`spanish-en/`** - Spanish to English (if available)

## Getting Help

- Check existing templates for patterns
- Ask questions in Issues
- Review the main CONTRIBUTING.md
- Test thoroughly before submitting