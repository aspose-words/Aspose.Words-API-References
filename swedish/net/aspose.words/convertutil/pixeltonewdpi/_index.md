---
title: ConvertUtil.PixelToNewDpi
linktitle: PixelToNewDpi
articleTitle: PixelToNewDpi
second_title: Aspose.Words för .NET
description: Omvandla pixelupplösningar enkelt med ConvertUtils PixelToNewDpi-metod. Uppnå optimal bildkvalitet och precision för dina projekt.
type: docs
weight: 30
url: /sv/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Konverterar pixlar från en upplösning till en annan.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| pixels | Double | Värdet som ska konverteras. |
| oldDpi | Double | Den aktuella dpi-upplösningen (punkter per tum). |
| newDpi | Double | Den nya dpi-upplösningen (punkter per tum). |

## Exempel

Visar hur man använder konvertera punkter till pixlar med standard- och anpassad upplösning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definiera storleken på den övre marginalen för detta avsnitt i pixlar, enligt en anpassad DPI.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Vid standard-DPI på 96 är en pixel 0,75 punkter.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Ställ in en ny DPI och justera värdet för den övre marginalen därefter.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Se även

* class [ConvertUtil](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
