---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words for .NET
description: Discover GlowFormat's Transparency property, easily adjust glow effects from opaque to clear (0.0 to 1.0) for stunning visual impact. Default, 0.0.
type: docs
weight: 30
url: /net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Gets or sets the degree of transparency for the glow effect as a value between 0.0 (opaque) and 1.0 (clear). The default value is 0.0.

```csharp
public double Transparency { get; set; }
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

Assert.That(shape.Glow.Color.ToArgb(), Is.EqualTo(Color.FromArgb(217, 250, 128, 114).ToArgb()));
Assert.That(shape.Glow.Radius, Is.EqualTo(30));
Assert.That(shape.Glow.Transparency, Is.EqualTo(0.15d).Within(0.01d));

shape.Glow.Remove();

Assert.That(shape.Glow.Color.ToArgb(), Is.EqualTo(Color.Black.ToArgb()));
Assert.That(shape.Glow.Radius, Is.EqualTo(0));
Assert.That(shape.Glow.Transparency, Is.EqualTo(0));
```

### See Also

* class [GlowFormat](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
