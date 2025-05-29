---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words لـ .NET
description: قم بتحسين ملف PDF الخاص بك باستخدام خاصية ImageCompression في PdfSaveOptions، مما يسمح لك باختيار أفضل نوع ضغط للحصول على صور نابضة بالحياة وعالية الجودة.
type: docs
weight: 200
url: /ar/net/aspose.words.saving/pdfsaveoptions/imagecompression/
---
## PdfSaveOptions.ImageCompression property

يحدد نوع الضغط الذي سيتم استخدامه لجميع الصور في المستند.

```csharp
public PdfImageCompression ImageCompression { get; set; }
```

## ملاحظات

الافتراضي هوAuto.

استخدامJpeg يتيح لك التحكم في جودة الصور في المستند الناتج من خلال[`JpegQuality`](../jpegquality/) ملكية.

استخدامJpeg يوفر أسرع سرعة تحويل عند مقارنته بأداء أنواع الضغط الأخرى، ولكن في هذه الحالة، يوجد ضغط JPEG مع فقدان البيانات.

استخدامAuto يتيح لك التحكم في جودة Jpeg في المستند الناتج من خلال[`JpegQuality`](../jpegquality/)الخاصية، ولكن بالنسبة للتنسيقات الأخرى، يتم استخراج بيانات البكسل الخام وحفظها باستخدام ضغط Flate. هذه الحالة أبطأ من تحويل Jpeg ولكنها بدون فقدان.

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

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
