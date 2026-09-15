---
title: "Aspose::Words::Document::UpdateThumbnail طريقة"
linktitle: "UpdateThumbnail"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::UpdateThumbnail طريقة. يقوم بتحديث Thumbnail للمستند باستخدام الخيارات الافتراضية في C++."
type: docs
weight: 100000
url: /ar/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


يقوم بتحديث [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) للمستند باستخدام الخيارات الافتراضية.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


يقوم بتحديث [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) للمستند وفقاً للخيارات المحددة.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| خيارات | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | خيارات الإنشاء التي سيتم استخدامها. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
