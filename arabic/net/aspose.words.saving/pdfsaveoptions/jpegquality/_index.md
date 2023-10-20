---
title: PdfSaveOptions.JpegQuality
linktitle: JpegQuality
articleTitle: JpegQuality
second_title: Aspose.Words لـ .NET
description: PdfSaveOptions JpegQuality ملكية. الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند PDF في C#.
type: docs
weight: 220
url: /ar/net/aspose.words.saving/pdfsaveoptions/jpegquality/
---
## PdfSaveOptions.JpegQuality property

الحصول على أو تعيين قيمة تحدد جودة صور JPEG داخل مستند PDF.

```csharp
public int JpegQuality { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 100.

يتم استخدام هذه الخاصية بالتزامن مع[`ImageCompression`](../imagecompression/) خيار.

يكون له تأثير فقط عندما يحتوي المستند على صور JPEG.

استخدم هذه الخاصية للحصول على جودة الصور داخل مستند أو تعيينها عند الحفظ بتنسيق PDF. قد تختلف القيمة من 0 إلى 100 حيث يعني 0 أسوأ جودة ولكن الحد الأقصى للضغط و100 يعني أفضل جودة ولكن الحد الأدنى من الضغط. إذا كانت الجودة هو 100 والصورة المصدر هي JPEG، وهذا يعني عدم وجود ضغط - سيتم حفظ البايتات الأصلية.

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

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
