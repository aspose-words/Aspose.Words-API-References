---
title: "Aspose::Words::TabStopCollection::GetPositionByIndex method"
linktitle: "GetPositionByIndex"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TabStopCollection::GetPositionByIndex метод. Получает позицию (в пунктах) табуляции по указанному индексу в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/tabstopcollection/getpositionbyindex/
---
## TabStopCollection::GetPositionByIndex method


Получает позицию (в пунктах) табуляции по указанному индексу.

```cpp
double Aspose::Words::TabStopCollection::GetPositionByIndex(int32_t index)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Индекс в коллекцию табуляций. |

### ReturnValue

Позиция табуляции.

## Примеры



Показывает, как найти табуляцию по её индексу и проверить её позицию.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::TabStopCollection> tabStops = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_TabStops();

tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(30), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);
tabStops->Add(Aspose::Words::ConvertUtil::MillimeterToPoint(60), Aspose::Words::TabAlignment::Left, Aspose::Words::TabLeader::Dashes);

// Проверьте позицию второй табуляции в коллекции.
ASSERT_NEAR(Aspose::Words::ConvertUtil::MillimeterToPoint(60), tabStops->GetPositionByIndex(1), 0.1);
```

## См. также

* Class [TabStopCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
