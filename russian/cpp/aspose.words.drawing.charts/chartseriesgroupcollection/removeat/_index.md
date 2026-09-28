---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt. Удаляет группу серий по указанному индексу. Все дочерние серии будут удалены из диаграммы в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection::RemoveAt method


Удаляет группу серий по указанному индексу. Все дочерние серии будут удалены из диаграммы.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt(int32_t index)
```


## Примеры



Показать, как удалить вторичную ось.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// Найдите вторичную ось и удалите её из коллекции.
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## См. также

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
