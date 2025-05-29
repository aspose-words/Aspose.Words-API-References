---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words för .NET
description: Upptäck PdfSaveOptions ZoomBehavior, styr zoominställningarna för optimal visning i PDF-visare. Förbättra användarupplevelsen med skräddarsydd dokumentvisning!
type: docs
weight: 350
url: /sv/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Hämtar eller ställer in ett värde som avgör vilken typ av zoom som ska tillämpas när ett dokument öppnas med en PDF-läsare.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Anmärkningar

Standardvärdet ärNone , dvs. ingen anpassning tillämpas.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
