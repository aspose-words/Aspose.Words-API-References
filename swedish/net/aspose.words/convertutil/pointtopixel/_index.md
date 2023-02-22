---
title: ConvertUtil.PointToPixel
second_title: Aspose.Words för .NET API Referens
description: ConvertUtil metod. Konverterar punkter till pixlar vid 96 dpi.
type: docs
weight: 60
url: /sv/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(double) {#pointtopixel}

Konverterar punkter till pixlar vid 96 dpi.

```csharp
public static double PointToPixel(double points)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| points | Double | Värdet att konvertera. |

### Anmärkningar

1 tum är lika med 72 poäng.

### Exempel

Visar hur man anger sidegenskaper i pixlar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En sektions "Sidinställningar" definierar storleken på sidmarginalerna i poäng.
// Vi kan också använda klassen "ConvertUtil" för att använda en annan måttenhet,
// som pixlar när man definierar gränser.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// En pixel är 0,75 poäng.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// Standardvärdet för DPI som används är 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Lägg till innehåll för att visa de nya marginalerna.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Se även

* class [ConvertUtil](../)
* namnutrymme [Aspose.Words](../../convertutil/)
* hopsättning [Aspose.Words](../../../)

---

## PointToPixel(double, double) {#pointtopixel_1}

Konverterar punkter till pixlar vid den angivna pixelupplösningen.

```csharp
public static double PointToPixel(double points, double resolution)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| points | Double | Värdet att konvertera. |
| resolution | Double | Upplösningen dpi (dots per inch). |

### Anmärkningar

1 tum är lika med 72 poäng.

### Exempel

Visar hur man använder konvertera punkter till pixlar med standard och anpassad upplösning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definiera storleken på den övre marginalen för detta avsnitt i pixlar, enligt en anpassad DPI.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Vid standard DPI på 96 är en pixel 0,75 poäng.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Ställ in en ny DPI och justera toppmarginalvärdet därefter.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Se även

* class [ConvertUtil](../)
* namnutrymme [Aspose.Words](../../convertutil/)
* hopsättning [Aspose.Words](../../../)


