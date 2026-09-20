---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap método"
linktitle: "get_Overlap"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap método. Obtiene o establece el porcentaje de superposición de las barras o columnas de series en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Obtiene o establece el porcentaje de cuánto se superponen las barras o columnas de la serie.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Observaciones


Se aplica a los grupos de series de todos los tipos de barras y columnas.

El rango de valores aceptables es de -100 a 100 inclusive. Un valor de 0 indica que no hay espacio entre barras/columnas. Si el valor es -100, la distancia entre barras/columnas es igual a su ancho. Un valor de 100 significa que las barras/columnas se superponen completamente.

## Ejemplos



Muestra cómo configurar el ancho del espacio y la superposición.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Establece el ancho del espacio de columna y la superposición.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## Ver también

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
