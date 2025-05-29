---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية ParagraphFormat FirstLineIndent لتخصيص المسافات البادئة للسطر الأول أو المعلقة في مستنداتك بسهولة لتحسين إمكانية القراءة.
type: docs
weight: 120
url: /ar/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

يحصل على القيمة (بالنقاط) للسطر الأول أو المسافة البادئة المعلقة أو يعينها.

استخدم القيم الموجبة لتعيين المسافة البادئة للسطر الأول، والقيم السلبية لتعيين المسافة البادئة المعلقة.

```csharp
public double FirstLineIndent { get; set; }
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
