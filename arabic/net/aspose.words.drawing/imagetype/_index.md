---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.ImageType تعداد. يحدد نوع تنسيق الصورة في مستند Microsoft Word في C#.
type: docs
weight: 1080
url: /ar/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

يحدد نوع (تنسيق) الصورة في مستند Microsoft Word.

```csharp
public enum ImageType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| NoImage | `0` | لا توجد بيانات صورة. |
| Unknown | `1` | نوع صورة غير معروف أو نوع صورة لا يمكن تخزينه مباشرة داخل مستند Microsoft Word. |
| Emf | `2` | ملف تعريف Windows المحسن. |
| Wmf | `3` | ملف تعريف Windows. |
| Pict | `4` | ماكنتوش PICT. سيتم الاحتفاظ بالصورة الموجودة في المستند، ولكن إدراج صور new PICT في المستند غير مدعوم. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | رسومات الشبكة المحمولة. |
| Bmp | `7` | الصورة النقطية لنظام Windows. |
| Eps | `8` | بوستسكريبت مغلف. |

## أمثلة

يوضح كيفية إضافة صورة إلى شكل والتحقق من نوعها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // الصورة الموجودة في عنوان URL هي .gif. يؤدي إدراجه في مستند إلى تحويله إلى ملف .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### أنظر أيضا

* property [ImageType](../imagedata/imagetype/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
