---
title: PdfSaveOptions.embedFullFonts property
linktitle: embedFullFonts property
articleTitle: embedFullFonts property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.embedFullFonts property. Controls how fonts are embedded into the resulting PDF documents."
type: docs
weight: 120
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/embedFullFonts/
---

## PdfSaveOptions.embedFullFonts property

Controls how fonts are embedded into the resulting PDF documents.


```js
get embedFullFonts(): boolean
```

### Remarks

The default value is ``false``, which means the fonts are subsetted before embedding.
Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all
unused glyphs from a font.

When this value is set to ``true``, a complete font file is embedded into PDF without
subsetting. This will result in larger output files, but can be a useful option when you want to
edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting
will result in large output documents.




### Examples

Shows how to enable or disable subsetting when embedding fonts while rendering a document to PDF.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.font.name = "Arial";
builder.writeln("Hello world!");
builder.font.name = "Arvo";
builder.writeln("The quick brown fox jumps over the lazy dog.");

// Configure our font sources to ensure that we have access to both the fonts in this document.
let originalFontsSources = aw.Fonts.FontSettings.defaultInstance.getFontsSources();
let folderFontSource =  new aw.Fonts.FolderFontSource(base.fontsDir, true);
aw.Fonts.FontSettings.defaultInstance.setFontsSources([ originalFontsSources.at(0), folderFontSource ]);

let fontSources = aw.Fonts.FontSettings.defaultInstance.getFontsSources();
expect(fontSources[0].getAvailableFonts().some(f => f.fullFontName == "Arial")).toEqual(true);
expect(fontSources[1].getAvailableFonts().some(f => f.fullFontName == "Arvo")).toEqual(true);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
let options = new aw.Saving.PdfSaveOptions();

// Since our document contains a custom font, embedding in the output document may be desirable.
// Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
// The document's size may become very large, but we will have full use of all fonts if we edit the PDF.
// Set the "EmbedFullFonts" property to "false" to apply subsetting to fonts, saving only the glyphs
// that the document is using. The file will be considerably smaller,
// but we may need access to any custom fonts if we edit the document.
options.embedFullFonts = embedFullFonts;

doc.save(base.artifactsDir + "PdfSaveOptions.embedFullFonts.pdf", options);

// Restore the original font sources.
aw.Fonts.FontSettings.defaultInstance.setFontsSources(originalFontsSources);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

