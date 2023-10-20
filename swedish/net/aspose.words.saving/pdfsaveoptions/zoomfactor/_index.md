---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words för .NET
description: PdfSaveOptions ZoomFactor fast egendom. Hämtar eller ställer in ett värde som bestämmer zoomfaktor i procent för ett dokument i C#.
type: docs
weight: 330
url: /sv/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Hämtar eller ställer in ett värde som bestämmer zoomfaktor (i procent) för ett dokument.

```csharp
public int ZoomFactor { get; set; }
```

## Anmärkningar

Detta värde används endast om[`ZoomBehavior`](../zoombehavior/) är satt tillZoomFactor .

## Exempel

Visar hur du ställer in standardzoomningen som en läsare tillämpar när du öppnar ett renderat PDF-dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ZoomBehavior" till "PdfZoomBehavior.ZoomFactor" för att få en PDF-läsare till
// tillämpa en procentbaserad zoomfaktor när vi öppnar dokumentet med den.
// Ställ in egenskapen "ZoomFactor" till "25" för att ge zoomfaktorn ett värde på 25%.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// När vi öppnar det här dokumentet med en läsare som Adobe Acrobat kommer vi att se dokumentet skalat till 1/4 av dess faktiska storlek.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Se även

* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
