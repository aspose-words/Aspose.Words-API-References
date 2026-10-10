---
title: "طريقة Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize"
linktitle: "get_ThumbnailSize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize. حجم الصورة المصغرة المُنشأة بالبكسل. القيمة الافتراضية هي 600x900 في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


حجم الصورة المصغرة المُنشأة بالبكسل. الافتراضي هو 600x900.

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
```


## أمثلة



يظهر كيفية تحديث صورة مصغرة للمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// هناك طريقتان لتعيين صورة مصغرة عند حفظ المستند بصيغة .epub.
// 1 -  استخدم الصفحة الأولى للمستند:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  استخدم الصورة الأولى الموجودة في المستند:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## انظر أيضًا

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
