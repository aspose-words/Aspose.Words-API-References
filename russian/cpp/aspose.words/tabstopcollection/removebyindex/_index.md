---
title: "Метод Aspose::Words::TabStopCollection::RemoveByIndex"
linktitle: "RemoveByIndex"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::TabStopCollection::RemoveByIndex. Удаляет табуляцию с указанным индексом из коллекции в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words/tabstopcollection/removebyindex/
---
## TabStopCollection::RemoveByIndex method


Удаляет табуляцию по указанному индексу из коллекции.

```cpp
void Aspose::Words::TabStopCollection::RemoveByIndex(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в коллекцию табуляций. |

## Примеры



Показывает, как выбрать табуляцию в документе по её индексу и удалить её.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

ASSERT_EQ(2, tabStops->get_Count());

// Удалить первую табуляцию.
tabStops->RemoveByIndex(0);

ASSERT_EQ(1, tabStops->get_Count());

doc->Save(get_ArtifactsDir() + u"TabStopCollection.RemoveByIndex.docx");
```

## См. также

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
