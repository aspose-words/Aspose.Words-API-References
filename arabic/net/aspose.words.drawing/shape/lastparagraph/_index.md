---
title: Shape.LastParagraph
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. الحصول على الفقرة الأخيرة في الشكل.
type: docs
weight: 120
url: /ar/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

الحصول على الفقرة الأخيرة في الشكل.

```csharp
public Paragraph LastParagraph { get; }
```

### أمثلة

يوضح كيفية ضبط اتجاه النص داخل مربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// انقل أداة إنشاء المستندات إلى داخل TextBox وأضف نصًا.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتعيين اتجاه لمحتويات النص في مربع النص هذا.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### أنظر أيضا

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


