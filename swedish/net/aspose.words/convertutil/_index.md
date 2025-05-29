---
title: ConvertUtil Class
linktitle: ConvertUtil
articleTitle: ConvertUtil
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ConvertUtil för sömlös enhetskonvertering. Förbättra din dokumentbehandling med viktiga hjälpfunktioner idag!
type: docs
weight: 560
url: /sv/net/aspose.words/convertutil/
---
## ConvertUtil class

Tillhandahåller hjälpfunktioner för att konvertera mellan olika måttenheter.

För att lära dig mer, besök[Konvertera mellan måttenheter](https://docs.aspose.com/words/net/convert-between-measurement-units/) dokumentationsartikel.

```csharp
public static class ConvertUtil
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(*double*) | Omvandlar tum till punkter. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(*double*) | Omvandlar millimeter till punkter. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(*double, double, double*) | Konverterar pixlar från en upplösning till en annan. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(*double*) | Konverterar pixlar till punkter med 96 dpi. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(*double, double*) | Konverterar pixlar till punkter med den angivna pixelupplösningen. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(*double*) | Omvandlar punkter till tum. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(*double*) | Konverterar punkter till pixlar med 96 dpi. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(*double, double*) | Konverterar punkter till pixlar med den angivna pixelupplösningen. |

## Exempel

Visar hur man justerar pappersstorlek, orientering, marginaler och andra inställningar för ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

Visar hur man anger sidegenskaper i tum.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En sektions "Sidinställningar" definierar storleken på sidmarginalerna i punkter.
// Vi kan också använda klassen "ConvertUtil" för att använda en mer välbekant måttenhet,
// såsom tum när man definierar gränser.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// En tum är 72 punkter.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Lägg till innehåll för att demonstrera de nya marginalerna.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
