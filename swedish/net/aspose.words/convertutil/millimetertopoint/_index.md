---
title: ConvertUtil.MillimeterToPoint
second_title: Aspose.Words för .NET API Referens
description: ConvertUtil metod. Konverterar millimeter till punkter.
type: docs
weight: 20
url: /sv/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Konverterar millimeter till punkter.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| millimeters | Double | Värdet att konvertera. |

### Anmärkningar

1 tum är lika med 25,4 millimeter. 1 tum är lika med 72 poäng.

### Exempel

Visar hur man anger sidegenskaper i millimeter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// En sektions "Sidinställningar" definierar storleken på sidmarginalerna i poäng.
// Vi kan också använda klassen "ConvertUtil" för att använda en mer bekant mätenhet,
// såsom millimeter när man definierar gränser.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// En centimeter är ungefär 28,3 poäng.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Lägg till innehåll för att visa de nya marginalerna.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Se även

* class [ConvertUtil](../)
* namnutrymme [Aspose.Words](../../convertutil/)
* hopsättning [Aspose.Words](../../../)


