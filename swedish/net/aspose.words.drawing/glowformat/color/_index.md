---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GlowFormat Color för att anpassa dina glödeffekter. Ställ enkelt in livfulla färger för en fantastisk visuell effekt. Standardinställningen är svart.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Hämtar eller ställer in enColor objekt som representerar färgen för en glödeffekt. Standardvärdet ärBlack .

```csharp
public Color Color { get; set; }
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

* class [GlowFormat](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
