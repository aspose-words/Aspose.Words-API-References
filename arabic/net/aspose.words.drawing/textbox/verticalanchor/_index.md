---
title: TextBox.VerticalAnchor
second_title: Aspose.Words لمراجع .NET API
description: TextBox ملكية. يحدد المحاذاة الرأسية للنص داخل الشكل.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

يحدد المحاذاة الرأسية للنص داخل الشكل.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

### ملاحظات

النظام الأساسيTop.

### أمثلة

يوضح كيفية محاذاة محتويات النص لمربع نص عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Top" إلى
// محاذاة النص في مربع النص هذا مع الجانب العلوي للشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Middle" على
// محاذاة النص في مربع النص هذا إلى وسط الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" إلى
// محاذاة النص في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// المحاذاة الرأسية للنص داخل مربعات النص متاحة من Microsoft Word 2007 وما بعده.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### أنظر أيضا

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../textbox/)
* المجسم [Aspose.Words](../../../)


