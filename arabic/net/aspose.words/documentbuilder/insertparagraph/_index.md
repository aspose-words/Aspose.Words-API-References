---
title: DocumentBuilder.InsertParagraph
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج فاصل فقرة في المستند.
type: docs
weight: 400
url: /ar/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

إدراج فاصل فقرة في المستند.

```csharp
public Paragraph InsertParagraph()
```

### قيمة الإرجاع

عقدة الفقرة التي تم إدراجها للتو. إنها نفس عقدة[`CurrentParagraph`](../currentparagraph/).

### ملاحظات

تنسيق الفقرة الحالي المحدد بواسطة[`ParagraphFormat`](../paragraphformat/) يتم استخدام الممتلكات.

يقطع الفقرة الحالية إلى قسمين. بعد إدراج الفقرة ، يتم وضع المؤشر في بداية الفقرة الجديدة.

### أمثلة

يوضح كيفية إدراج فقرة في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// طريقة "Writeln" تنهي الفقرة بعد إلحاق النص
// ثم يبدأ سطرًا جديدًا ، مضيفًا فقرة جديدة.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


