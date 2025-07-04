---
title: GlowFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words for .NET
description: Effortlessly remove GlowFormat from your parent object with our efficient GlowFormat Remove method. Enhance your design workflow today!
type: docs
weight: 40
url: /net/aspose.words.drawing/glowformat/remove/
---
## GlowFormat.Remove method

Removes [`GlowFormat`](../) from the parent object.

```csharp
public void Remove()
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
