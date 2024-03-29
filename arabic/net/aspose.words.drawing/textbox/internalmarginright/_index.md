---
title: TextBox.InternalMarginRight
linktitle: InternalMarginRight
articleTitle: InternalMarginRight
second_title: Aspose.Words لـ .NET
description: TextBox InternalMarginRight ملكية. يحدد الهامش الأيمن الداخلي بالنقاط للشكل في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

يحدد الهامش الأيمن الداخلي بالنقاط للشكل.

```csharp
public double InternalMarginRight { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 1/10 بوصة.

## أمثلة

يوضح كيفية تعيين الهوامش الداخلية لمربع النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل مربع نص آخر بهوامش محددة.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### أنظر أيضا

* class [TextBox](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
