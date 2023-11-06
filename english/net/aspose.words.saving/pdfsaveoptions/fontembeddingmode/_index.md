---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words for .NET
description: PdfSaveOptions FontEmbeddingMode property. Specifies the font embedding mode in C#.
type: docs
weight: 170
url: /net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Specifies the font embedding mode.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Remarks

The default value is EmbedAll.

This setting works only for the text in ANSI (Windows-1252) encoding. If the document contains non-ANSI text then corresponding fonts will be embedded regardless of this setting.

PDF/A and PDF/UA compliance requires all fonts to be embedded. EmbedAll value will be used automatically when saving to PDF/A and PDF/UA.

## Examples

Shows how to set Aspose.Words to skip embedding Arial and Times New Roman fonts into a PDF document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" is a standard font, and "Courier New" is a nonstandard font.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Set the "EmbedFullFonts" property to "true" to embed every glyph of every embedded font in the output PDF.
options.EmbedFullFonts = true;
// Set the "FontEmbeddingMode" property to "EmbedAll" to embed all fonts in the output PDF.
// Set the "FontEmbeddingMode" property to "EmbedNonstandard" to only allow nonstandard fonts' embedding in the output PDF.
// Set the "FontEmbeddingMode" property to "EmbedNone" to not embed any fonts in the output PDF.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### See Also

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
