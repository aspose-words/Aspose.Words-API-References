---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase ParentParagraph—يمكنك الوصول بكفاءة إلى الفقرة الأصلية المباشرة لإدارة المحتوى بشكل مبسط وتحسين التنظيم.
type: docs
weight: 430
url: /ar/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

إرجاع الفقرة الأصلية المباشرة.

```csharp
public Paragraph ParentParagraph { get; }
```

## ملاحظات

بالنسبة للأشكال الفرعية لشكل المجموعة والأشكال الفرعية لكائن Office Math، يتم إرجاعها دائمًا`باطل`.

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
