---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
linktitle: ThresholdForFloydSteinbergDithering
articleTitle: ThresholdForFloydSteinbergDithering
second_title: Aspose.Words لـ .NET
description: حسّن صورك باستخدام عتبة ImageSaveOptions لتقنية Floyd-Steinberg Dithering. تحكّم في أخطاء التثنية للحصول على نتائج مذهلة في معالجة الصور.
type: docs
weight: 160
url: /ar/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

يحصل على أو يعين الحد الذي يحدد قيمة لخطأ التثنية في طريقة Floyd-Steinberg. عندما[`ImageBinarizationMethod`](../../imagebinarizationmethod/) يكونFloydSteinbergDithering .

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

## ملاحظات

القيمة الافتراضية هي 128.

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

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
