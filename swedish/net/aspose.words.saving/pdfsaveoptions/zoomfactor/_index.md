---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions ZoomFactor-egenskap för att enkelt justera dokumentzoomnivåer i procent, vilket förbättrar din PDF-visningsupplevelse.
type: docs
weight: 360
url: /sv/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Hämtar eller ställer in ett värde som bestämmer zoomfaktorn (i procent) för ett dokument.

```csharp
public int ZoomFactor { get; set; }
```

## Anmärkningar

Detta värde används endast om[`ZoomBehavior`](../zoombehavior/) är inställd påZoomFactor .

## Exempel

Visar hur man ställer in standardzoomningen som en läsare använder när ett renderat PDF-dokument öppnas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ZoomBehavior" till "PdfZoomBehavior.ZoomFactor" för att få en PDF-läsare att
// tillämpa en procentbaserad zoomfaktor när vi öppnar dokumentet med den.
// Sätt egenskapen "ZoomFactor" till "25" för att ge zoomfaktorn ett värde på 25 %.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// När vi öppnar det här dokumentet med en läsare som Adobe Acrobat, ser vi dokumentet skalat till 1/4 av sin faktiska storlek.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
