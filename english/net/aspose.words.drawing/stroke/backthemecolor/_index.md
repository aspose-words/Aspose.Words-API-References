---
title: Stroke.BackThemeColor
linktitle: BackThemeColor
articleTitle: BackThemeColor
second_title: Aspose.Words for .NET
description: Stroke BackThemeColor property. Gets or sets a ThemeColor object that represents the stroke background color in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing/stroke/backthemecolor/
---
## Stroke.BackThemeColor property

Gets or sets a ThemeColor object that represents the stroke background color.

```csharp
public ThemeColor BackThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
