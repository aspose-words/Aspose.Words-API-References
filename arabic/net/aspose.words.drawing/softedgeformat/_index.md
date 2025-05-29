---
title: SoftEdgeFormat Class
linktitle: SoftEdgeFormat
articleTitle: SoftEdgeFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.SoftEdgeFormat لتحسين مستنداتك بتأثيرات حافة ناعمة مذهلة للحصول على مظهر احترافي.
type: docs
weight: 1710
url: /ar/net/aspose.words.drawing/softedgeformat/
---
## SoftEdgeFormat class

يمثل تنسيق الحافة الناعمة لكائن ما.

```csharp
public class SoftEdgeFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Radius](../../aspose.words.drawing/softedgeformat/radius/) { get; set; } | يحصل على أو يعين قيمة مزدوجة تمثل طول نصف القطر لتأثير الحافة الناعمة بالنقاط (pt). القيمة الافتراضية هي 0.0. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Remove](../../aspose.words.drawing/softedgeformat/remove/)() | يزيل`SoftEdgeFormat` من الكائن الرئيسي. |

## ملاحظات

استخدم[`SoftEdge`](../shapebase/softedge/) الخاصية للوصول إلى خصائص الحافة الناعمة لكائن ما. لا تقم بإنشاء مثيلات من`SoftEdgeFormat` الصف مباشرة.

## أمثلة

يوضح كيفية العمل مع تنسيق الحافة الناعمة.

```csharp
DocumentBuilder builder = new DocumentBuilder();
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 200);

// قم بتطبيق حافة ناعمة على الشكل.
shape.SoftEdge.Radius = 30;

builder.Document.Save(ArtifactsDir + "Shape.SoftEdge.docx");

// قم بتحميل المستند على شكل مستطيل ذو حافة ناعمة.
Document doc = new Document(ArtifactsDir + "Shape.SoftEdge.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
SoftEdgeFormat softEdgeFormat = shape.SoftEdge;

//تحقق من نصف قطر الحافة الناعمة.
Assert.AreEqual(30, softEdgeFormat.Radius);

// قم بإزالة الحافة الناعمة من الشكل.
softEdgeFormat.Remove();

//تحقق من نصف قطر الحافة الناعمة التي تمت إزالتها.
Assert.AreEqual(0, softEdgeFormat.Radius);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
