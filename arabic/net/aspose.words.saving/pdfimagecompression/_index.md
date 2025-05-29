---
title: PdfImageCompression Enum
linktitle: PdfImageCompression
articleTitle: PdfImageCompression
second_title: Aspose.Words لـ .NET
description: اكتشف أداة Aspose.Words.PdfImageCompression لتحسين ضغط الصور في ملفات PDF لديك، مما يعزز الجودة ويقلل حجم الملف بسهولة.
type: docs
weight: 6280
url: /ar/net/aspose.words.saving/pdfimagecompression/
---
## PdfImageCompression enumeration

يحدد نوع الضغط المطبق على الصور في ملف PDF.

```csharp
public enum PdfImageCompression
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | يختار تلقائيًا الضغط الأكثر ملاءمة لكل صورة. |
| Jpeg | `1` | ضغط Jpeg. لا يدعم الشفافية. |

## أمثلة

يوضح كيفية تحديد نوع الضغط لجميع الصور في المستند الذي نقوم بتحويله إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jpeg image:");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertParagraph();
builder.Writeln("Png image:");
builder.InsertImage(ImageDir + "Transparent background logo.png");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
// اضبط خاصية "ImageCompression" على "PdfImageCompression.Auto" لاستخدام
// خاصية "ImageCompression" للتحكم في جودة صور Jpeg التي تظهر في ملف PDF الناتج.
// اضبط خاصية "ImageCompression" على "PdfImageCompression.Jpeg" لاستخدام
// خاصية "ImageCompression" للتحكم في جودة جميع الصور التي تظهر في ملف PDF الناتج.
pdfSaveOptions.ImageCompression = pdfImageCompression;
// قم بضبط خاصية "JpegQuality" على "10" لتعزيز الضغط على حساب جودة الصورة.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
