---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail метод"
linktitle: "get_Thumbnail"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail метод. Получает или задаёт миниатюру документа в C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Получает или задает миниатюру документа.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Примечания


Пока это свойство используется только при экспорте документа в ePub, оно не читается и не записывается в другие форматы документов.

Изображение произвольного формата можно установить в это свойство, но формат проверяется при экспорте.

Для публикации ePub можно использовать только изображения gif, jpeg и png.

## Примеры



Показывает, как добавить миниатюру к документу, который мы сохраняем как Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Если мы сохраняем документ, у которого свойство "Thumbnail" содержит добавленные нами данные изображения, как Epub,
// чтатель, открывающий этот документ, может отобразить изображение до первой страницы.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Мы можем извлечь миниатюру документа и сохранить её в локальной файловой системе.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
