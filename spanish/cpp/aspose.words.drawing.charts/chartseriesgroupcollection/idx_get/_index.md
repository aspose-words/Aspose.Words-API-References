---
title: "Método idx_get de Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection"
linktitle: "idx_get"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método idx_get de Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection. Devuelve un ChartSeriesGroup en el índice especificado en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/idx_get/
---
## ChartSeriesGroupCollection::idx_get method


Devuelve un [ChartSeriesGroup](../../chartseriesgroup/) en el índice especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::idx_get(int32_t index)
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

* Class [ChartSeriesGroup](../../chartseriesgroup/)
* Class [ChartSeriesGroupCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
