---
title: RelativeHorizontalSize Enum
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.RelativeHorizontalSize enum för exakt kontroll över form och textramsbredder i dina dokument. Förbättra din formatering idag!
type: docs
weight: 1590
url: /sv/net/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enumeration

Anger relativt till vad bredden på en form eller en textram beräknas horisontellt.

```csharp
public enum RelativeHorizontalSize
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Margin | `0` | Anger att bredden beräknas i förhållande till avståndet mellan vänster och höger marginal. |
| Page | `1` | Anger att bredden beräknas relativt till sidans bredd. |
| LeftMargin | `2` | Anger att bredden beräknas relativt till vänstermarginalens storlek. |
| RightMargin | `3` | Anger att bredden beräknas relativt till högermarginalens storlek. |
| InnerMargin | `4` | Anger att bredden beräknas i förhållande till den inre marginalytans storlek, till den vänstra marginalytans storlek för udda sidor och till den högra marginalytans storlek för jämna sidor. |
| OuterMargin | `5` | Anger att bredden beräknas i förhållande till den yttre marginalytans storlek, i förhållande till den högra marginalytans storlek för udda sidor och i förhållande till den vänstra marginalytans storlek för jämna sidor. |
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

* property [RelativeHorizontalSize](../shapebase/relativehorizontalsize/)
* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
