---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.RelativeVerticalSize uppräkning. Anger i förhållande till vad höjden på en form eller en textram beräknas vertikalt i C#.
type: docs
weight: 1220
url: /sv/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Anger i förhållande till vad höjden på en form eller en textram beräknas vertikalt.

```csharp
public enum RelativeVerticalSize
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Margin | `0` | Anger att höjden beräknas i förhållande till utrymmet mellan den övre och nedre marginalen. |
| Page | `1` | Anger att höjden beräknas i förhållande till sidhöjden. |
| TopMargin | `2` | Anger att höjden beräknas i förhållande till den övre marginalytans storlek. |
| BottomMargin | `3` | Anger att höjden beräknas i förhållande till bottenmarginalens storlek. |
| InnerMargin | `4` | Anger att höjden beräknas i förhållande till storleken på den inre marginalytan, till den övre marginalens områdesstorlek för udda sidor och till den nedre marginalens områdesstorlek för jämna sidor. |
| OuterMargin | `5` | Anger att höjden beräknas i förhållande till yttermarginalens områdesstorlek, till den nedre marginalens områdesstorlek för udda sidor och till den övre marginalens områdesstorlek för jämna sidor. |
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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
