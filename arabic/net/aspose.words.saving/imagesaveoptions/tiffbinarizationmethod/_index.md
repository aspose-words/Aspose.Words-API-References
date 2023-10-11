---
title: ImageSaveOptions.TiffBinarizationMethod
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. الحصول على أو تعيين الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 bpp عندماSaveFormat يكونTiff و TiffCompression مساوي لCcitt3 أوCcitt4 .
type: docs
weight: 170
url: /ar/net/aspose.words.saving/imagesaveoptions/tiffbinarizationmethod/
---
## ImageSaveOptions.TiffBinarizationMethod property

الحصول على أو تعيين الطريقة المستخدمة أثناء تحويل الصور إلى تنسيق 1 bpp عندما[`SaveFormat`](../saveformat/) يكونTiff و [`TiffCompression`](../tiffcompression/) مساوي لCcitt3 أوCcitt4 .

```csharp
public ImageBinarizationMethod TiffBinarizationMethod { get; set; }
```

### ملاحظات

القيمة الافتراضية هيThreshold.

### أمثلة

يوضح كيفية تعيين حد خطأ التنسيق الثنائي TIFF عند استخدام طريقة Floyd-Steinberg لعرض صورة TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند كملف TIFF، يمكننا تمرير كائن SaveOptions إليه
// اضبط التردد الذي سيطبقه Aspose.Words عند عرض هذه الصورة.
// القيمة الافتراضية لخاصية "ThresholdForFloydSteinbergDithering" هي 128.
// تميل القيم الأعلى إلى إنتاج صور أكثر قتامة.
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
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


