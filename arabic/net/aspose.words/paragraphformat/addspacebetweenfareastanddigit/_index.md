---
title: ParagraphFormat.AddSpaceBetweenFarEastAndDigit
linktitle: AddSpaceBetweenFarEastAndDigit
articleTitle: AddSpaceBetweenFarEastAndDigit
second_title: Aspose.Words لـ .NET
description: ParagraphFormat AddSpaceBetweenFarEastAndDigit ملكية. الحصول على أو تعيين علامة تشير إلى ما إذا كان يتم ضبط التباعد بين الأحرف تلقائيًا بين مناطق من الأرقام ومناطق نص شرق آسيا في الفقرة الحالية في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/paragraphformat/addspacebetweenfareastanddigit/
---
## ParagraphFormat.AddSpaceBetweenFarEastAndDigit property

الحصول على أو تعيين علامة تشير إلى ما إذا كان يتم ضبط التباعد بين الأحرف تلقائيًا بين مناطق من الأرقام ومناطق نص شرق آسيا في الفقرة الحالية.

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

// تنهي طريقة "Writeln" الفقرة بعد إلحاق النص
// ثم يبدأ سطرًا جديدًا ويضيف فقرة جديدة.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
