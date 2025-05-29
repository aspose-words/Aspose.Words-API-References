---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfFontEmbeddingMode-enum för optimal teckensnittsinbäddning i PDF-filer. Förbättra dokumentkvaliteten och säkerställ en konsekvent textvisning.
type: docs
weight: 6260
url: /sv/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Anger hur Aspose.Words ska bädda in teckensnitt.

```csharp
public enum PdfFontEmbeddingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words bäddar in alla teckensnitt. |
| EmbedNonstandard | `1` | Aspose.Words bäddar in alla teckensnitt förutom standard Windows-teckensnitten Arial och Times New Roman. Endast Arial- och Times New Roman-teckensnitt påverkas i det här läget eftersom MS Word inte bäddar in bara dessa teckensnitt när dokumentet sparas till PDF. |
| EmbedNone | `2` | Aspose.Words bäddar inte in några teckensnitt. |

## Exempel

Visar hur man ställer in Aspose.Words så att det hoppar över att bädda in Arial- och Times New Roman-teckensnitt i ett PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" är ett standardtypsnitt och "Courier New" är ett icke-standardtypsnitt.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Sätt egenskapen "EmbedFullFonts" till "true" för att bädda in alla teckensnitt i varje inbäddat teckensnitt i PDF-filen.
options.EmbedFullFonts = true;
// Ställ in egenskapen "FontEmbeddingMode" till "EmbedAll" för att bädda in alla teckensnitt i PDF-filen.
// Ställ in egenskapen "FontEmbeddingMode" till "EmbedNonstandard" för att endast tillåta inbäddning av icke-standardiserade teckensnitt i PDF-filen.
// Ställ in egenskapen "FontEmbeddingMode" till "EmbedNone" för att inte bädda in några teckensnitt i PDF-filen.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
