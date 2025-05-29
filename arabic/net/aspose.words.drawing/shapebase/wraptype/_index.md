---
title: ShapeBase.WrapType
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase WrapType، وتحكم في الأشكال المضمنة أو العائمة وقم بتخصيص التفاف النص لتحسين مرونة التخطيط.
type: docs
weight: 640
url: /ar/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

يُحدد ما إذا كان الشكل مضمنًا أم عائمًا. بالنسبة للأشكال العائمة، يُحدد وضع التفاف النص حول الشكل.

```csharp
public WrapType WrapType { get; set; }
```

## ملاحظات

القيمة الافتراضية هيNone.

له تأثير فقط على الأشكال ذات المستوى الأعلى.

## أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع مركز الصفحة.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

يوضح كيفية إنشاء مربع نص وتنسيقه.

```csharp
Document doc = new Document();

// إنشاء مربع نص عائم.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// تعيين المحاذاة الأفقية والرأسية للنص داخل الشكل.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

//أضف فقرة إلى مربع النص وأضف سلسلة من النص الذي سيعرضه مربع النص.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### أنظر أيضا

* enum [WrapType](../../wraptype/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
