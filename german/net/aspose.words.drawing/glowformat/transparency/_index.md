---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words für .NET
description: Entdecken Sie die Transparenzeigenschaft von GlowFormat und passen Sie Leuchteffekte einfach von undurchsichtig bis transparent (0,0 bis 1,0) an, um eine beeindruckende visuelle Wirkung zu erzielen. Standard: 0,0.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Ruft den Transparenzgrad für den Leuchteffekt als Wert zwischen 0,0 (undurchsichtig) und 1,0 (transparent) ab oder legt ihn fest. Der Standardwert ist 0,0.

```csharp
public double Transparency { get; set; }
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
