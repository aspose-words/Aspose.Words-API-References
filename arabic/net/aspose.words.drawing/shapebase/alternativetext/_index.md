---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words لـ .NET
description: ShapeBase AlternativeText ملكية. تحديد النص البديل الذي سيتم عرضه بدلاً من الرسم في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

تحديد النص البديل الذي سيتم عرضه بدلاً من الرسم.

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

// يمكننا الوصول إلى النص البديل للشكل عن طريق النقر بزر الماوس الأيمن عليه، ثم عبر "تنسيق الشكل التلقائي" -> "نص بديل".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// احفظ المستند بتنسيق HTML، ثم احذف الصورة المرتبطة التي تنتمي إلى الشكل الخاص بنا.
// سيعرض المتصفح الذي يقرأ HTML النص البديل بدلاً من الصورة المفقودة.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
