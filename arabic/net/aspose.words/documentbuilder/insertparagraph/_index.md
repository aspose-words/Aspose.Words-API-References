---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertParagraph في DocumentBuilder، مما يسمح بإنشاء فواصل فقرات سلسة لتحسين إمكانية القراءة.
type: docs
weight: 450
url: /ar/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

يقوم بإدراج فاصل فقرة في المستند.

```csharp
public Paragraph InsertParagraph()
```

### قيمة الإرجاع

عقدة الفقرة التي أُدرجت للتو. وهي نفس العقدة[`CurrentParagraph`](../currentparagraph/).

## ملاحظات

تنسيق الفقرة الحالية المحدد بواسطة[`ParagraphFormat`](../paragraphformat/) تم استخدام الخاصية.

يقسم الفقرة الحالية إلى نصفين. بعد إدراج الفقرة، يوضع المؤشر في بداية الفقرة الجديدة.

يتم طرح استثناء إذا لم يكن من الممكن إدراج فاصل فقرة في موضع المؤشر الحالي.

## أمثلة

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

// تنهي طريقة "Writeln" الفقرة بعد إضافة النص
// ثم يبدأ سطرًا جديدًا، ويضيف فقرة جديدة.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
