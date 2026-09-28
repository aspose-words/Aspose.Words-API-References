---
title: "Метод Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle"
linktitle: "GetByTitle"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle. Возвращает первый структурированный тег документа, найденный в коллекции с указанным заголовком, в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection::GetByTitle method


Возвращает первый найденный в коллекции тег структурированного документа с указанным заголовком.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetByTitle(const System::String &title)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| title | const System::String\& | Заголовок структурированного тега документа. |
## Примечания


Возвращает null, если структурированный тег документа с указанным заголовком не найден.

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

* Interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
