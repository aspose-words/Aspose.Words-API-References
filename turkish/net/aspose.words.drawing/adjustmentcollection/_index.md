---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: .NET için Aspose.Words
description: Aspose.Words.Drawing.AdjustmentCollection sınıfını keşfedin; şekiller için salt okunur ayar değerlerini yönetme çözümünüz. Belge tasarımlarınızı zahmetsizce geliştirin!
type: docs
weight: 710
url: /tr/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

Salt okunur bir koleksiyonu temsil eder[`Adjustment`](../adjustment/) belirtilen şekle uygulanan değerleri ayarlayın.

```csharp
public class AdjustmentCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | Belirtilen dizinde bir ayarlama döndürür. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
