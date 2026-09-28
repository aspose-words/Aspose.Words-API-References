---
title: "Класс Aspose::Words::Markup::StructuredDocumentTagCollection"
linktitle: "StructuredDocumentTagCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Markup::StructuredDocumentTagCollection. Коллекция экземпляров IStructuredDocumentTag, представляющих теги структурированных документов в указанном диапазоне. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class


Коллекция экземпляров [IStructuredDocumentTag](../istructureddocumenttag/), представляющих теги структурированных документов в указанном диапазоне. Чтобы узнать больше, посетите статью документации [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Count](./get_count/)() | Возвращает количество тегов структурированных документов в коллекции. |
| [GetById](./getbyid/)(int32_t) | Возвращает тег структурированного документа по идентификатору. |
| [GetByTag](./getbytag/)(const System::String\&) | Возвращает первый найденный в коллекции тег структурированного документа с указанным тегом. |
| [GetByTitle](./getbytitle/)(const System::String\&) | Возвращает первый найденный в коллекции тег структурированного документа с указанным заголовком. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Возвращает тег структурированного документа по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Удаляет тег структурированного документа с указанным идентификатором. |
| [RemoveAt](./removeat/)(int32_t) | Удаляет тег структурированного документа по указанному индексу. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
