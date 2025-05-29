---
title: ImageBinarizationMethod Enum
linktitle: ImageBinarizationMethod
articleTitle: ImageBinarizationMethod
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة Aspose.Words.ImageBinarizationMethod لثنائية الصور الفعالة. حسّن معالجة مستنداتك باستخدام تقنيات متقدمة.
type: docs
weight: 5950
url: /ar/net/aspose.words.saving/imagebinarizationmethod/
---
## ImageBinarizationMethod enumeration

يحدد الطريقة المستخدمة لتحويل الصورة إلى صورة ثنائية.

```csharp
public enum ImageBinarizationMethod
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Threshold | `0` | يحدد طريقة العتبة. |
| FloydSteinbergDithering | `1` | يحدد التمويه باستخدام طريقة انتشار خطأ Floyd-Steinberg. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
