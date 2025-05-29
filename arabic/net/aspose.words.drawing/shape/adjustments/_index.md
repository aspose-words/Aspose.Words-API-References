---
title: Shape.Adjustments
linktitle: Adjustments
articleTitle: Adjustments
second_title: Aspose.Words لـ .NET
description: اكتشف تعديلات الأشكال. احصل على قيم خام لتعديلات دقيقة للأشكال. حسّن تصاميمك بسهولة باستخدام تعديلات مُخصصة لتحقيق أفضل النتائج.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/shape/adjustments/
---
## Shape.Adjustments property

يوفر الوصول إلى قيم التعديل الخام لشكل ما. بالنسبة للشكل الذي لا يحتوي على أي قيم تعديل خام، فإنه يعيد مجموعة فارغة.

```csharp
public AdjustmentCollection Adjustments { get; }
```

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

* class [AdjustmentCollection](../../adjustmentcollection/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
