---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument метод"
linktitle: "get_SharedDocument"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument метод. Указывает, является ли документ совместно используемым в C++."
type: docs
weight: 25500
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_shareddocument/
---
## BuiltInDocumentProperties::get_SharedDocument method


Указывает, является ли документ общим.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_SharedDocument()
```

## Примечания


Aspose.Words не обновляет это свойство.

## Примеры



Показывает, как получить расширенные свойства.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Extended properties.docx");
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_ScaleCrop());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_SharedDocument());
ASSERT_TRUE(doc->get_BuiltInDocumentProperties()->get_HyperlinksChanged());
```

## См. также

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
