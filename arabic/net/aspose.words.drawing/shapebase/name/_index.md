---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase Name لإدارة أسماء الأشكال الاختيارية بسهولة، مما يعزز مرونة التصميم وتنظيم المشروع.
type: docs
weight: 420
url: /ar/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

يحصل على اسم الشكل الاختياري أو يعينه.

```csharp
public string Name { get; set; }
```

## ملاحظات

افتراضيًا، السلسلة فارغة.

لا يمكن أن يكون`باطل`، ولكن يمكن أن تكون سلسلة فارغة.

## أمثلة

يوضح كيفية استخدام النص البديل للشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// يمكننا الوصول إلى النص البديل للشكل عن طريق النقر بزر الماوس الأيمن فوقه، ثم عبر "تنسيق الشكل التلقائي" -> "نص بديل".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// احفظ المستند بصيغة HTML، ثم احذف الصورة المرتبطة التي تنتمي إلى شكلنا.
// سيعرض المتصفح الذي يقرأ HTML نصًا بديلًا بدلاً من الصورة المفقودة.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
