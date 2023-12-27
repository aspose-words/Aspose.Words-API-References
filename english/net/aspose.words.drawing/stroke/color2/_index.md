---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words for .NET
description: Stroke Color2 property. Defines a second color for a stroke in C#.
type: docs
weight: 60
url: /net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Defines a second color for a stroke.

```csharp
public Color Color2 { get; set; }
```

## Remarks

The default value for a [`Shape`](../../shape/) is White.

## Examples

Shows how to process shape stroke features.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
// Strokes with a single color do not use the Color2 property.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### See Also

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
