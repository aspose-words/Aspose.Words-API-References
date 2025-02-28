---
title: PdfSaveOptions
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words for .NET
description: Discover the PdfSaveOptions constructor, designed to effortlessly initialize and save your documents in high-quality PDF format. Streamline your workflow today!
type: docs
weight: 10
url: /net/aspose.words.saving/pdfsaveoptions/pdfsaveoptions/
---
## PdfSaveOptions constructor

Initializes a new instance of this class that can be used to save a document in the Pdf format.

```csharp
public PdfSaveOptions()
```

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
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(fontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

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
