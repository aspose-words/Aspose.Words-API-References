---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.PdfTextCompression enum لضغط محتوى PDF بكفاءة، وتحسين حجم الملف والأداء مع الحفاظ على الجودة.
type: docs
weight: 6330
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
| None | `0` | لا يوجد ضغط. |
| Flate | `1` | ضغط مسطح (ZIP). |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
