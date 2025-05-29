---
title: Adjustment.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية قيمة التعديل، واحصل بسهولة على قيم التعديل الخام أو قم بتعيينها لتحسين إدارة البيانات وتبسيط العمليات لديك.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/adjustment/value/
---
## Adjustment.Value property

يحصل على القيمة الخام للتعديل أو يعينها.

```csharp
public int Value { get; set; }
```

## ملاحظات

قيمة التعديل هي ببساطة دليل يحتوي على صيغة محددة تعتمد على القيمة. وهذا يعني أنه لا يتم إجراء أي حساب لدليل قيمة التعديل. بدلاً من ذلك، يحدد هذا الدليل قيمة معلمة تُستخدم في الحسابات داخل أدلة الشكل.

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

* class [Adjustment](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
