---
title: ImageSaveOptions.TiffCompression
second_title: Aspose.Words لمراجع .NET API
description: ImageSaveOptions ملكية. الحصول على أو تحديد نوع الضغط المراد تطبيقه عند حفظ الصور المُنشأة بتنسيق TIFF.
type: docs
weight: 170
url: /ar/net/aspose.words.saving/imagesaveoptions/tiffcompression/
---
## ImageSaveOptions.TiffCompression property

الحصول على أو تحديد نوع الضغط المراد تطبيقه عند حفظ الصور المُنشأة بتنسيق TIFF.

```csharp
public TiffCompression TiffCompression { get; set; }
```

### ملاحظات

يكون له تأثير فقط عند الحفظ في TIFF.

النظام الأساسيLzw.

### أمثلة

يوضح كيفية تحديد نظام الضغط لتطبيقه على مستند نقوم بتحويله إلى صورة TIFF.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // قم بإنشاء كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "حفظ" المستند
            // لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // اضبط خاصية "TiffCompression" على "TiffCompression.None" لعدم تطبيق ضغط أثناء الحفظ ،
            // مما قد ينتج عنه ملف إخراج كبير جدًا.
            // اضبط خاصية "TiffCompression" على "TiffCompression.Rle" لتطبيق ضغط RLE
            // اضبط خاصية "TiffCompression" على "TiffCompression.Lzw" لتطبيق ضغط LZW.
            // اضبط خاصية "TiffCompression" على "TiffCompression.Ccitt3" لتطبيق ضغط CCITT3.
            // اضبط خاصية "TiffCompression" على "TiffCompression.Ccitt4" لتطبيق ضغط CCITT4.
            options.TiffCompression = tiffCompression;

            doc.Save(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff", options);

            switch (tiffCompression)
            {
                case TiffCompression.None:
                    Assert.That(3000000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Rle:
#if NET5_0_OR_GREATER
                    Assert.That(6000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#else
                    Assert.That(600000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
#endif
                    break;
                case TiffCompression.Lzw:
                    Assert.That(200000, Is.LessThan(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt3:
                    Assert.That(90000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
                case TiffCompression.Ccitt4:
                    Assert.That(20000, Is.AtLeast(new FileInfo(ArtifactsDir + "ImageSaveOptions.TiffImageCompression.tiff").Length));
                    break;
            }
```

### أنظر أيضا

* enum [TiffCompression](../../tiffcompression/)
* class [ImageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesaveoptions/)
* المجسم [Aspose.Words](../../../)


