---
title: ParagraphFormat.AddSpaceBetweenFarEastAndDigit
linktitle: AddSpaceBetweenFarEastAndDigit
articleTitle: AddSpaceBetweenFarEastAndDigit
second_title: Aspose.Words لـ .NET
description: قم بتحسين تخطيط مستندك باستخدام الخاصية AddSpaceBetweenFarEastAndDigit، مما يعزز قابلية القراءة من خلال ضبط المسافة بين النص والأرقام في شرق آسيا.
type: docs
weight: 20
url: /ar/net/aspose.words/paragraphformat/addspacebetweenfareastanddigit/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndDigit property

يحصل على أو يعين علمًا يشير إلى ما إذا كان يتم تعديل المسافة بين الأحرف تلقائيًا بين مناطق من الأرقام ومناطق النص في شرق آسيا في الفقرة الحالية.

```csharp
public bool AddSpaceBetweenFarEastAndDigit { get; set; }
```

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

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
