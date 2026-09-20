---
title: "Метод Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage"
linktitle: "get_GenerateFromFirstPage"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage. Указывает, следует ли генерировать миниатюру с первой страницы документа или с первого изображения в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.rendering/thumbnailgeneratingoptions/get_generatefromfirstpage/
---
## ThumbnailGeneratingOptions::get_GenerateFromFirstPage method


Указывает, генерировать ли миниатюру с первой страницы документа или с первого изображения.

```cpp
bool Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage() const
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
