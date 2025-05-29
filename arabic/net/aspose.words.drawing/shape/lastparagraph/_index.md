---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى خاصية LastParagraph لاسترداد الفقرة الأخيرة في النموذج الخاص بك بسهولة، مما يعزز تخطيط المستند وقابليته للقراءة.
type: docs
weight: 130
url: /ar/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

يحصل على الفقرة الأخيرة في الشكل.

```csharp
public Paragraph LastParagraph { get; }
```

## أمثلة

يوضح كيفية تعيين اتجاه النص داخل مربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// انقل منشئ المستندات إلى داخل مربع النص وأضف نصًا.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتعيين اتجاه محتويات النص في مربع النص هذا.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### أنظر أيضا

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
