---
title: ShapeBase.Font
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يوفر الوصول إلى تنسيق خط هذا الكائن.
type: docs
weight: 190
url: /ar/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

يوفر الوصول إلى تنسيق خط هذا الكائن.

```csharp
public Font Font { get; }
```

### أمثلة

يوضح كيفية إدراج مربع نص ، وتعيين خط محتوياته.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// قم بتعيين الخاصية "Hidden" لكائن "Font" للشكل على "true" لإخفاء مربع النص عن الأنظار
// وخفض المساحة التي تشغلها عادةً.
// قم بتعيين الخاصية "Hidden" لكائن "Font" للشكل على "false" لترك مربع النص مرئيًا.
shape.Font.Hidden = hideShape;

// إذا كان الشكل مرئيًا ، فسنقوم بتعديل مظهره عبر كائن الخط.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// انقل المنشئ خارج مربع النص إلى المستند الرئيسي.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### أنظر أيضا

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


