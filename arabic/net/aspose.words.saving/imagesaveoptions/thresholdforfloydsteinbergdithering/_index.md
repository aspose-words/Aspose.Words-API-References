---
title: ImageSaveOptions.ThresholdForFloydSteinbergDithering
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. الحصول على أو تعيين الحد الذي يحدد القيمة لخطأ الترميز الثنائي في طريقة FloydSteinberg.ImageBinarizationMethod هي ImageBinarizationMethod.FloydSteinbergDithering.
type: docs
weight: 150
url: /ar/net/aspose.words.saving/imagesaveoptions/thresholdforfloydsteinbergdithering/
---
## ImageSaveOptions.ThresholdForFloydSteinbergDithering property

الحصول على أو تعيين الحد الذي يحدد القيمة لخطأ الترميز الثنائي في طريقة Floyd-Steinberg.[`ImageBinarizationMethod`](../../imagebinarizationmethod/) هي ImageBinarizationMethod.FloydSteinbergDithering.

```csharp
public byte ThresholdForFloydSteinbergDithering { get; set; }
```

### ملاحظات

القيمة الافتراضية هي 128.

### أمثلة

يوضح كيفية تعيين حد خطأ TIFF الثنائي عند استخدام طريقة Floyd-Steinberg لعرض صورة TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// عندما نحفظ المستند بتنسيق TIFF ، يمكننا تمرير كائن SaveOptions إليه
// اضبط التردد الذي ستطبقه Aspose.Words عند عرض هذه الصورة.
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

* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


