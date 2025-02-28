---
title: Fill.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words for .NET
description: Discover how to set the ForeThemeColor property to customize your design with vibrant fill colors. Enhance your project’s visual appeal effortlessly!
type: docs
weight: 80
url: /net/aspose.words.drawing/fill/forethemecolor/
---
## Fill.ForeThemeColor property

Gets or sets a ThemeColor object that represents the foreground color for the fill.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
