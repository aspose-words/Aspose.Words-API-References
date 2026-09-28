---
title: "Aspose::Words::Comparing::AdvancedCompareOptions класс"
linktitle: "AdvancedCompareOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Comparing::AdvancedCompareOptions класс. Позволяет задавать расширенные параметры сравнения в C++."
type: docs
weight: 500
url: /ru/cpp/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class


Позволяет задавать расширенные параметры сравнения.

```cpp
class AdvancedCompareOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [AdvancedCompareOptions](./advancedcompareoptions/)() |  |
| [get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/)() const | Указывает, следует ли игнорировать различия в уникальном идентификаторе DrawingML. |
| [get_IgnoreStoreItemId](./get_ignorestoreitemid/)() const | Указывает, следует ли игнорировать различия в идентификаторе элемента хранилища StructuredDocumentTag. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IgnoreDmlUniqueId](./set_ignoredmluniqueid/)(bool) | Сеттер для [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreDmlUniqueId](./get_ignoredmluniqueid/). |
| [set_IgnoreStoreItemId](./set_ignorestoreitemid/)(bool) | Сеттер для [Aspose::Words::Comparing::AdvancedCompareOptions::get_IgnoreStoreItemId](./get_ignorestoreitemid/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как сравнить SDT с одинаковым содержимым, но разным идентификатором элемента хранилища.
```cpp
auto docA = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 1.docx");
auto docB = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document with SDT 2.docx");

// Настройте параметры для сравнения SDT с одинаковым содержимым, но разным идентификатором элемента хранилища.
auto compareOptions = System::MakeObject<Aspose::Words::Comparing::CompareOptions>();
compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(false);

docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(8, docA->get_Revisions()->get_Count());

compareOptions->get_AdvancedOptions()->set_IgnoreStoreItemId(true);

docA->get_Revisions()->RejectAll();
docA->Compare(docB, u"user", System::DateTime::get_Now(), compareOptions);
ASSERT_EQ(0, docA->get_Revisions()->get_Count());
```

## См. также

* Namespace [Aspose::Words::Comparing](../)
* Library [Aspose.Words for C++](../../)
