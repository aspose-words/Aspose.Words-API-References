---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية TextBox VerticalAnchor على تعزيز محاذاة النص داخل الأشكال لتحسين التصميم وسهولة القراءة في مشاريعك.
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

// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Top" لـ
// قم بمحاذاة النص الموجود في مربع النص هذا مع الجانب العلوي للشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Middle"
// محاذاة النص في مربع النص هذا إلى مركز الشكل.
// اضبط خاصية "VerticalAnchor" على "TextBoxAnchor.Bottom" لـ
// قم بمحاذاة النص الموجود في مربع النص هذا إلى أسفل الشكل.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// أصبحت المحاذاة الرأسية للنص داخل مربعات النص متاحة من Microsoft Word 2007 فصاعدًا.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### أنظر أيضا

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
