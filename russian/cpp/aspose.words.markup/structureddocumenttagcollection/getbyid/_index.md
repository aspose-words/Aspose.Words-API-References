---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById метод"
linktitle: "GetById"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::GetById метод. Возвращает структурированный тег документа по идентификатору в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.markup/structureddocumenttagcollection/getbyid/
---
## StructuredDocumentTagCollection::GetById method


Возвращает тег структурированного документа по идентификатору.

```cpp
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> Aspose::Words::Markup::StructuredDocumentTagCollection::GetById(int32_t id)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| id | int32_t | Идентификатор структурированного тега документа. |
## Примечания


Возвращает null, если структурированный тег документа с указанным идентификатором не найден.

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
