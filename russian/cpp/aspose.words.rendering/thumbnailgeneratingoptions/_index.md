---
title: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class"
linktitle: "ThumbnailGeneratingOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Rendering::ThumbnailGeneratingOptions class. Можно использовать для указания дополнительных параметров при создании миниатюры документа в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.rendering/thumbnailgeneratingoptions/
---
## ThumbnailGeneratingOptions class


Можно использовать для указания дополнительных параметров при создании миниатюры документа.

```cpp
class ThumbnailGeneratingOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_GenerateFromFirstPage](./get_generatefromfirstpage/)() const | Указывает, генерировать ли миниатюру с первой страницы документа или с первого изображения. |
| [get_ThumbnailSize](./get_thumbnailsize/)() const | Размер сгенерированной миниатюры в пикселях. По умолчанию 600x900. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_GenerateFromFirstPage](./set_generatefromfirstpage/)(bool) | Сеттер для [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_GenerateFromFirstPage](./get_generatefromfirstpage/). |
| [set_ThumbnailSize](./set_thumbnailsize/)(System::Drawing::Size) | Сеттер для [Aspose::Words::Rendering::ThumbnailGeneratingOptions::get_ThumbnailSize](./get_thumbnailsize/). |
| [ThumbnailGeneratingOptions](./thumbnailgeneratingoptions/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Rendering](../)
* Library [Aspose.Words for C++](../../)
