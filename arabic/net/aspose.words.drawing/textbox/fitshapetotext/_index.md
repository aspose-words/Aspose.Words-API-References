---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words لـ .NET
description: TextBox FitShapeToText ملكية. يحدد ما إذا كان Microsoft Word سيقوم بتكبير الشكل ليناسب النص في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

يحدد ما إذا كان Microsoft Word سيقوم بتكبير الشكل ليناسب النص.

```csharp
public bool FitShapeToText { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية جعل مربع النص يغير حجمه ليناسب محتوياته بإحكام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// قم بتطبيق هذه القيم على هذين العضوين للحصول على الشكل الأصلي المناسب
// يحيط بإحكام بمحتويات النص، متجاهلاً الأبعاد التي وضعناها.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### أنظر أيضا

* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
