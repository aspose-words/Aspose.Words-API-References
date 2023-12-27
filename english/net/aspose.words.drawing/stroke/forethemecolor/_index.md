---
title: Stroke.ForeThemeColor
linktitle: ForeThemeColor
articleTitle: ForeThemeColor
second_title: Aspose.Words for .NET
description: Stroke ForeThemeColor property. Gets or sets a ThemeColor object that represents the stroke foreground color in C#.
type: docs
weight: 140
url: /net/aspose.words.drawing/stroke/forethemecolor/
---
## Stroke.ForeThemeColor property

Gets or sets a ThemeColor object that represents the stroke foreground color.

```csharp
public ThemeColor ForeThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
