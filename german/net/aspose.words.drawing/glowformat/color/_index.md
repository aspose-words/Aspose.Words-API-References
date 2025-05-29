---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Entdecken Sie die GlowFormat-Farbeigenschaft, um Ihre Leuchteffekte anzupassen. Stellen Sie einfach leuchtende Farben für eine beeindruckende visuelle Wirkung ein. Standard ist Schwarz.
type: docs
weight: 10
url: /de/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Ruft ab oder setzt einenColor Objekt, das die Farbe für einen Leuchteffekt darstellt. Der Standardwert istBlack .

```csharp
public Color Color { get; set; }
```

## Beispiele

Zeigt, wie mit dem Leuchtformeffekt interagiert wird.

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

### Siehe auch

* class [GlowFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
