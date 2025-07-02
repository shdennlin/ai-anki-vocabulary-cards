# General Anki Setup Guide

This guide covers the general process of setting up Anki with language templates. For language-specific instructions, refer to your template's README.

## Prerequisites

- **Anki installed** on your device ([Download here](https://apps.ankiweb.net/))
- **Access to AI** (ChatGPT, Claude, or similar) for generating vocabulary data
- **5-10 minutes** for initial setup

## Step 1: Choose Your Language Template

Visit the main README to see available language templates:
- [English → Traditional Chinese](../templates/english-zh-tw/)
- More templates coming soon!

Each template includes:
- Complete setup instructions
- AI prompt for generating data
- HTML/CSS template files
- Field configuration
- Example screenshots

## Step 2: Generate Vocabulary Data

1. **Prepare word list**: Create a list of words/phrases you want to learn
2. **Use AI prompt**: Copy the template's AI prompt
3. **Generate CSV**: Paste your word list and get CSV output
4. **Download file**: Save the CSV to your computer

## Step 3: Create Anki Note Type

1. **Open Anki** → **Tools** → **Manage Note Types**
2. **Add new type** → **Clone: Basic**
3. **Name your template** (e.g., "English-Chinese Vocabulary")
4. **Add fields** according to your template's requirements

### Common Field Types
- **Word/Term**: The vocabulary being learned
- **Pronunciation**: Phonetic guide or audio
- **Definition**: Meaning in target language
- **Translation**: Native language translation
- **Examples**: Usage examples
- **Notes**: Additional information

## Step 4: Apply Template Styling

1. **Click "Cards..."** in Note Type manager
2. **Front Template**: Copy from template's `front.html`
3. **Back Template**: Copy from template's `back.html`
4. **Styling**: Copy from template's `style.css`
5. **Save changes**

## Step 5: Import Your Data

1. **File** → **Import** in Anki
2. **Select CSV file**
3. **Choose note type** (the one you just created)
4. **Map columns** to fields
5. **Import**

## Step 6: Test and Study

1. **Preview cards** to ensure proper display
2. **Test on mobile** if you use AnkiMobile/AnkiDroid
3. **Adjust styling** if needed
4. **Start studying!**

## Troubleshooting

### Cards Display Issues
- Verify all template files were copied correctly
- Check that field names match between CSV and template
- Ensure CSS was applied in the Styling section

### Import Problems
- Verify CSV column order matches template requirements
- Check for special characters or encoding issues
- Make sure note type has all required fields

### Mobile Display
- Templates are designed to be mobile-responsive
- Test on your mobile device
- Adjust font sizes in CSS if needed

### Font Issues
- Some languages may need specific fonts
- Check template documentation for font recommendations
- Install additional fonts if needed

## Customization

### Changing Colors
Most templates use CSS variables for easy customization:

```css
:root {
  --bg-card: #2e2e2e;    /* Card background */
  --text-main: #eeeeee;  /* Text color */
  --accent: #88c0d0;     /* Accent color */
}
```

### Adding Fields
1. Add field in Note Type manager
2. Update HTML templates to display the field
3. Modify AI prompt to generate data for new field

### Layout Changes
- Edit HTML templates for structural changes
- Modify CSS for styling adjustments
- Test on both desktop and mobile

## Best Practices

### Data Generation
- Start with 10-20 words to test your setup
- Review AI-generated content for accuracy
- Edit CSV file to fix any errors before import

### Study Habits
- Use Anki's spaced repetition consistently
- Review cards daily for best results
- Adjust new card limits based on your capacity

### Maintenance
- Regular backups of your Anki collection
- Update templates when improvements are released
- Contribute feedback to help improve templates

## Getting Help

- **Template-specific issues**: Check your template's README
- **General Anki help**: [Official Anki Manual](https://docs.ankiweb.net/)
- **Community support**: Create an issue on GitHub

---

**Need template-specific help?** Each language template has its own detailed setup guide with language-specific tips and troubleshooting!