---
title: ShapeBase.Glow
linktitle: Glow
articleTitle: Glow
second_title: Aspose.Words for .NET
description: Enhance your designs with ShapeBase Glow! Achieve stunning glow effects for your shapes and elevate your visual projects effortlessly.
type: docs
weight: 200
url: /net/aspose.words.drawing/shapebase/glow/
---
## ShapeBase.Glow property

Gets glow formatting for the shape.

```csharp
public GlowFormat Glow { get; }
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

* class [GlowFormat](../../glowformat/)
* class [ShapeBase](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
