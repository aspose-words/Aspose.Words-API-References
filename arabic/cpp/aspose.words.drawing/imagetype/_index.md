---
title: "Aspose::Words::Drawing::ImageType enum"
linktitle: "ImageType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ImageType enum. يحدد نوع (تنسيق) الصورة في مستند Microsoft Word بلغة C++."
type: docs
weight: 28000
url: /ar/cpp/aspose.words.drawing/imagetype/
---
## ImageType enum


يحدد نوع (تنسيق) الصورة في مستند Microsoft Word.

```cpp
enum class ImageType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| NoImage | 0 | لا توجد بيانات صورة. |
| غير معروف | 1 | نوع صورة غير معروف أو نوع صورة لا يمكن تخزينه مباشرة داخل مستند Microsoft Word. |
| Emf | 2 | ملف Windows Enhanced Metafile. |
| Wmf | 3 | Windows Metafile. |
| Pict | 4 | Macintosh PICT. سيتم الحفاظ على صورة موجودة في المستند، ولكن إدراج صور PICT جديدة في المستند غير مدعوم. |
| Jpeg | 5 | JPEG JFIF. |
| Png | 6 | Portable Network Graphics. |
| Bmp | 7 | Windows Bitmap. |
| Eps | 8 | Encapsulated PostScript. |
| WebP | 9 | WebP. |
| Gif | 10 | GIF. |


## أمثلة



يوضح كيفية إضافة صورة إلى شكل والتحقق من نوعها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> imgShape = builder->InsertImage(get_ImageDir() + u"Logo.jpg");
ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, imgShape->get_ImageData()->get_ImageType());
```

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
