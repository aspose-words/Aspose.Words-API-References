---
title: TiffCompression Enum
linktitle: TiffCompression
articleTitle: TiffCompression
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.TiffCompression لحفظ ملفات TIFF بشكل مثالي. اختر نوع الضغط الأنسب لصور صفحات عالية الجودة بسهولة.
type: docs
weight: 6430
url: /ar/net/aspose.words.saving/tiffcompression/
---
## TiffCompression enumeration

يحدد نوع الضغط الذي سيتم تطبيقه عند حفظ صور الصفحة في ملف TIFF.

```csharp
public enum TiffCompression
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يحدد أي ضغط. |
| Rle | `1` | يحدد مخطط ضغط RLE. |
| Lzw | `2` | يحدد مخطط ضغط LZW. في Java يتم محاكاته بواسطة ضغط Deflate (Zip). |
| Ccitt3 | `3` | يحدد مخطط ضغط CCITT3. |
| Ccitt4 | `4` | يحدد مخطط ضغط CCITT4. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
