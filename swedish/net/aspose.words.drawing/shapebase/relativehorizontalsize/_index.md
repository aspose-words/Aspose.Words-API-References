---
title: ShapeBase.RelativeHorizontalSize
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase RelativeHorizontalSize för att enkelt justera formstorlekar horisontellt för ökad designflexibilitet och precision.
type: docs
weight: 460
url: /sv/net/aspose.words.drawing/shapebase/relativehorizontalsize/
---
## ShapeBase.RelativeHorizontalSize property

Hämtar eller ställer in värdet för formens relativa storlek i horisontell riktning.

```csharp
public RelativeHorizontalSize RelativeHorizontalSize { get; set; }
```

## Anmärkningar

Standardvärdet är[`RelativeHorizontalSize`](../../relativehorizontalsize/).

Har endast effekt om[`WidthRelative`](../widthrelative/) är inställd.

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

* enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
