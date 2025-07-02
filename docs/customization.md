# Template Customization Guide

This guide explains how to customize and modify language templates to suit your specific needs.

## Overview

Each language template consists of:
- **HTML Templates**: Structure and content layout
- **CSS Styling**: Colors, fonts, and visual design
- **Field Configuration**: Data structure and requirements
- **AI Prompt**: Instructions for generating vocabulary data

## CSS Customization

### Color Themes

Most templates use CSS variables for easy color customization:

```css
:root {
  /* Main colors */
  --bg-card:    #2e2e2e;  /* Card background */
  --bg-box:     #383838;  /* Content box background */
  --text-main:  #eeeeee;  /* Primary text color */
  --text-muted: #bbb;     /* Secondary text color */
  --accent:     #88c0d0;  /* Accent/highlight color */
  --border:     #555;     /* Border color */
}
```

#### Creating Light Theme
```css
:root {
  --bg-card:    #ffffff;
  --bg-box:     #f8f9fa;
  --text-main:  #212529;
  --text-muted: #6c757d;
  --accent:     #007bff;
  --border:     #dee2e6;
}
```

#### Creating Custom Color Schemes
```css
/* Blue theme */
:root {
  --bg-card:    #1a1d23;
  --bg-box:     #2c3e50;
  --text-main:  #ecf0f1;
  --text-muted: #bdc3c7;
  --accent:     #3498db;
  --border:     #34495e;
}

/* Green theme */
:root {
  --bg-card:    #1e2d1e;
  --bg-box:     #2d4a2d;
  --text-main:  #e0f0e0;
  --text-muted: #a0c0a0;
  --accent:     #27ae60;
  --border:     #4a664a;
}
```

### Typography

#### Font Families
```css
:root {
  /* Western languages */
  --font-main: "Helvetica Neue", Arial, sans-serif;
  
  /* Chinese */
  --font-chinese: "PingFang SC", "Microsoft YaHei", sans-serif;
  
  /* Japanese */
  --font-japanese: "Hiragino Sans", "Yu Gothic", sans-serif;
  
  /* Korean */
  --font-korean: "Malgun Gothic", "Apple SD Gothic Neo", sans-serif;
  
  /* Arabic */
  --font-arabic: "Tahoma", "Arial Unicode MS", sans-serif;
}
```

#### Font Sizes
```css
.word {
  font-size: 2em;    /* Main word size */
}

.pronunciation {
  font-size: 0.9em;  /* Pronunciation size */
}

.content {
  font-size: 1em;    /* Body text size */
}

.label {
  font-size: 0.85em; /* Label size */
}
```

#### Mobile Responsive Fonts
```css
@media (max-width: 600px) {
  .word {
    font-size: 1.5em;
  }
  
  .content {
    font-size: 0.9em;
  }
}
```

## HTML Template Customization

### Adding New Fields

1. **Add field in Anki**: Tools → Manage Note Types → Fields → Add
2. **Update HTML template**:

```html
<!-- Add this where you want the field to appear -->
{{#NewField}}
<p class="label-inline">
  <span class="label">NEW FIELD:</span> 
  <span class="content">{{NewField}}</span>
</p>
{{/NewField}}
```

### Conditional Display

Show fields only when they contain data:

```html
<!-- Only show if field has content -->
{{#FieldName}}
<div class="field-content">{{FieldName}}</div>
{{/FieldName}}

<!-- Show different content based on field -->
{{#Audio}}
<audio controls>
  <source src="{{Audio}}" type="audio/mpeg">
</audio>
{{/Audio}}
```

### Layout Modifications

#### Two-Column Layout
```html
<div class="row">
  <div class="col-left">
    {{#Synonyms}}<p>Synonyms: {{Synonyms}}</p>{{/Synonyms}}
  </div>
  <div class="col-right">
    {{#Antonyms}}<p>Antonyms: {{Antonyms}}</p>{{/Antonyms}}
  </div>
</div>
```

```css
.row {
  display: flex;
  gap: 20px;
}

.col-left, .col-right {
  flex: 1;
}

@media (max-width: 600px) {
  .row {
    flex-direction: column;
  }
}
```

#### Tabbed Interface
```html
<div class="tabs">
  <div class="tab-buttons">
    <button class="tab-btn active" onclick="showTab('definition')">Definition</button>
    <button class="tab-btn" onclick="showTab('examples')">Examples</button>
  </div>
  
  <div id="definition" class="tab-content active">
    {{#QuickDef}}<p>{{QuickDef}}</p>{{/QuickDef}}
  </div>
  
  <div id="examples" class="tab-content">
    {{#Example1}}<p>{{Example1}}</p>{{/Example1}}
  </div>
</div>
```

