---
title: "Метод Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize"
linktitle: "get_ThumbnailSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize. Размер генерируемой миниатюры в пикселях. По умолчанию 600x900 в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_thumbnailsize/
---
## ThumbnailGeneratingOptions::get_ThumbnailSize method


Размер сгенерированной миниатюры в пикселях. По умолчанию 600x900.

```cpp
System::Drawing::Size Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize() const
```


## Примеры



Показывает, как обновить миниатюру документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Существует два способа установить изображение миниатюры при сохранении документа в .epub.
// 1 -  Использовать первую страницу документа:
doc->UpdateThumbnail();
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstPage.epub");

// 2 -  Использовать первое найденное в документе изображение:
auto options = System::MakeObject<Aspose::Words::Rendering::ThumbnailGeneratingOptions>();
options->set_ThumbnailSize(System::Drawing::Size(400, 400));
options->set_GenerateFromFirstPage(false);

doc->UpdateThumbnail(options);
doc->Save(get_ArtifactsDir() + u"Document.UpdateThumbnail.FirstImage.epub");
```

## См. также

* Class [ThumbnailGeneratingOptions](../)
* Namespace [Aspose::Words::Rendering](../../)
* Library [Aspose.Words for C++](../../../)
