---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ضغط النص في PdfSaveOptions لتحسين مستنداتك. اختر نوع الضغط الأنسب لتخزين نصوص فعّال وتحميل أسرع.
type: docs
weight: 310
url: /ar/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

يحدد نوع الضغط الذي سيتم استخدامه لجميع النصوص في المستند.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## ملاحظات

الافتراضي هوFlate.

يزيد حجم الإخراج بشكل كبير عند حفظ مستند بدون ضغط.

## أمثلة

يوضح كيفية تطبيق ضغط النص عند حفظ مستند بتنسيق PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "TextCompression" على "PdfTextCompression.None" لعدم تطبيق أي
// ضغط النص عندما نحفظ المستند بصيغة PDF.
// اضبط خاصية "TextCompression" على "PdfTextCompression.Flate" لتطبيق ضغط ZIP
// إلى نص عند حفظ المستند بصيغة PDF. كلما كان حجم المستند أكبر، كان تأثير ذلك أكبر.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### أنظر أيضا

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
