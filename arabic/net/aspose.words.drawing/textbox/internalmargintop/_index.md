---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words لـ .NET
description: TextBox InternalMarginTop ملكية. يحدد الهامش العلوي الداخلي بالنقاط للشكل في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

يحدد الهامش العلوي الداخلي بالنقاط للشكل.

```csharp
public double InternalMarginTop { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 1/20 بوصة.

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
