---
title: GlowFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words för .NET
description: Upptäck egenskapen GlowFormat Radius för att anpassa dina glödeffekter. Justera radien i punkter för fantastiska visuella förbättringar. Standardvärde 0,0.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing/glowformat/radius/
---
## GlowFormat.Radius property

Hämtar eller ställer in ett dubbelvärde som representerar längden på radien för en glödeffekt i punkter (pt). Standardvärdet är 0,0.

```csharp
public double Radius { get; set; }
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
