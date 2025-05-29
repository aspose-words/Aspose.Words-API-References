---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words لـ .NET
description: خصّص خصائص مربع نص الشكل لتحسين عرض النص وتحسين المظهر البصري لتصاميمك. أطلق العنان لإبداعك اليوم!
type: docs
weight: 230
url: /ar/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

يحدد السمات التي تحدد كيفية عرض النص في الشكل.

```csharp
public TextBox TextBox { get; }
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

* class [TextBox](../../textbox/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
