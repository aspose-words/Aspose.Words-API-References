---
title: TextBox.LayoutFlow
second_title: Aspose.Words لمراجع .NET API
description: TextBox ملكية. يحدد تدفق تخطيط النص في شكل.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

يحدد تدفق تخطيط النص في شكل.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

### ملاحظات

النظام الأساسيHorizontal.

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

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../textbox/)
* المجسم [Aspose.Words](../../../)


