---
title: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove метод"
linktitle: "Remove"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Markup::StructuredDocumentTagCollection::Remove метод. Удаляет структурированный тег документа с указанным идентификатором в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection::Remove method


Удаляет тег структурированного документа с указанным идентификатором.

```cpp
void Aspose::Words::Markup::StructuredDocumentTagCollection::Remove(int32_t id)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| id | int32_t | Идентификатор структурированного тега документа. |

## Примеры



Показывает, как удалить структурированный тег документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTagCollection> structuredDocumentTags = doc->get_Range()->get_StructuredDocumentTags();
System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag> sdt;
for (int32_t i = 0; i < structuredDocumentTags->get_Count(); i++)
{
    sdt = structuredDocumentTags->idx_get(i);
    std::cout << sdt->get_Title() << std::endl;
}

sdt = structuredDocumentTags->GetById(1691867797);
ASSERT_EQ(1691867797, sdt->get_Id());

ASSERT_EQ(5, structuredDocumentTags->get_Count());
// Удалите структурированный тег документа по идентификатору.
structuredDocumentTags->Remove(1691867797);
// Удалите структурированный тег документа в позиции 0.
structuredDocumentTags->RemoveAt(0);
ASSERT_EQ(3, structuredDocumentTags->get_Count());
```

## См. также

* Class [StructuredDocumentTagCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
