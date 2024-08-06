---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.GlowFormat class. Represents the glow formatting for an object in C#.
type: docs
weight: 1140
url: /net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Represents the glow formatting for an object.

```csharp
public class GlowFormat
```

## Properties

| Name | Description |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Gets or sets a Color object that represents the color for a glow effect. The default value is Black. |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Gets or sets a double value that represents the length of the radius for a glow effect in points (pt). The default value is 0.0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0. |

## Methods

| Name | Description |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Removes `GlowFormat` from the parent object. |

## Remarks

Use the [`Glow`](../shapebase/glow/) property to access glow properties of an object. You do not create instances of the `GlowFormat` class directly.

## Examples

Shows how to interact with glow shape effect.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