## Language-Specific Customizations

### Right-to-Left Languages (Arabic, Hebrew)

```css
.rtl-content {
  direction: rtl;
  text-align: right;
}

.word {
  direction: rtl;
  font-family: "Tahoma", "Arial Unicode MS", sans-serif;
}
```

```html
<div class="word rtl-content">{{Word}}</div>
```

### Japanese with Furigana

```html
<ruby class="word">
  {{Kanji}}<rt>{{Furigana}}</rt>
</ruby>
```

```css
ruby {
  font-size: 2em;
}

rt {
  font-size: 0.5em;
  color: var(--text-muted);
}
```

### Chinese with Pinyin

```html
<div class="chinese-word">
  <div class="characters">{{Word}}</div>
  {{#Pinyin}}<div class="pinyin">{{Pinyin}}</div>{{/Pinyin}}
</div>
```

```css
.characters {
  font-size: 2em;
  font-family: "PingFang SC", "Microsoft YaHei", sans-serif;
}

.pinyin {
  font-size: 0.9em;
  color: var(--text-muted);
  margin-top: 4px;
}
```

## Advanced Customizations

### Progress Indicators

```html
<div class="progress-bar">
  <div class="progress" style="width: {{Progress}}%"></div>
</div>
```

```css
.progress-bar {
  width: 100%;
  height: 4px;
  background: var(--border);
  border-radius: 2px;
  overflow: hidden;
}

.progress {
  height: 100%;
  background: var(--accent);
  transition: width 0.3s ease;
}
```

### Interactive Elements

```html
<button onclick="playAudio('{{Word}}')">🔊</button>
<button onclick="showHint()">💡</button>
```

```javascript
function playAudio(word) {
  // Text-to-speech functionality
  if ('speechSynthesis' in window) {
    const utterance = new SpeechSynthesisUtterance(word);
    speechSynthesis.speak(utterance);
  }
}

function showHint() {
  // Show/hide hint content
  const hint = document.querySelector('.hint');
  hint.style.display = hint.style.display === 'none' ? 'block' : 'none';
}
```

### Animations

```css
.card-front, .card-back {
  animation: fadeIn 0.3s ease-in-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

.word {
  transition: color 0.3s ease;
}

.word:hover {
  color: var(--accent);
}
```

## Field Configuration

### Adding Custom Fields

To add custom fields to your template:

1. **Add field in Anki**: Tools → Manage Note Types → Fields → Add
2. **Update HTML templates** to include the new field
3. **Modify AI prompt** to generate data for your custom fields

### AI Prompt Customization

Update the AI prompt to generate data for your custom fields:

```markdown
- **Gender**
The grammatical gender for Spanish nouns (masculine, feminine, or leave blank for other parts of speech).

- **Conjugation**  
For verbs, provide the present tense conjugation (yo, tú, él/ella).
```

## Testing Your Customizations

### Local Testing
1. **Create test cards** with sample data
2. **Preview in Anki** to check display
3. **Test on mobile** device
4. **Verify all fields** render correctly

### Validation Checklist
- [ ] All new fields display properly
- [ ] Mobile responsiveness maintained
- [ ] Colors have sufficient contrast
- [ ] Fonts render correctly for your language
- [ ] No JavaScript errors in console
- [ ] CSS doesn't break existing layouts

## Sharing Your Customizations

### Creating a New Template
1. Copy an existing template directory
2. Modify all files for your customizations
3. Test thoroughly
4. Create documentation
5. Submit as a pull request

### Contributing Improvements
1. Fork the repository
2. Make your changes
3. Test with multiple word sets
4. Update documentation
5. Submit pull request with description

## Common Pitfalls

### CSS Issues
- **Specificity problems**: Use more specific selectors
- **Mobile breakage**: Test responsive design
- **Font loading**: Ensure fallback fonts

### HTML Problems
- **Field name mismatches**: Verify field names exactly match
- **Broken conditional logic**: Test with empty fields
- **Invalid HTML**: Validate markup

### JavaScript Errors
- **Undefined functions**: Check function definitions
- **Mobile compatibility**: Test on actual devices
- **Security restrictions**: Some features may be limited

---

**Need help with customization?** Create an issue with your specific requirements and we'll help you get started!