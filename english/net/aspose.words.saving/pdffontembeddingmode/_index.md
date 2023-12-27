---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.PdfFontEmbeddingMode enum. Specifies how Aspose.Words should embed fonts in C#.
type: docs
weight: 5580
url: /net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Specifies how Aspose.Words should embed fonts.

```csharp
public enum PdfFontEmbeddingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words embeds all fonts. |
| EmbedNonstandard | `1` | Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. Only Arial and Times New Roman fonts are affected in this mode because MS Word doesn't embed only these fonts when saving document to PDF. |
| EmbedNone | `2` | Aspose.Words do not embed any fonts. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
