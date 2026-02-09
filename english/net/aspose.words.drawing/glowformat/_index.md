---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words for .NET
description: Explore Aspose.Words.Drawing.GlowFormat class to enhance your documents with stunning glow effects. Elevate your design with unique formatting options!
type: docs
weight: 1300
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

Assert.That(shape.Glow.Color.ToArgb(), Is.EqualTo(Color.FromArgb(217, 250, 128, 114).ToArgb()));
Assert.That(shape.Glow.Radius, Is.EqualTo(30));
Assert.That(shape.Glow.Transparency, Is.EqualTo(0.15d).Within(0.01d));

shape.Glow.Remove();

Assert.That(shape.Glow.Color.ToArgb(), Is.EqualTo(Color.Black.ToArgb()));
Assert.That(shape.Glow.Radius, Is.EqualTo(0));
Assert.That(shape.Glow.Transparency, Is.EqualTo(0));
```

### See Also

* namespace [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assembly [Aspose.Words](../../)
