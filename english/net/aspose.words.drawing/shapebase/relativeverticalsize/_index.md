---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words for .NET
description: Discover the ShapeBase RelativeVerticalSize property to easily adjust shapes' vertical dimensions for enhanced design flexibility and precision.
type: docs
weight: 480
url: /net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

Gets or sets the value of shape's relative size in vertical direction.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## Remarks

The default value is Margin.

Has effect only if [`HeightRelative`](../heightrelative/) is set.

## Examples

Shows how to set relative size and position.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adding a simple shape with absolute size and position.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
shape.WrapType = WrapType.None;

// Checking and setting the relative horizontal size.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Setting the horizontal size binding to Margin.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Setting the width to 50% of Margin width.
    shape.WidthRelative = 50;
}

// Checking and setting the relative vertical size.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Setting the vertical size binding to Margin.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Setting the heigh to 30% of Margin height.
    shape.HeightRelative = 30;
}

// Checking and setting the relative vertical position.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // etting the position binding to TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Setting relative Top to 30% of TopMargin position.
    shape.TopRelative = 30;
}

// Checking and setting the relative horizontal position.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Setting the position binding to RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // The position relative value can be negative.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### See Also

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
