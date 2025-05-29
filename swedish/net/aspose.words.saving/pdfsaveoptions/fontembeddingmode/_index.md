---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FontEmbeddingMode i PdfSaveOptions för att optimera inbäddningen av teckensnitt i din PDF. Förbättra dokumentkvalitet och kompatibilitet utan ansträngning!
type: docs
weight: 170
url: /sv/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Anger inbäddningsläget för teckensnitt.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Anmärkningar

Standardvärdet ärEmbedAll.

Den här inställningen fungerar endast för text i ANSI-kodning (Windows-1252). Om dokumentet innehåller icke-ANSI-text kommer motsvarande teckensnitt att bäddas in oavsett den här inställningen.

PDF/A- och PDF/UA-efterlevnad kräver att alla teckensnitt är inbäddade. EmbedAll värdet kommer att användas automatiskt när man sparar till PDF/A och PDF/UA.

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

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
