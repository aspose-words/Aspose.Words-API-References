---
title: PdfSaveOptions.ZoomBehavior
second_title: Aspose.Words för .NET API Referens
description: PdfSaveOptions fast egendom. Hämtar eller ställer in ett värde som bestämmer vilken typ av zoom som ska användas när ett dokument öppnas med en PDFvisare.
type: docs
weight: 320
url: /sv/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Hämtar eller ställer in ett värde som bestämmer vilken typ av zoom som ska användas när ett dokument öppnas med en PDF-visare.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

### Anmärkningar

Standardvärdet ärNone , dvs ingen passning tillämpas.

### Exempel

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pdfsaveoptions/)
* hopsättning [Aspose.Words](../../../)


