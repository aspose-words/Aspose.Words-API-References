---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfZoomBehavior-enum för anpassningsbara PDF-zoominställningar. Förbättra användarupplevelsen med skräddarsydda visningsalternativ i PDF-dokument.
type: docs
weight: 6340
url: /sv/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Anger vilken typ av zoom som tillämpas på ett PDF-dokument när det öppnas i en PDF-läsare.

```csharp
public enum PdfZoomBehavior
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Hur dokumentet visas beror på PDF-läsaren. Vanligtvis visar läsaren dokumentet så att det passar sidbredden. |
| ZoomFactor | `1` | Visar sidan med den angivna zoomfaktorn. |
| FitPage | `2` | Visar sidan så att den är helt synlig. |
| FitWidth | `3` | Anpassar sidans bredd. |
| FitHeight | `4` | Anpassar sidans höjd. |
| FitBox | `5` | Anpassar avgränsningsramen (rektangeln som innehåller alla synliga element på sidan). |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
