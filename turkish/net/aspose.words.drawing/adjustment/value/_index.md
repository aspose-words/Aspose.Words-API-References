---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: .NET için Aspose.Words
description: Ayarlama Değeri özelliğini keşfedin, veri yönetiminizi geliştirmek ve süreçlerinizi hızlandırmak için ham ayarlama değerlerini kolayca alın veya ayarlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

Ayarlamanın ham değerini alır veya ayarlar.

```csharp
public int Value { get; set; }
```

## Notlar

Bir ayar değeri, basitçe, değer tabanlı bir formül belirtilmiş bir kılavuzdur. Yani, bir ayar değeri kılavuzu için hiçbir hesaplama yapılmaz. Bunun yerine, bu kılavuz, şekil kılavuzları içindeki hesaplamalar için kullanılan bir parametre değerini belirtir.

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

* class [Adjustment](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
