---
title: Enum TextBoxWrapMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.TextBoxWrapMode تعداد. يحدد كيفية التفاف النص داخل الشكل.
type: docs
weight: 1340
url: /ar/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

يحدد كيفية التفاف النص داخل الشكل.

```csharp
public enum TextBoxWrapMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Square | `0` | يلتف النص داخل الشكل. |
| None | `2` | عدم التفاف النص داخل الشكل. |

### أمثلة

يوضح كيفية تعيين وضع الالتفاف لمحتويات مربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// قم بتعيين خاصية "TextBoxWrapMode" على "TextBoxWrapMode.None" لزيادة عرض مربع النص
// لاستيعاب النص، إذا كان كبيرًا بدرجة كافية.
// قم بتعيين خاصية "TextBoxWrapMode" على "TextBoxWrapMode.Square" إلى
// لف النص بالكامل داخل مربع النص، مع الحفاظ على أبعاده.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


