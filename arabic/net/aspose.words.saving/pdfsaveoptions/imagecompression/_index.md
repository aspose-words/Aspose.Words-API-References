---
title: PdfSaveOptions.ImageCompression
linktitle: ImageCompression
articleTitle: ImageCompression
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions ImageCompression ملكية. يحدد نوع الضغط الذي سيتم استخدامه لجميع الصور في المستند في C#.
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

استخدامJpeg يتيح لك التحكم في جودة الصور في مستند الإخراج من خلال[`JpegQuality`](../jpegquality/) ملكية.

استخدامJpeg يوفر أسرع سرعة تحويل بالمقارنة مع أداء أنواع الضغط الأخرى، ولكن في هذه الحالة، هناك ضغط JPEG مع فقدان.

استخدامAuto يتيح لك التحكم في جودة ملف Jpeg في مستند الإخراج من خلال ملف[`JpegQuality`](../jpegquality/)الخاصية، ولكن بالنسبة للتنسيقات الأخرى، يتم استخراج بيانات البكسل الأولية وحفظها باستخدام ضغط Flate. هذه الحالة أبطأ من تحويل Jpeg ولكنها لا تفقد البيانات.

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

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// اضبط خاصية "ImageCompression" على "PdfImageCompression.Auto" لاستخدامها
// خاصية "ImageCompression" للتحكم في جودة صور Jpeg التي تنتهي في ملف PDF الناتج.
// اضبط خاصية "ImageCompression" على "PdfImageCompression.Jpeg" لاستخدامها
// خاصية "ImageCompression" للتحكم في جودة جميع الصور التي تنتهي في ملف PDF الناتج.
pdfSaveOptions.ImageCompression = pdfImageCompression;

// اضبط خاصية "JpegQuality" على "10" لتعزيز الضغط على حساب جودة الصورة.
pdfSaveOptions.JpegQuality = 10;

doc.Save(ArtifactsDir + "PdfSaveOptions.ImageCompression.pdf", pdfSaveOptions);
```

### أنظر أيضا

* enum [PdfImageCompression](../../pdfimagecompression/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
