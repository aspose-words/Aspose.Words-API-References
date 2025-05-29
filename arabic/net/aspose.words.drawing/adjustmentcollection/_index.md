---
title: AdjustmentCollection Class
linktitle: AdjustmentCollection
articleTitle: AdjustmentCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.AdjustmentCollection، الحل الأمثل لإدارة قيم تعديلات القراءة فقط للأشكال. حسّن تصميمات مستنداتك بسهولة!
type: docs
weight: 710
url: /ar/net/aspose.words.drawing/adjustmentcollection/
---
## AdjustmentCollection class

يمثل مجموعة للقراءة فقط من[`Adjustment`](../adjustment/) ضبط القيم المطبقة على الشكل المحدد.

```csharp
public class AdjustmentCollection
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.drawing/adjustmentcollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.drawing/adjustmentcollection/item/) { get; } | يعيد تعديلًا عند الفهرس المحدد. |

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
