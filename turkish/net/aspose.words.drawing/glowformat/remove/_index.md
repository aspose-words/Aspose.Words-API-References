---
title: GlowFormat.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Verimli GlowFormat Kaldırma yöntemimizle GlowFormat'ı ana nesnenizden zahmetsizce kaldırın. Tasarım iş akışınızı bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/glowformat/remove/
---
## GlowFormat.Remove method

Kaldırır[`GlowFormat`](../) ana nesneden.

```csharp
public void Remove()
```

## Örnekler

Parıltılı şekil efektiyle nasıl etkileşim kurulacağını gösterir.

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

### Ayrıca bakınız

* class [GlowFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
