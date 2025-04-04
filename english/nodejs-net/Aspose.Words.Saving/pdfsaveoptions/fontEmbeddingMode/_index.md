---
title: PdfSaveOptions.fontEmbeddingMode property
linktitle: fontEmbeddingMode property
articleTitle: fontEmbeddingMode property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.fontEmbeddingMode property. Specifies the font embedding mode."
type: docs
weight: 170
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/fontEmbeddingMode/
---

## PdfSaveOptions.fontEmbeddingMode property

Specifies the font embedding mode.


```js
get fontEmbeddingMode(): Aspose.Words.Saving.PdfFontEmbeddingMode
```

### Remarks

The default value is [PdfFontEmbeddingMode.EmbedAll](../../pdffontembeddingmode/#EmbedAll).

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains
non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded.
[PdfFontEmbeddingMode.EmbedAll](../../pdffontembeddingmode/#EmbedAll) value will be used automatically when saving to
PDF/A and PDF/UA.




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

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

