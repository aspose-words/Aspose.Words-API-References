---
title: ShapeBase.Name
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على اسم الشكل الاختياري أو تعيينه.
type: docs
weight: 380
url: /ar/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

الحصول على اسم الشكل الاختياري أو تعيينه.

```csharp
public string Name { get; set; }
```

### ملاحظات

الافتراضي هو سلسلة فارغة.

لا يمكن أن يكون فارغًا ، لكن يمكن أن يكون سلسلة فارغة.

### أمثلة

يوضح كيفية استخدام النص البديل للشكل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// يمكننا الوصول إلى النص البديل للشكل بالنقر بزر الماوس الأيمن فوقه ، ثم عبر "تنسيق الشكل التلقائي" - >; "نص بديل".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// احفظ المستند إلى HTML ، ثم احذف الصورة المرتبطة التي تنتمي إلى شكلنا.
// سيعرض المتصفح الذي يقرأ HTML الخاص بنا النص البديل بدلاً من الصورة المفقودة.
doc.Save(ArtifactsDir + "Shape.AltText.html");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


