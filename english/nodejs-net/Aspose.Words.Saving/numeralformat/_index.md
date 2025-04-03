---
title: NumeralFormat enumeration
linktitle: NumeralFormat enumeration
articleTitle: NumeralFormat enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.NumeralFormat enumeration. Indicates the symbol set that is used to represent numbers while rendering to fixed page formats."
type: docs
weight: 490
url: /nodejs-net/aspose.words.saving/numeralformat/
---

## NumeralFormat enumeration

Indicates the symbol set that is used to represent numbers
while rendering to fixed page formats.


### Members

| Name | Description |
| --- | --- |
| European | European numerals: 0123456789. |
| ArabicIndic | Numerals used in Arabic: ٠١٢٣٤٥٦٧٨٩. Unicode range U+0660 - u+0669. |
| EasternArabicIndic | Numerals used in Persian and Urdu: ۰۱۲۳۴۵۶۷۸۹. Unicode range U+06F0 - u+06F9. |
| Context | Symbol set is decided from context(locale and RTL property). |
| System | THIS OPTION IS NOT SUPPORTED. Symbol set is decided from regional settings. |

### Examples

Shows how to set the numeral format used when saving to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.localeId = 5121;//new CultureInfo("ar-AR").LCID;
builder.writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Set the "NumeralFormat" property to "NumeralFormat.ArabicIndic" to
// use glyphs from the U+0660 to U+0669 range as numbers.
// Set the "NumeralFormat" property to "NumeralFormat.Context" to
// look up the locale to determine what number of glyphs to use.
// Set the "NumeralFormat" property to "NumeralFormat.EasternArabicIndic" to
// use glyphs from the U+06F0 to U+06F9 range as numbers.
// Set the "NumeralFormat" property to "NumeralFormat.European" to use european numerals.
// Set the "NumeralFormat" property to "NumeralFormat.System" to determine the symbol set from regional settings.
options.numeralFormat = numeralFormat;

doc.save(base.artifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)

