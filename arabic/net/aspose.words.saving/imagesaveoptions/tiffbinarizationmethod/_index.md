---
title: ImageSaveOptions.TiffBinarizationMethod
linktitle: TiffBinarizationMethod
articleTitle: TiffBinarizationMethod
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية TiffBinarizationMethod لخيار ImageSaveOptions. حوّل الصور بسهولة إلى تنسيق 1 بت لكل بوصة باستخدام ضغط Ccitt3 أو Ccitt4.
type: docs
weight: 170
url: /ar/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

يحصل على الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 بت لكل بوصة أو يعينها عندما[`SaveFormat`](../saveformat/) يكونTiff و [`TiffCompression`](../tiffcompression/) يساويCcitt3 أوCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

## ملاحظات

القيمة الافتراضية هيThreshold.

## أمثلة

يوضح كيفية تعيين عتبة خطأ تحويل TIFF إلى ثنائي عند استخدام طريقة Floyd-Steinberg لعرض صورة TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند بتنسيق TIFF، يمكننا تمرير كائن SaveOptions إلى
// اضبط التمويه الذي سيطبقه Aspose.Words عند عرض هذه الصورة.
// القيمة الافتراضية لخاصية "ThresholdForFloydSteinbergDithering" هي 128.
// تميل القيم الأعلى إلى إنتاج صور أغمق.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff)
{
    TiffCompression = TiffCompression.Ccitt3,
    TiffBinarizationMethod = ImageBinarizationMethod.FloydSteinbergDithering,
    ThresholdForFloydSteinbergDithering = 240
};

doc.Save(ArtifactsDir + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
```

### أنظر أيضا

* enum [ImageBinarizationMethod](../../imagebinarizationmethod/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
