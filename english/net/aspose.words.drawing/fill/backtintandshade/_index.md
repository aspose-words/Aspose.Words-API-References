---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
second_title: Aspose.Words for .NET API Reference
description: Fill property. Gets or sets a double value that lightens or darkens the background color in C#.
type: docs
weight: 30
url: /net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Gets or sets a double value that lightens or darkens the background color.

```csharp
public double BackTintAndShade { get; set; }
```

## Remarks

The allowed values are within the range from -1 (the darkest) to 1 (the lightest) for this property. Zero (0) is neutral. Attempting to set this property to a value less than -1 or more than 1 results in ArgumentOutOfRangeException.

## Examples

Shows how to set theme color for foreground/background shape color.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Note: do not use "BackThemeColor" and "BackTintAndShade" for font fill.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../fill/)
* assembly [Aspose.Words](../../../)
