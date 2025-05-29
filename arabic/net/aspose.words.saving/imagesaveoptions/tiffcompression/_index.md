---
title: ImageSaveOptions.TiffCompression
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words لـ .NET
description: قم بتحسين صور TIFF الخاصة بك باستخدام خاصية TiffCompression في ImageSaveOptions، مما يسمح لك باختيار أفضل طريقة ضغط للحصول على نتائج عالية الجودة.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

يحصل على نوع الضغط الذي سيتم تطبيقه عند حفظ الصور المولدة بتنسيق TIFF أو يحدده.

```csharp
public TiffCompression TiffCompression { get; set; }
```

## ملاحظات

لا يكون له تأثير إلا عند الحفظ بصيغة TIFF.

القيمة الافتراضية هيLzw.

## أمثلة

يوضح كيفية تحديد مخطط الضغط الذي سيتم تطبيقه على مستند نقوم بتحويله إلى صورة TIFF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Logo.jpg");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);
// اضبط خاصية "TiffCompression" على "TiffCompression.None" لعدم تطبيق أي ضغط أثناء الحفظ،
// مما قد يؤدي إلى إنتاج ملف إخراج كبير جدًا.
// اضبط خاصية "TiffCompression" على "TiffCompression.Rle" لتطبيق ضغط RLE
// قم بتعيين خاصية "TiffCompression" إلى "TiffCompression.Lzw" لتطبيق ضغط LZW.
// قم بضبط خاصية "TiffCompression" إلى "TiffCompression.Ccitt3" لتطبيق ضغط CCITT3.
// قم بتعيين خاصية "TiffCompression" إلى "TiffCompression.Ccitt4" لتطبيق ضغط CCITT4.
options.TiffCompression = tiffCompression;

doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);
```

### أنظر أيضا

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
