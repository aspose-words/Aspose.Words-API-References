---
title: ConvertUtil.PointToInch
linktitle: PointToInch
articleTitle: PointToInch
second_title: Aspose.Words för .NET
description: Konvertera enkelt punkter till tum med ConvertUtils PointToInch-metod. Förenkla dina mått och förbättra din designnoggrannhet idag!
type: docs
weight: 50
url: /sv/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Omvandlar punkter till tum.

```csharp
public static double PointToInch(double points)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| points | Double | Värdet som ska konverteras. |

## Anmärkningar

1 tum är lika med 72 punkter.

## Exempel

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

* class [ConvertUtil](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
