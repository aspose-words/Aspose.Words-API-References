---
title: "Метод Aspose::Words::Document::RemoveMacros"
linktitle: "RemoveMacros"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Document::RemoveMacros. Удаляет все макросы (VBA‑проект), а также панели инструментов и пользовательские настройки команд из документа в C++."
type: docs
weight: 69000
url: /ru/cpp/aspose.words/document/removemacros/
---
## Document::RemoveMacros method


Удаляет все макросы (VBA‑проект), а также панели инструментов и настройки команд из документа.

```cpp
void Aspose::Words::Document::RemoveMacros()
```

## Примечания


Удаляя все макросы из документа, вы можете убедиться, что документ не содержит макровирусов.

## Примеры



Показывает, как удалить все макросы из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Macro.docm");

ASSERT_TRUE(doc->get_HasMacros());
ASSERT_EQ(u"Project", doc->get_VbaProject()->get_Name());

// Удалите VBA‑проект документа вместе со всеми его макросами.
doc->RemoveMacros();

ASSERT_FALSE(doc->get_HasMacros());
ASSERT_TRUE(System::TestTools::IsNull(doc->get_VbaProject()));
```

## См. также

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
