---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: AdjustmentCollection Öğesi özelliğini keşfedin, kesintisiz veri yönetimi ve gelişmiş performans için ayarlamaları dizine göre zahmetsizce alın.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

Belirtilen dizinde bir ayarlama döndürür.

```csharp
public Adjustment this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyonun indeksi. |

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

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
