---
title: "Метод Aspose::Words::Properties::DocumentProperty::ToByteArray"
linktitle: "ToByteArray"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Properties::DocumentProperty::ToByteArray. Возвращает значение свойства в виде массива байтов в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Возвращает значение свойства как массив байтов.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Примечания


Выбрасывает исключение, если тип свойства не является [ByteArray](../../propertytype/).

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

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
