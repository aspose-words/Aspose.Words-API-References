---
title: "Aspose::Words::NodeCollection::RemoveAt метод"
linktitle: "RemoveAt"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeCollection::RemoveAt метод. Удаляет узел с указанным индексом из коллекции и из документа в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/nodecollection/removeat/
---
## NodeCollection::RemoveAt method


Удаляет узел по указанному индексу из коллекции и из документа.

```cpp
void Aspose::Words::NodeCollection::RemoveAt(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс узла. Допускаются отрицательные индексы, указывающие доступ с конца списка. Например, -1 означает последний узел, -2 — предпоследний и т.д. |

## Примеры



Показывает, как добавлять и удалять разделы в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Удалите первый раздел из документа.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Добавьте копию текущего первого раздела в конец документа.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## См. также

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
