---
title: AdjustmentCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية AdjustmentCollection Item، واسترد التعديلات بسهولة حسب الفهرس لإدارة البيانات بسلاسة وتحسين الأداء.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/adjustmentcollection/item/
---
## AdjustmentCollection indexer

يعيد تعديلًا عند الفهرس المحدد.

```csharp
public Adjustment this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للمجموعة. |

## أمثلة

يوضح كيفية العمل مع قيم التعديل الخام.

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

### أنظر أيضا

* class [Adjustment](../../adjustment/)
* class [AdjustmentCollection](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
