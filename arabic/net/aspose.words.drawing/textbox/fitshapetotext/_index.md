---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم خاصية FitShapeToText في Microsoft Word بتعديل الأشكال تلقائيًا لتناسب النص بشكل مثالي، مما يعزز عرض المستند.
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

يوضح كيفية تغيير حجم مربع النص ليتناسب مع محتوياته بشكل محكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// قم بتطبيق هذه القيم على كلا هذين العنصرين للحصول على الشكل الرئيسي المناسب
// بإحكام حول محتويات النص، متجاهلاً الأبعاد التي حددناها.
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
