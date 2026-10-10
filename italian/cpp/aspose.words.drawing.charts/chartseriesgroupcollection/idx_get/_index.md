---
title: "Metodo Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get. Restituisce un ChartSeriesGroup all'indice specificato in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/idx_get/
---
## ChartSeriesGroupCollection::idx_get method


Restituisce un [ChartSeriesGroup](../../chartseriesgroup/) all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get(int32_t index)
```


## Esempi



Mostra come rimuovere l'asse secondario.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// Trova l'asse secondario e rimuovilo dalla collezione.
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## Vedi anche

* Class [ChartSeriesGroup](../../chartseriesgroup/)
* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
