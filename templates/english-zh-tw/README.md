# English → Traditional Chinese Vocabulary Template

🎯 **AI-powered vocabulary cards for learning English with Traditional Chinese translations**

> **語言:** English | [繁體中文](#繁體中文說明)

## What You'll Get

✅ **Rich vocabulary cards** with English definitions and Traditional Chinese translations  
✅ **Beautiful dark theme** with clear typography optimized for studying  
✅ **Multiple example sentences** at B1 and B2 difficulty levels  
✅ **Memory aids** including mnemonics and synonyms/antonyms  
✅ **Audio pronunciation** support built-in  
✅ **Traditional Chinese explanations** for better comprehension

## Card Preview

| **Front (Question)** | **Back (Answer)** |
|:-------------------:|:-----------------:|
| ![Front Card](preview/front.png) | ![Back Card](preview/back.png) |

## Quick Setup

### 1. Generate Your Vocabulary Data

Use the [AI prompt](prompt.md) to generate CSV data for your word list.

### 2. Create Anki Note Type

1. **Open Anki** → **Tools** → **Manage Note Types**
2. **Add** → **Clone: Basic** → Name it "English-Traditional Chinese"
3. **Fields...** → Add these fields in order:
   - Word, Pronunciation, PartOfSpeech, QuickDef, FullDef
   - B1Example, B2Example1, B2Example2, Synonyms, Antonyms
   - Mnemonic, ChTrans, ChDef, Supplement

### 3. Apply Templates

1. **Cards...** in Note Type manager
2. **Front Template:** Copy content from [`front.html`](front.html)
3. **Back Template:** Copy content from [`back.html`](back.html)
4. **Styling:** Copy content from [`style.css`](style.css)
5. **Save**

### 4. Import Your Data

1. **File** → **Import** in Anki
2. Select your CSV file
3. Choose "English-Traditional Chinese" note type
4. Map columns correctly
5. **Import**

## Field Reference

| Field | English Description | 中文說明 |
|-------|-------------------|---------|
| **Word** | Target vocabulary | 學習的單字或片語 |
| **Pronunciation** | IPA or phonetic guide | 音標或發音指南 |
| **PartOfSpeech** | Grammar category | 詞性（名詞、動詞等） |
| **QuickDef** | Brief definition | 簡短定義 |
| **FullDef** | Complete explanation | 完整英文解釋 |
| **B1Example** | Simple example sentence | 簡單例句 |
| **B2Example1** | Complex example sentence | 複雜例句1 |
| **B2Example2** | Another usage example | 複雜例句2 |
| **Synonyms** | Similar words | 同義詞 |
| **Antonyms** | Opposite words | 反義詞 |
| **Mnemonic** | Memory aid | 記憶技巧 |
| **ChTrans** | Traditional Chinese translation | 繁體中文翻譯 |
| **ChDef** | Chinese explanation | 中文解釋 |
| **Supplement** | Additional notes | 補充說明 |

## Customization

### Color Themes

Edit `style.css` CSS variables to change colors:

```css
:root {
  --bg-card:    #2e2e2e;  /* Card background */
  --bg-box:     #383838;  /* Box background */
  --text-main:  #eeeeee;  /* Main text color */
  --text-muted: #bbb;     /* Secondary text */
  --accent:     #88c0d0;  /* Accent color */
  --border:     #555;     /* Border color */
}
```

### Field Display

Modify the HTML templates to show/hide specific fields or change layouts.

---

## 繁體中文說明

### 快速設置

1. **生成詞彙數據：** 使用 [AI 提示](prompt.md) 生成您的單字清單的 CSV 檔案
2. **創建 Anki 筆記類型：** 按照上述步驟創建「英文-繁體中文」筆記類型
3. **應用模板：** 複製 HTML 和 CSS 模板到 Anki
4. **匯入數據：** 將 CSV 檔案匯入到 Anki

### 欄位說明

此模板專為學習英文的繁體中文使用者設計，包含：
- **完整的英文定義和例句**
- **繁體中文翻譯和解釋**
- **記憶技巧和同反義詞**
- **美觀的深色主題設計**

### 自定義

您可以修改 CSS 檔案來更改顏色主題，或編輯 HTML 模板來調整卡片佈局。

### 疑難排解

如果卡片顯示不正確：
1. 確認已正確複製所有模板檔案
2. 檢查欄位順序是否與 CSV 檔案一致
3. 確認已套用 CSS 樣式

---

**需要幫助？** 請查看主要的 [README.md](../../README.md) 或建立 Issue。