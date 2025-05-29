---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: .NET için Aspose.Words
description: Şekil Ayarlamalarını Keşfedin. Hassas şekil değişiklikleri için ham değerlere erişin. En iyi sonuçlar için tasarımları özel ayarlamalarla kolayca geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

Bir şeklin ayar ham değerlerine erişim sağlar. Herhangi bir ayar ham değeri içermeyen bir şekil için boş bir koleksiyon döndürür.

```csharp
public AdjustmentCollection Adjustments { get; }
```

## Örnekler

Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rounded rectangle shape.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

AdjustmentCollection adjustments = shape.Adjustments;
Assert.AreEqual(1, adjustments.Count);

Adjustment adjustment = adjustments[0];
Assert.AreEqual("adj", adjustment.Name);
Assert.AreEqual(16667, adjustment.Value);

adjustment.Value = 30000;

doc.Save(ArtifactsDir + "Shape.Adjustments.docx");
```

### Ayrıca bakınız

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
