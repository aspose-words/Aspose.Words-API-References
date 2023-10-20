---
title: ShapeBase.LeftRelative
linktitle: LeftRelative
articleTitle: LeftRelative
second_title: Aspose.Words för .NET
description: ShapeBase LeftRelative fast egendom. Hämtar eller ställer in värdet som representerar formens relativa vänstra position i procent i C#.
type: docs
weight: 380
url: /sv/net/aspose.words.drawing/shapebase/leftrelative/
---
## ShapeBase.LeftRelative property

Hämtar eller ställer in värdet som representerar formens relativa vänstra position i procent.

```csharp
public float LeftRelative { get; set; }
```

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

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
