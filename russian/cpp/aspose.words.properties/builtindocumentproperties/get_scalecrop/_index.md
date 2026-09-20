---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop метод"
linktitle: "get_ScaleCrop"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop метод. Указывает, обрезана ли миниатюра документа или масштабирована для отображения на C++."
type: docs
weight: 24500
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_scalecrop/
---
## BuiltInDocumentProperties::get_ScaleCrop method


Указывает, обрезан ли миниатюра документа или масштабируется для соответствия отображению.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_ScaleCrop()
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
