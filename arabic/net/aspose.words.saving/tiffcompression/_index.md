---
title: Enum TiffCompression
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.TiffCompression تعداد. يحدد نوع الضغط المطلوب تطبيقه عند حفظ صور الصفحة في ملف TIFF.
type: docs
weight: 5630
url: /ar/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

يحدد نوع الضغط المطلوب تطبيقه عند حفظ صور الصفحة في ملف TIFF.

```csharp
public enum TiffCompression
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | يحدد عدم الضغط. |
| Rle | `1` | يحدد نظام ضغط RLE. |
| Lzw | `2` | يحدد نظام ضغط LZW. في Java تمت محاكاته بواسطة ضغط Deflate (Zip). |
| Ccitt3 | `3` | يحدد نظام الضغط CCITT3. |
| Ccitt4 | `4` | يحدد نظام الضغط CCITT4. |

### أمثلة

يوضح كيفية تحديد نظام الضغط لتطبيقه على مستند نقوم بتحويله إلى صورة TIFF.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            builder.InsertImage(ImageDir + "Logo.jpg");

            // أنشئ كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
            // لتعديل الطريقة التي تعرض بها هذه الطريقة المستند إلى صورة.
            ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Tiff);

            // اضبط خاصية "TiffCompression" على "TiffCompression.None" حتى لا يتم تطبيق أي ضغط أثناء الحفظ،
            // مما قد يؤدي إلى ملف إخراج كبير جدًا.
            // قم بتعيين خاصية "TiffCompression" على "TiffCompression.Rle" لتطبيق ضغط RLE
            // قم بتعيين خاصية "TiffCompression" على "TiffCompression.Lzw" لتطبيق ضغط LZW.
            // قم بتعيين خاصية "TiffCompression" على "TiffCompression.Ccitt3" لتطبيق ضغط CCITT3.
            // قم بتعيين خاصية "TiffCompression" على "TiffCompression.Ccitt4" لتطبيق ضغط CCITT4.
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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


