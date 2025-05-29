---
title: TextBox.InternalMarginRight
linktitle: InternalMarginRight
articleTitle: InternalMarginRight
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TextBox InternalMarginRight لتخصيص الأشكال الخاصة بك باستخدام هوامش يمين دقيقة في النقاط لتحسين مرونة التصميم.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

يحدد الهامش الداخلي الأيمن بالنقاط للشكل.

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

//إدراج مربع نص آخر بهوامش محددة.
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
