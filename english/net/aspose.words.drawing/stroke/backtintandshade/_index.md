---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words for .NET
description: Stroke BackTintAndShade property. Gets or sets a double value that lightens or darkens the stroke background color in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Gets or sets a double value that lightens or darkens the stroke background color.

```csharp
public double BackTintAndShade { get; set; }
```

## Remarks

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in ArgumentOutOfRangeException.

## Examples

Shows how to set back theme color and tint and shade.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### See Also

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
