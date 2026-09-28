---
title: "Метод Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection"
linktitle: "get_IsMultiSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection. Возвращает true, если данный экземпляр является диапазонным (многоразделным) структурированным тегом документа в C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words.markup/istructureddocumenttag/get_ismultisection/
---
## IStructuredDocumentTag::get_IsMultiSection method


Возвращает true, если данный экземпляр является диапазонным (многоразделным) структурированным тегом документа.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_IsMultiSection()=0
```


## Примеры



Показывает, как получить тег структурированного документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags by id.docx");

// Получить тег структурированного документа по Id.
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt = doc->get_Range()->get_StructuredDocumentTags()->GetById(1160505028);
std::cout << System::Convert::ToString(sdt->get_IsMultiSection()) << std::endl;
std::cout << sdt->get_Title() << std::endl;

// Получить тег структурированного документа или диапазонный тег по Title.
sdt = doc->get_Range()->get_StructuredDocumentTags()->GetByTitle(u"Alias4");
std::cout << sdt->get_Id() << std::endl;
```

## См. также

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
