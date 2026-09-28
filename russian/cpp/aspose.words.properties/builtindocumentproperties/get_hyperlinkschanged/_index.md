---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged метод"
linktitle: "get_HyperlinksChanged"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged метод. Указывает, были ли изменены гиперссылки в документе в C++."
type: docs
weight: 13500
url: /ru/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkschanged/
---
## BuiltInDocumentProperties::get_HyperlinksChanged method


Указывает, были ли изменены гиперссылки в документе.

```cpp
bool Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinksChanged()
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
