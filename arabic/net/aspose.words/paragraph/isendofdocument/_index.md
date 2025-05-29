---
title: Paragraph.IsEndOfDocument
linktitle: IsEndOfDocument
articleTitle: IsEndOfDocument
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية IsEndOfDocument للفقرات. تعلّم كيفية تحديد الفقرة الأخيرة في القسم الأخير من مستندك لضمان تنسيق فعّال.
type: docs
weight: 60
url: /ar/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند.

```csharp
public bool IsEndOfDocument { get; }
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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
