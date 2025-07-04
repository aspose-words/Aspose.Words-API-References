---
title: PdfSaveOptions.EmbedFullFonts
linktitle: EmbedFullFonts
articleTitle: EmbedFullFonts
second_title: Aspose.Words for .NET
description: Discover how the PdfSaveOptions EmbedFullFonts feature enhances your PDF documents by ensuring complete font embedding for perfect formatting.
type: docs
weight: 120
url: /net/aspose.words.saving/pdfsaveoptions/embedfullfonts/
---
## PdfSaveOptions.EmbedFullFonts property

Controls how fonts are embedded into the resulting PDF documents.

```csharp
public bool EmbedFullFonts { get; set; }
```

## Remarks

The default value is `false`, which means the fonts are subsetted before embedding. Subsetting is useful if you want to keep the output file size smaller. Subsetting removes all unused glyphs from a font.

When this value is set to `true`, a complete font file is embedded into PDF without subsetting. This will result in larger output files, but can be a useful option when you want to edit the resulting PDF later (e.g. add more text).

Some fonts are large (several megabytes) and embedding them without subsetting will result in large output documents.

## Examples

Shows how to enable or disable subsetting when embedding fonts while rendering a document to PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Configure our font sources to ensure that we have access to both the fonts in this document.
FontSourceBase[] originalFontsSources = FontSettings.DefaultInstance.GetFontsSources();
Aspose.Words.Fonts.FolderFontSource folderFontSource =
    new Aspose.Words.Fonts.FolderFontSource(FontsDir, true);
FontSettings.DefaultInstance.SetFontsSources(new[] { originalFontsSources[0], folderFontSource });

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();
Assert.That(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"), Is.True);
Assert.That(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"), Is.True);

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Since our document contains a custom font, embedding in the output document may be desirable.
// Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
// The document's size may become very large, but we will have full use of all fonts if we edit the PDF.
// Set the "EmbedFullFonts" property to "false" to apply subsetting to fonts, saving only the glyphs
// that the document is using. The file will be considerably smaller,
// but we may need access to any custom fonts if we edit the document.
options.EmbedFullFonts = embedFullFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedFullFonts.pdf", options);

// Restore the original font sources.
FontSettings.DefaultInstance.SetFontsSources(originalFontsSources);
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
