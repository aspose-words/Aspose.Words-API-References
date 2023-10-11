---
title: Enum PdfFontEmbeddingMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.PdfFontEmbeddingMode uppräkning. Anger hur Aspose.Words ska bädda in teckensnitt.
type: docs
weight: 5470
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
| EmbedNonstandard | `1` | Aspose.Words bäddar in alla typsnitt utom standard Windows-teckensnitt Arial och Times New Roman. Endast Arial och Times New Roman-teckensnitt påverkas i det här läget eftersom MS Word inte bäddar in bara dessa teckensnitt när dokument sparas till PDF. |
| EmbedNone | `2` | Aspose.Words bäddar inte in några teckensnitt. |

### Exempel

Visar hur du ställer in Aspose.Words för att hoppa över att bädda in Arial- och Times New Roman-teckensnitt i ett PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" är ett standardteckensnitt och "Courier New" är ett icke-standardtypsnitt.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "EmbedFullFonts" till "true" för att bädda in varje glyf för alla inbäddade teckensnitt i den utgående PDF-filen.
options.EmbedFullFonts = true;

// Ställ in egenskapen "FontEmbeddingMode" till "EmbedAll" för att bädda in alla teckensnitt i utdata-PDF-filen.
// Ställ in egenskapen "FontEmbeddingMode" till "EmbedNonstandard" för att endast tillåta icke-standardtypsnitts inbäddning i utdata-PDF.
// Ställ in egenskapen "FontEmbeddingMode" till "EmbedNone" för att inte bädda in några teckensnitt i utdata-PDF-filen.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);

switch (pdfFontEmbeddingMode)
{
    case PdfFontEmbeddingMode.EmbedAll:
        Assert.That(1000000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNonstandard:
        Assert.That(480000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
    case PdfFontEmbeddingMode.EmbedNone:
        Assert.That(4255, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf").Length));
        break;
}
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


