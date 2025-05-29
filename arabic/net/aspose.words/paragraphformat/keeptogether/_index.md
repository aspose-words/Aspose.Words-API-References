---
title: ParagraphFormat.KeepTogether
linktitle: KeepTogether
articleTitle: KeepTogether
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat KeepTogether، وتأكد من بقاء جميع الأسطر معًا على صفحة واحدة لتحسين قابلية قراءة المستند وتقديمه بشكل احترافي.
type: docs
weight: 160
url: /ar/net/aspose.words/paragraphformat/keeptogether/
---
## ParagraphFormat.KeepTogether property

صحيح إذا كانت جميع الأسطر في الفقرة ستبقى على نفس الصفحة.

```csharp
public bool KeepTogether { get; set; }
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
