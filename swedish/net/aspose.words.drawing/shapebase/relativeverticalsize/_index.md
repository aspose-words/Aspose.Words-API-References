---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase RelativeVerticalSize för att enkelt justera formers vertikala dimensioner för ökad designflexibilitet och precision.
type: docs
weight: 480
url: /sv/net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

Hämtar eller ställer in värdet för formens relativa storlek i vertikal riktning.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## Anmärkningar

Standardvärdet ärMargin.

Har endast effekt om[`HeightRelative`](../heightrelative/) är inställd.

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

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
