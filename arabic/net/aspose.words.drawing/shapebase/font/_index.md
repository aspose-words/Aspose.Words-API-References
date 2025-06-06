---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase Font لسهولة الوصول إلى تنسيق الخطوط. حسّن تصميماتك بأنماط نص قابلة للتخصيص وخيارات طباعة فريدة.
type: docs
weight: 190
url: /ar/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

يوفر الوصول إلى تنسيق الخط لهذا الكائن.

```csharp
public Font Font { get; }
```

## أمثلة

يوضح كيفية إدراج مربع نص، وتعيين الخط الخاص بمحتوياته.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// اضبط خاصية "مخفي" لكائن "الخط" الخاص بالشكل على "صحيح" لإخفاء مربع النص عن الأنظار
// وانهيار المساحة التي من شأنها أن تشغلها عادة.
// قم بضبط خاصية "مخفي" لكائن "الخط" الخاص بالشكل إلى "خطأ" لترك مربع النص مرئيًا.
shape.Font.Hidden = hideShape;

// إذا كان الشكل مرئيًا، فسوف نقوم بتعديل مظهره عبر كائن الخط.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// نقل المنشئ خارج مربع النص إلى المستند الرئيسي.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### أنظر أيضا

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
