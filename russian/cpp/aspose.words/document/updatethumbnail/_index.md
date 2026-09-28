---
title: "Aspose::Words::Document::UpdateThumbnail метод"
linktitle: "UpdateThumbnail"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Document::UpdateThumbnail метод. Обновляет миниатюру документа, используя параметры по умолчанию в C++."
type: docs
weight: 100000
url: /ru/cpp/aspose.words/document/updatethumbnail/
---
## Document::UpdateThumbnail() method


Обновляет [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) документа, используя параметры по умолчанию.

```cpp
void Aspose::Words::Document::UpdateThumbnail()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::UpdateThumbnail(const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\&) method


Обновляет [Thumbnail](../../../aspose.words.properties/builtindocumentproperties/get_thumbnail/) документа в соответствии с указанными параметрами.

```cpp
void Aspose::Words::Document::UpdateThumbnail(const System::SharedPtr<Aspose::Words::Rendering::ThumbnailGeneratingOptions> &options)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| параметры | const System::SharedPtr\<Aspose::Words::Rendering::ThumbnailGeneratingOptions\>\& | Параметры генерации для использования. |

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

* Class [ThumbnailGeneratingOptions](../../../aspose.words.rendering/thumbnailgeneratingoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
