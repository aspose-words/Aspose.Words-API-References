---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count method"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count. Devuelve el número de grupos de series en esta colección en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/get_count/
---
## ChartSeriesGroupCollection::get_Count method


Devuelve el número de grupos de series en esta colección.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::get_Count()
```


## Ejemplos



Mostrar cómo eliminar el eje secundario.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Combo chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> seriesGroups = chart->get_SeriesGroups();

// Encontrar el eje secundario y eliminarlo de la colección.
for (int32_t i = 0; i < seriesGroups->get_Count(); i++)
{
    if (seriesGroups->idx_get(i)->get_AxisGroup() == Aspose::Words::Drawing::Charts::AxisGroup::Secondary)
    {
        seriesGroups->RemoveAt(i);
    }
}
```

## Ver también

* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
