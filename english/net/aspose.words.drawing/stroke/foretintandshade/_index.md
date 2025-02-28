---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words for .NET
description: Adjust the Stroke ForeTintAndShade property to effortlessly lighten or darken your stroke's foreground color for enhanced visual impact.
type: docs
weight: 150
url: /net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Gets or sets a double value that lightens or darkens the stroke foreground color.

```csharp
public double ForeTintAndShade { get; set; }
```

## Remarks

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in ArgumentOutOfRangeException.

## Examples

Shows how to set fore theme color and tint and shade.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### See Also

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
