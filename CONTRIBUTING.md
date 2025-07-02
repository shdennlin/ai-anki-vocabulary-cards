# Contributing to Anki Language Templates

We welcome contributions! This project supports multiple language pairs for vocabulary learning, and we're always looking for new templates, improvements, and language combinations.

## 🌍 Types of Contributions

### 1. New Language Templates
Create templates for new language pairs (e.g., Spanish→English, French→German, Japanese→English).

### 2. Template Improvements
Enhance existing templates with better styling, additional fields, or improved functionality.

### 3. Documentation
Improve setup guides, add translations, or create tutorials.

### 4. Tools and Scripts
Build utilities for template validation, testing, or automation.

## 🚀 Quick Start for Contributors

### Prerequisites
- Git knowledge
- Basic HTML/CSS skills
- Anki installed for testing
- Access to AI tools (ChatGPT, Claude) for prompt testing

### Setting Up
1. Fork this repository
2. Clone your fork: `git clone https://github.com/your-username/anki-card-template-for-learn-language.git`
3. Create a feature branch: `git checkout -b feature/your-feature-name`

## 📝 Creating a New Language Template

### Step 1: Choose Your Language Pair
- **Target Language**: The language being learned
- **Native Language**: The learner's native language
- **Template Name**: Format as `[target]-[native]` (e.g., `spanish-en`, `french-de`)

### Step 2: Use the Template Base
```bash
cp -r templates/_template-base templates/your-language-pair
cd templates/your-language-pair
```

### Step 3: Customize Files

#### Required Files Checklist:
- [ ] `README.md` - Setup instructions in both languages
- [ ] `front.html` - Anki front template
- [ ] `back.html` - Anki back template
- [ ] `style.css` - Card styling
- [ ] `prompt.md` - AI generation prompt
- [ ] `fields.json` - Field configuration
- [ ] `preview/front.png` - Front card screenshot
- [ ] `preview/back.png` - Back card screenshot

### Step 4: Customize Each File

#### `fields.json`
```json
{
  "templateName": "Spanish → English Vocabulary",
  "targetLanguage": "Spanish",
  "nativeLanguage": "English",
  "ankiFields": [
    // Update field definitions for your language pair
  ]
}
```

#### HTML Templates
- Update field references to match your `fields.json`
- Add language-specific elements (furigana, diacritics, etc.)
- Adjust layout for text direction (RTL for Arabic/Hebrew)

#### `style.css`
```css
:root {
  --font-native: "Font for your native language";
  /* Add language-specific font stacks */
}
```

#### `prompt.md`
- Adapt the AI prompt for your language pair
- Include language-specific instructions
- Add examples in both languages

### Step 5: Testing
1. Generate test vocabulary with your AI prompt
2. Import CSV into Anki using your templates
3. Test on desktop and mobile
4. Verify all fields display correctly
5. Check text rendering and fonts

### Step 6: Documentation
- Complete the README.md with setup instructions
- Add examples in both languages
- Include troubleshooting tips
- Take screenshots for the preview folder

## 🎨 Design Guidelines

### Color Themes
- Use the existing CSS variable system for consistency
- Dark theme by default, but provide light theme alternatives
- Ensure good contrast ratios (WCAG AA compliance)

### Typography
- Choose appropriate fonts for your language's script
- Consider readability at different sizes
- Test on various devices

### Layout
- Mobile-first responsive design
- Support for different text directions (LTR/RTL)
- Clean, uncluttered appearance

## 🌐 Language-Specific Considerations

### Chinese (Simplified/Traditional)
- Include pinyin/zhuyin pronunciation
- Handle character variants properly
- Consider stroke order information

### Japanese
- Support furigana for kanji
- Include multiple reading systems
- Consider JLPT level indicators

### Arabic/Hebrew
- Implement RTL text direction
- Handle diacritical marks correctly
- Support mixed LTR/RTL content

### European Languages
- Include grammatical gender
- Add case information where relevant
- Consider CEFR level examples

### Other Scripts
- Ensure proper Unicode support
- Test character rendering
- Include appropriate input methods

## 🧪 Testing Your Contribution

### Manual Testing
1. **Template Import**: Successfully import into Anki
2. **Field Display**: All fields render correctly
3. **Mobile Compatibility**: Cards work on mobile devices
4. **Text Rendering**: Characters display properly
5. **TTS Support**: Audio pronunciation works (if applicable)

### Validation Tools
```bash
# Validate HTML (if available)
python tools/validate-template.py templates/your-language-pair

# Test CSV generation
# Generate sample CSV using your prompt
# Import into Anki to verify
```

## 📋 Pull Request Guidelines

### Before Submitting
- [ ] All files in template directory complete
- [ ] Templates tested in Anki
- [ ] Screenshots included
- [ ] Documentation written
- [ ] AI prompt functional
- [ ] Code follows project style

### PR Template
Use this format for your pull request:

```markdown
## Language Template: [Target] → [Native]

### Overview
Brief description of the language pair and any special features.

### Testing
- [ ] Templates import successfully into Anki
- [ ] All fields display correctly
- [ ] Mobile compatibility verified
- [ ] AI prompt generates valid CSV
- [ ] Screenshots captured

### Language-Specific Features
- Feature 1 (e.g., tone marks for Chinese)
- Feature 2 (e.g., case marking for German)
- Feature 3 (e.g., furigana for Japanese)

### Files Added
- templates/[language-pair]/README.md
- templates/[language-pair]/front.html
- templates/[language-pair]/back.html
- templates/[language-pair]/style.css
- templates/[language-pair]/prompt.md
- templates/[language-pair]/fields.json
- templates/[language-pair]/preview/front.png
- templates/[language-pair]/preview/back.png

### Additional Notes
Any special considerations or known limitations.
```

## 🛠️ Development Tools

### Creating Templates
```bash
# Copy base template
cp -r templates/_template-base templates/new-language-pair

# Run validation (if available)
python tools/validate-template.py templates/new-language-pair
```

### Taking Screenshots
1. Create test cards in Anki
2. Use Anki's preview function
3. Take clean screenshots at standard resolution
4. Save as `front.png` and `back.png` in preview folder

## 📚 Resources

### Language Resources
- [ISO 639 Language Codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)
- [Unicode Character Database](https://unicode.org/ucd/)
- [Google Fonts](https://fonts.google.com/) for language-specific fonts

### Anki Resources
- [Anki Manual](https://docs.ankiweb.net/)
- [Template Reference](https://docs.ankiweb.net/templates/intro.html)
- [Field Replacements](https://docs.ankiweb.net/templates/fields.html)

### AI Prompt Resources
- [ChatGPT Best Practices](https://platform.openai.com/docs/guides/prompt-engineering)
- [Claude Prompt Engineering](https://docs.anthropic.com/claude/docs/prompt-engineering)

## 🤝 Community

### Getting Help
- Open an issue for questions
- Check existing templates for examples
- Review the base template documentation

### Code of Conduct
- Be respectful and inclusive
- Provide constructive feedback
- Help others learn and contribute

### Recognition
Contributors will be acknowledged in:
- README.md contributors section
- Individual template documentation
- Release notes for major contributions

## 📄 License

By contributing to this project, you agree that your contributions will be licensed under the same MIT License that covers the project.

---

**Thank you for contributing to making language learning more accessible!** 🎉