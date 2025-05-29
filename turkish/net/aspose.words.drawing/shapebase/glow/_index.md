---
title: ShapeBase.Glow
linktitle: Glow
articleTitle: Glow
second_title: .NET için Aspose.Words
description: ShapeBase Glow ile tasarımlarınızı geliştirin! Şekilleriniz için çarpıcı parıltı efektleri elde edin ve görsel projelerinizi zahmetsizce bir üst seviyeye taşıyın.
type: docs
weight: 200
url: /tr/net/aspose.words.drawing/shapebase/glow/
---
## ShapeBase.Glow property

Şekil için parıltı biçimlendirmesini alır.

```csharp
public GlowFormat Glow { get; }
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

* class [GlowFormat](../../glowformat/)
* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
