---
title: Paragraph.IsEndOfDocument
second_title: Aspose.Words لمراجع .NET API
description: Paragraph ملكية. صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند.
type: docs
weight: 60
url: /ar/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند.

```csharp
public bool IsEndOfDocument { get; }
```

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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../paragraph/)
* المجسم [Aspose.Words](../../../)


