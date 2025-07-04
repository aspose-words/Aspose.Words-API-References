---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words for .NET
description: Discover how to use the ImageBytes property to create stunning stroke images and unique pattern fills for your designs. Enhance your visuals today!
type: docs
weight: 160
url: /net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Defines the image for a stroke image or pattern fill.

```csharp
public byte[] ImageBytes { get; }
```

## Examples

Shows how to process shape stroke features.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Strokes can have two colors, which are used to create a pattern defined by two-tone image data.
// Strokes with a single color do not use the Color2 property.
Assert.That(stroke.Color, Is.EqualTo(Color.FromArgb(255, 128, 0, 0)));
Assert.That(stroke.Color2, Is.EqualTo(Color.FromArgb(255, 255, 255, 0)));

Assert.That(stroke.ImageBytes, Is.Not.Null);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### See Also

* class [Stroke](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
