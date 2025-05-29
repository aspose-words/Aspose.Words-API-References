---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: .NET için Aspose.Words
description: GlowFormat'ın Şeffaflık özelliğini keşfedin, çarpıcı görsel etki için parıltı efektlerini opak ile şeffaf arasında (0,0 ila 1,0) kolayca ayarlayın. Varsayılan, 0,0.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Parıltı efekti için şeffaflık derecesini 0,0 (opak) ile 1,0 (temiz) arasında bir değer olarak alır veya ayarlar. Varsayılan değer 0,0'dır.

```csharp
public double Transparency { get; set; }
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
