---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words för .NET
description: Upptäck enumerationen Aspose.Words.Drawing.RelativeVerticalSize, som definierar beräkningar av vertikal höjd för former och textramar, vilket förbättrar precisionen i dokumentlayouten.
type: docs
weight: 1610
url: /sv/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Anger relativt till vad höjden på en form eller en textram beräknas vertikalt.

```csharp
public enum RelativeVerticalSize
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Margin | `0` | Anger att höjden beräknas i förhållande till avståndet mellan den övre och nedre marginalen. |
| Page | `1` | Anger att höjden beräknas relativt till sidans höjd. |
| TopMargin | `2` | Anger att höjden beräknas relativt till den övre marginalens storlek. |
| BottomMargin | `3` | Anger att höjden beräknas relativt till den nedre marginalens storlek. |
| InnerMargin | `4` | Anger att höjden beräknas i förhållande till den inre marginalytans storlek, i förhållande till den övre marginalytans storlek för udda sidor och i förhållande till den nedre marginalytans storlek för jämna sidor. |
| OuterMargin | `5` | Anger att höjden beräknas i förhållande till den yttre marginalens storlek, i förhållande till den nedre marginalens storlek för udda sidor och i förhållande till den övre marginalens storlek för jämna sidor. |
| Default | `1` | Standardvärdet ärMargin . |

## Exempel

Visar hur man ställer in relativ storlek och position.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägger till en enkel form med absolut storlek och position.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Sätt WrapType till WrapType.None eftersom inbäddade former automatiskt konverteras till absoluta enheter.
shape.WrapType = WrapType.None;

// Kontroll och inställning av relativ horisontell storlek.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Ställer in den horisontella storleksbindningen till Marginal.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Ställer in bredden till 50% av marginalbredden.
    shape.WidthRelative = 50;
}

// Kontroll och inställning av relativ vertikal storlek.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Ställer in den vertikala storleksbindningen till Marginal.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Ställer in höjden till 30 % av marginalhöjden.
    shape.HeightRelative = 30;
}

// Kontroll och inställning av relativ vertikal position.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // binder positionen till TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Ställer in relativ topp till 30 % av TopMargin-positionen.
    shape.TopRelative = 30;
}

// Kontroll och inställning av det relativa horisontella läget.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Ställer in positionsbindningen till RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Positionsrelativa värdet kan vara negativt.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Se även

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
