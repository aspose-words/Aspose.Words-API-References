---
title: "Aspose::Words::TabStopCollection::GetIndexByPosition метод"
linktitle: "GetIndexByPosition"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TabStopCollection::GetIndexByPosition метод. Получает индекс табуляции с указанной позицией в пунктах в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/tabstopcollection/getindexbyposition/
---
## TabStopCollection::GetIndexByPosition method


Получает индекс табуляции с указанной позицией в пунктах.

```cpp
int32_t Aspose::Words::TabStopCollection::GetIndexByPosition(double position)
```


## Примеры



Показывает, как проверить позицию, чтобы увидеть, существует ли там табуляция, и получить её индекс.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

// Добавьте табуляцию на позицию 30 мм.
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Результат "0", возвращённый методом "GetIndexByPosition", подтверждает, что табуляция
// на 30 мм существует в этой коллекции, и её индекс равен 0.
ASSERT_EQ(0, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(30)));

// Значение "-1", возвращённое методом "GetIndexByPosition", подтверждает, что
// в этой коллекции нет табуляции с позицией 60 мм.
ASSERT_EQ(-1, tabStops->GetIndexByPosition(Aspose::Words::ConvertUtil::MillimeterToPoint(60)));
```

## См. также

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
