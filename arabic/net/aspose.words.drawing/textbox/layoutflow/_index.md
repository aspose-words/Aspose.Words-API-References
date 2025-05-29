---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية TextBox LayoutFlow على تحسين تخطيط النص في الأشكال، مما يؤدي إلى تحسين مرونة التصميم وإمكانية قراءته لمشاريعك.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

يحدد تدفق تخطيط النص في الشكل.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## ملاحظات

القيمة الافتراضية هيHorizontal.

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

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
