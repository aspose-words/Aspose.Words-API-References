---
title: Enum PdfTextCompression
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfTextCompression تعداد. يحدد نوع الضغط المطبق على كل المحتوى في ملف PDF باستثناء الصور.
type: docs
weight: 5250
url: /ar/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

يحدد نوع الضغط المطبق على كل المحتوى في ملف PDF باستثناء الصور.

```csharp
public enum PdfTextCompression
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | بدون ضغط . |
| Flate | `1` | ضغط Flate (ZIP) . |

### أمثلة

يوضح كيفية تطبيق ضغط النص عند حفظ مستند في PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "TextCompression" على "PdfTextCompression.None" لعدم تطبيق أي منها
// الضغط على النص عندما نحفظ المستند في PDF.
// اضبط خاصية "TextCompression" على "PdfTextCompression.Flate" لتطبيق ضغط ZIP
// إلى النص عندما نحفظ المستند في PDF. كلما زاد حجم المستند ، زاد تأثير ذلك.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


