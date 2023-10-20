---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words لـ .NET
description: TextBox VerticalAnchor ملكية. يحدد المحاذاة الرأسية للنص داخل الشكل في C#.
type: docs
weight: 120
url: /ar/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

يحدد المحاذاة الرأسية للنص داخل الشكل.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## ملاحظات

القيمة الافتراضية هيTop.

## أمثلة

يوضح كيفية محاذاة محتويات النص في مربع النص عموديًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Top" إلى
// قم بمحاذاة النص الموجود في مربع النص هذا مع الجانب العلوي من الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Middle" إلى
// قم بمحاذاة النص الموجود في مربع النص هذا إلى منتصف الشكل.
// قم بتعيين خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" إلى
// قم بمحاذاة النص الموجود في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// المحاذاة الرأسية للنص داخل مربعات النص متاحة بدءًا من Microsoft Word 2007 وما بعده.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### أنظر أيضا

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
