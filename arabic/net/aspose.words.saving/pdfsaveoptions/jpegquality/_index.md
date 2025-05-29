---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words لـ .NET
description: قم بتحسين صور PDF الخاصة بك باستخدام خاصية JpegQuality في PdfSaveOptions، مما يسمح لك بالتحكم في جودة JPEG للحصول على صور مذهلة للمستندات.
type: docs
weight: 220
url: /ar/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

يحصل على قيمة تحدد جودة صور JPEG داخل مستند PDF أو يعينها.

```csharp
public int JpegQuality { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 100.

يتم استخدام هذه الخاصية بالتزامن مع[`ImageCompression`](../imagecompression/) خيار.

يكون له تأثير فقط عندما يحتوي المستند على صور JPEG.

استخدم هذه الخاصية للحصول على جودة الصور داخل مستند أو تعيينها عند الحفظ بتنسيق PDF. قد تختلف القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة ولكن أقصى ضغط ويعني 100 أفضل جودة ولكن أقل ضغط. إذا كانت الجودة 100 وكانت الصورة المصدر هي JPEG، فهذا يعني عدم وجود ضغط - سيتم حفظ البايتات الأصلية.

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

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
