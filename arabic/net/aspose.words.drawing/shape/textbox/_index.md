---
title: Shape.TextBox
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. يحدد السمات التي تحدد كيفية عرض النص في شكل.
type: docs
weight: 220
url: /ar/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

يحدد السمات التي تحدد كيفية عرض النص في شكل.

```csharp
public TextBox TextBox { get; }
```

### أمثلة

يوضح كيفية تعيين اتجاه النص داخل مربع نص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// انقل منشئ المستندات إلى داخل TextBox وأضف نصًا.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتعيين اتجاه لمحتويات النص في مربع النص هذا.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### أنظر أيضا

* class [TextBox](../../textbox/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


