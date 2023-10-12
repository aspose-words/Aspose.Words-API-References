---
title: ShapeBase.ParentParagraph
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاع الفقرة الأصلية المباشرة.
type: docs
weight: 410
url: /ar/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

إرجاع الفقرة الأصلية المباشرة.

```csharp
public Paragraph ParentParagraph { get; }
```

### ملاحظات

بالنسبة للأشكال التابعة لشكل المجموعة والأشكال الفرعية لكائن Office Math، يتم إرجاعها دائمًا`باطل`.

### أمثلة

يوضح كيفية إدراج مربع نص وتعيين خط محتوياته.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// قم بتعيين الخاصية "مخفي" لكائن "الخط" الخاص بالشكل على "صحيح" لإخفاء مربع النص عن الأنظار
// وقم بطي المساحة التي كانت تشغلها عادةً.
// قم بتعيين الخاصية "مخفي" لكائن "الخط" الخاص بالشكل على "خطأ" لترك مربع النص مرئيًا.
shape.Font.Hidden = hideShape;

// إذا كان الشكل مرئيًا، فسنقوم بتعديل مظهره عبر كائن الخط.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// انقل المنشئ خارج مربع النص مرة أخرى إلى المستند الرئيسي.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### أنظر أيضا

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


