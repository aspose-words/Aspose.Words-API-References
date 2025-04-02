---
title: PdfSaveOptions.useCoreFonts property
linktitle: useCoreFonts property
articleTitle: useCoreFonts property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.useCoreFonts property. Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman, Courier New and Symbol with core PDF Type 1 fonts."
type: docs
weight: 330
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/useCoreFonts/
---

## PdfSaveOptions.useCoreFonts property

Gets or sets a value determining whether or not to substitute TrueType fonts Arial, Times New Roman,
Courier New and Symbol with core PDF Type 1 fonts.


```js
get useCoreFonts(): boolean
```

### Remarks

The default value is ``False``. When this value is set to ``True`` Arial, Times New Roman,
Courier New and Symbol fonts are replaced in PDF document with corresponding core Type 1 font.

Core PDF fonts, or their font metrics and suitable substitution fonts, are required to be available to any
PDF viewer application.

This setting works only for the text in ANSI (Windows-1252) encoding. Non-ANSI text will be written
with embedded TrueType font regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. ``False`` value will be used
automatically when saving to PDF/A and PDF/UA.

Core fonts are not supported when saving to PDF 2.0 format. ``False`` value will be used
automatically when saving to PDF 2.0.

This option has a higher priority then [PdfSaveOptions.fontEmbeddingMode](../fontEmbeddingMode/) option.




### Examples

Shows how enable/disable PDF Type 1 font substitution.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Arial";
builder.writeln("Hello world!");
builder.font.name = "Courier New";
builder.writeln("The quick brown fox jumps over the lazy dog.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();
// Set the "UseCoreFonts" property to "true" to replace some fonts,
// including the two fonts in our document, with their PDF Type 1 equivalents.
// Set the "UseCoreFonts" property to "false" to not apply PDF Type 1 fonts.
options.useCoreFonts = useCoreFonts;

doc.save(base.artifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

