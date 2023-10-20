---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions TextCompression ملكية. يحدد نوع الضغط الذي سيتم استخدامه لكل المحتوى النصي في المستند في C#.
type: docs
weight: 290
url: /ar/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

يحدد نوع الضغط الذي سيتم استخدامه لكل المحتوى النصي في المستند.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## ملاحظات

الافتراضي هوFlate.

يزيد حجم الإخراج بشكل ملحوظ عند حفظ مستند دون ضغط.

## أمثلة

يوضح كيفية تطبيق ضغط النص عند حفظ مستند إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "ضغط النص" على "PdfTextCompression.None" حتى لا يتم تطبيق أي منها
// الضغط على النص عندما نحفظ المستند بصيغة PDF.
// اضبط خاصية "TextCompression" على "PdfTextCompression.Flate" لتطبيق ضغط ZIP
// إلى النص عندما نحفظ المستند إلى PDF. كلما كانت الوثيقة أكبر، كلما كان التأثير أكبر.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### أنظر أيضا

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
