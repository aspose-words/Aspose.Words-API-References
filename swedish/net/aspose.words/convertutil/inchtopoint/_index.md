---
title: ConvertUtil.InchToPoint
second_title: Aspose.Words för .NET API Referens
description: ConvertUtil metod. Konverterar tum till poäng.
type: docs
weight: 10
url: /sv/net/aspose.words/convertutil/inchtopoint/
---
## ConvertUtil.InchToPoint method

Konverterar tum till poäng.

```csharp
public static double InchToPoint(double inches)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inches | Double | Värdet att konvertera. |

### Anmärkningar

1 tum är lika med 72 poäng.

### Exempel

Visar hur du justerar pappersstorlek, orientering, marginaler, tillsammans med andra inställningar för ett avsnitt.

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

// En sektions "Sidinställningar" definierar storleken på sidmarginalerna i poäng.
// Vi kan också använda klassen "ConvertUtil" för att använda en mer bekant mätenhet,
// såsom tum när man definierar gränser.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// En tum är 72 poäng.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Lägg till innehåll för att visa de nya marginalerna.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Se även

* class [ConvertUtil](../)
* namnutrymme [Aspose.Words](../../convertutil/)
* hopsättning [Aspose.Words](../../../)


