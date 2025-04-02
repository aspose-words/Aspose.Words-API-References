---
title: FixedPageSaveOptions.numeralFormat property
linktitle: numeralFormat property
articleTitle: numeralFormat property
second_title: Aspose.Words for NodeJs
description: "FixedPageSaveOptions.numeralFormat property. Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/fixedpagesaveoptions/numeralFormat/
---

## FixedPageSaveOptions.numeralFormat property

Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals.
European numerals are used by default.



```js
get numeralFormat(): Aspose.Words.Saving.NumeralFormat
```

### Remarks

If the value of this property is changed and page layout is already built then
[Document.updatePageLayout()](../../../Aspose.Words/document/updatePageLayout/#default) is invoked automatically to update any changes.



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

* module [Aspose.Words.Saving](../../)
* class [FixedPageSaveOptions](../)

