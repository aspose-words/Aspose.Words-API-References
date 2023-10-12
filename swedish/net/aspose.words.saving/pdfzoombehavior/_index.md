---
title: Enum PdfZoomBehavior
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.PdfZoomBehavior uppräkning. Anger typen av zoom som tillämpas på ett PDFdokument när det öppnas i en PDFvisare.
type: docs
weight: 5540
url: /sv/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Anger typen av zoom som tillämpas på ett PDF-dokument när det öppnas i en PDF-visare.

```csharp
public enum PdfZoomBehavior
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Hur dokumentet visas överlåts till PDF-läsaren. Vanligtvis visar visningsprogrammet dokumentet så att det passar sidbredden. |
| ZoomFactor | `1` | Visar sidan med den angivna zoomfaktorn. |
| FitPage | `2` | Visar sidan så att den är helt synlig. |
| FitWidth | `3` | Passar sidans bredd. |
| FitHeight | `4` | Passar höjden på sidan. |
| FitBox | `5` | Passar begränsningsrutan (rektangel som innehåller alla synliga element på sidan). |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


