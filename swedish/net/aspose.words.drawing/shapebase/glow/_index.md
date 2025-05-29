---
title: ShapeBase.Glow
linktitle: Glow
articleTitle: Glow
second_title: Aspose.Words för .NET
description: Förbättra dina designer med ShapeBase Glow! Få fantastiska glödeffekter för dina former och lyft dina visuella projekt utan ansträngning.
type: docs
weight: 200
url: /sv/net/aspose.words.drawing/shapebase/glow/
---
## ShapeBase.Glow property

Hämtar glödformatering för formen.

```csharp
public GlowFormat Glow { get; }
```

## Exempel

Visar hur man interagerar med glödformseffekten.

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

### Se även

* class [GlowFormat](../../glowformat/)
* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
