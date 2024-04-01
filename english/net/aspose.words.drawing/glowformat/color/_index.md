---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: GlowFormat Color property. Gets or sets a Color object that represents the color for a glow effect. The default value is Black in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Gets or sets a Color object that represents the color for a glow effect. The default value is Black.

```csharp
public Color Color { get; set; }
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
