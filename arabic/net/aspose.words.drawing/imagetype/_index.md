---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.ImageType لإدارة تنسيقات الصور بسهولة في مستندات Microsoft Word. حسّن مظهر مستندك!
type: docs
weight: 1410
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
| NoImage | `0` | لا توجد بيانات للصورة. |
| Unknown | `1` | نوع صورة غير معروف أو نوع صورة لا يمكن تخزينه مباشرة داخل مستند Microsoft Word. |
| Emf | `2` | ملف تعريف Windows المحسن. |
| Wmf | `3` | ملف تعريف Windows. |
| Pict | `4` | Macintosh PICT. سيتم حفظ الصورة الموجودة في المستند، ولكن إدراج صور PICT جديدة في المستند غير مدعوم. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | رسومات الشبكة المحمولة. |
| Bmp | `7` | خريطة نقطية لنظام Windows. |
| Eps | `8` | PostScript مُغلَّف. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## أمثلة

يوضح كيفية قراءة صورة WebP.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

يوضح كيفية إضافة صورة إلى شكل والتحقق من نوعها.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### أنظر أيضا

* property [ImageType](../imagedata/imagetype/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
