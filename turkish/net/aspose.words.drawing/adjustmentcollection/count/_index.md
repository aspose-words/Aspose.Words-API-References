---
title: AdjustmentCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Toplam öğe sayısını kolayca almak ve veri yönetimi verimliliğinizi artırmak için AdjustmentCollection Count özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/adjustmentcollection/count/
---
## AdjustmentCollection.Count property

Koleksiyonda bulunan öğelerin sayısını alır.

```csharp
public int Count { get; }
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

* class [AdjustmentCollection](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
