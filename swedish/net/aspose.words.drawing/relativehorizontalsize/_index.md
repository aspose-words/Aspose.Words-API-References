---
title: RelativeHorizontalSize Enum
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.RelativeHorizontalSize uppräkning. Anger i förhållande till vad bredden på en form eller en textram beräknas horisontellt i C#.
type: docs
weight: 1200
url: /sv/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Anger i förhållande till vad bredden på en form eller en textram beräknas horisontellt.

```csharp
public enum RelativeHorizontalSize
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Margin | `0` | Anger att bredden beräknas i förhållande till utrymmet mellan vänster och höger marginal. |
| Page | `1` | Anger att bredden beräknas i förhållande till sidbredden. |
| LeftMargin | `2` | Anger att bredden beräknas relativt den vänstra marginalens områdesstorlek. |
| RightMargin | `3` | Anger att bredden beräknas relativt den högra marginalytans storlek. |
| InnerMargin | `4` | Anger att bredden beräknas i förhållande till storleken på den inre marginalytan, till den vänstra marginalens områdesstorlek för udda sidor och till den högra marginalens områdesstorlek för jämna sidor. |
| OuterMargin | `5` | Anger att bredden beräknas i förhållande till yttermarginalområdets storlek, till högermarginalområdets storlek för udda sidor och till vänstermarginalens områdesstorlek för jämna sidor. |
| Default | `1` | Standardvärdet ärMargin . |

## Exempel

Visar hur man ställer in relativ storlek och position.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägga till en enkel form med absolut storlek och position.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Ställ in WrapType till WrapType.None eftersom inline-former automatiskt konverteras till absoluta enheter.
shape.WrapType = WrapType.None;

// Kontrollera och ställa in den relativa horisontella storleken.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Ställ in den horisontella storleksbindningen till Margin.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Ställa in bredden till 50 % av Margin width.
    shape.WidthRelative = 50;
}

// Kontrollera och ställa in den relativa vertikala storleken.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Ställa in den vertikala storleksbindningen till Margin.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Ställ in höjden till 30 % av Marginalhöjden.
    shape.HeightRelative = 30;
}

// Kontrollera och ställa in den relativa vertikala positionen.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // att binda positionen till TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Inställning av relativ Top till 30% av TopMargin position.
    shape.TopRelative = 30;
}

// Kontrollera och ställa in den relativa horisontella positionen.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Ställer in positionsbindningen till RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Positionens relativa värde kan vara negativt.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Se även

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
