---
title: ShapeBase.WrapType
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد ما إذا كان الشكل سطريًا أم عائمًا. للأشكال العائمة يحدد وضع الالتفاف للنص حول الشكل.
type: docs
weight: 600
url: /ar/net/aspose.words.drawing/shapebase/wraptype/
---
## ShapeBase.WrapType property

يحدد ما إذا كان الشكل سطريًا أم عائمًا. للأشكال العائمة يحدد وضع الالتفاف للنص حول الشكل.

```csharp
public WrapType WrapType { get; set; }
```

### ملاحظات

القيمة الافتراضية هيNone.

له تأثير فقط على أشكال المستوى الأعلى.

### أمثلة

يوضح كيفية إدراج صورة عائمة في وسط الصفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل صورة عائمة ستظهر خلف النص المتداخل وقم بمحاذاتها مع منتصف الصفحة.
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

// قم بتعيين المحاذاة الأفقية والرأسية للنص داخل الشكل.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// أضف فقرة إلى مربع النص وأضف سلسلة من النص سيعرضها مربع النص.
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
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


