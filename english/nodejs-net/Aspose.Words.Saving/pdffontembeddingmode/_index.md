---
title: PdfFontEmbeddingMode enumeration
linktitle: PdfFontEmbeddingMode enumeration
articleTitle: PdfFontEmbeddingMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PdfFontEmbeddingMode enumeration. Specifies how Aspose.Words should embed fonts."
type: docs
weight: 650
url: /nodejs-net/aspose.words.saving/pdffontembeddingmode/
---

## PdfFontEmbeddingMode enumeration

Specifies how Aspose.Words should embed fonts.


### Members

| Name | Description |
| --- | --- |
| EmbedAll | Aspose.Words embeds all fonts. |
| EmbedNonstandard | Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. Only Arial and Times New Roman fonts are affected in this mode because MS Word doesn't embed only these fonts when saving document to PDF. |
| EmbedNone | Aspose.Words do not embed any fonts. |

### Examples

Shows how to set Aspose.words to skip embedding Arial and Times New Roman fonts into a PDF document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// "Arial" is a standard font, and "Courier New" is a nonstandard font.
builder.font.name = "Arial";
builder.writeln("Hello world!");
builder.font.name = "Courier New";
builder.writeln("The quick brown fox jumps over the lazy dog.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();
// Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
options.embedFullFonts = true;
// Set the "FontEmbeddingMode" property to "EmbedAll" to embed all fonts in the output PDF.
// Set the "FontEmbeddingMode" property to "EmbedNonstandard" to only allow nonstandard fonts' embedding in the output PDF.
// Set the "FontEmbeddingMode" property to "EmbedNone" to not embed any fonts in the output PDF.
options.fontEmbeddingMode = pdfFontEmbeddingMode;

doc.save(base.artifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### See Also

* module [Aspose.Words.Saving](../)

