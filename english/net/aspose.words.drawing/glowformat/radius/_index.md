---
title: GlowFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words for .NET
description: Discover the GlowFormat Radius property to customize your glow effects. Adjust the radius in points for stunning visual enhancements. Default: 0.0.
type: docs
weight: 20
url: /net/aspose.words.drawing/glowformat/radius/
---
## GlowFormat.Radius property

Gets or sets a double value that represents the length of the radius for a glow effect in points (pt). The default value is 0.0.

```csharp
public double Radius { get; set; }
```

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

* class [GlowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
