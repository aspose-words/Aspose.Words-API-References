---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase AlternativeText، التي تعمل على تعزيز إمكانية الوصول من خلال توفير نص وصفي للرسومات، وتحسين تجربة المستخدم وتحسين محركات البحث.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

يحدد نصًا بديلًا ليتم عرضه بدلاً من الرسم البياني.

```csharp
public string AlternativeText { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

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
