---
title: Enum ImageType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.ImageType تعداد. يحدد نوع تنسيق الصورة في مستند Microsoft Word.
type: docs
weight: 950
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
| NoImage | `0` | ليست بيانات الصورة . |
| Unknown | `1` | نوع صورة غير معروف أو نوع صورة لا يمكن تخزينه مباشرة داخل مستند Microsoft Word. |
| Emf | `2` | ملف تعريف محسن لـ Windows . |
| Wmf | `3` | ملف تعريف Windows. |
| Pict | `4` | Macintosh PICT. سيتم الاحتفاظ بالصورة الموجودة في المستند ، ولكن لا يتم دعم إدراج صور new PICT في المستند. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | رسومات الشبكة المحمولة. |
| Bmp | `7` | صورة نقطية لـ Windows . |

### أمثلة

يوضح كيفية إضافة صورة إلى شكل والتحقق من نوعه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // الصورة في عنوان URL هي ملف gif. يؤدي إدراجه في مستند إلى تحويله إلى ملف png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### أنظر أيضا

* property [ImageType](../imagedata/imagetype/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


