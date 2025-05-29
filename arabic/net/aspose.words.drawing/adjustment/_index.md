---
title: Adjustment Class
linktitle: Adjustment
articleTitle: Adjustment
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Adjustment، المصممة لتحسين أشكالك بقيم تعديل دقيقة لتنسيق المستندات بشكل متفوق.
type: docs
weight: 700
url: /ar/net/aspose.words.drawing/adjustment/
---
## Adjustment class

يمثل قيم التعديل المطبقة على الشكل المحدد.

```csharp
public class Adjustment
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Name](../../aspose.words.drawing/adjustment/name/) { get; } | يحصل على اسم التعديل. |
| [Value](../../aspose.words.drawing/adjustment/value/) { get; set; } | يحصل على القيمة الخام للتعديل أو يعينها. |

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
