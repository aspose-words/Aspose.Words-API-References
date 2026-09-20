---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt. Elimina un grupo de series en el índice especificado. Todas las series secundarias serán eliminadas del gráfico en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroupcollection/removeat/
---
## ChartSeriesGroupCollection::RemoveAt method


Elimina un grupo de series en el índice especificado. Todas las series hijas serán eliminadas del gráfico.

```cpp
void Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection::RemoveAt(int32_t index)
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
