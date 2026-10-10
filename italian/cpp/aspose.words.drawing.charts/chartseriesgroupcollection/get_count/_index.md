---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count method"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count. Restituisce il numero di gruppi di serie in questa collezione in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/get_count/
---
## ChartSeriesGroupCollection::get_Count method


Restituisce il numero di gruppi di serie in questa raccolta.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count()
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

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
