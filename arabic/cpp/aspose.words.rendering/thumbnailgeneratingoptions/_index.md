---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions فئة"
linktitle: "ThumbnailGeneratingOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions فئة. يمكن استخدامها لتحديد خيارات إضافية عند إنشاء صورة مصغرة لمستند في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


يمكن استخدامه لتحديد خيارات إضافية عند إنشاء صورة مصغرة لمستند.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | يحدد ما إذا كان سيتم إنشاء صورة مصغرة من الصفحة الأولى للمستند أو من الصورة الأولى. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | حجم الصورة المصغرة المُنشأة بالبكسل. الافتراضي هو 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | مُعيّن لـ [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | مُعيّن لـ [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
