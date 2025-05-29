---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextBox WrapMode لتحسين التفاف النص داخل الأشكال، مما يؤدي إلى تحسين وضوح تصميمك وجاذبيته البصرية.
type: docs
weight: 110
url: /ar/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

يحدد كيفية التفاف النص داخل الشكل.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيSquare.

## أمثلة

يوضح كيفية تعيين وضع الالتفاف لمحتويات مربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// اضبط خاصية "TextBoxWrapMode" على "TextBoxWrapMode.None" لزيادة عرض مربع النص
// لاستيعاب النص، إذا كان كبيرًا بدرجة كافية.
// اضبط خاصية "TextBoxWrapMode" إلى "TextBoxWrapMode.Square"
// لف كل النص داخل مربع النص، مع الحفاظ على أبعاده.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### أنظر أيضا

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
