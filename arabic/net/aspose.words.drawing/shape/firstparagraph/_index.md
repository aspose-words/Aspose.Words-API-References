---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words لـ .NET
description: استرجاع الفقرة الأولى من أي شكل بسهولة. حسّن تصميم مستندك باستخدام ميزة "الشكل في الفقرة الأولى" سهلة الاستخدام.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

يحصل على الفقرة الأولى في الشكل.

```csharp
public Paragraph FirstParagraph { get; }
```

## أمثلة

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
