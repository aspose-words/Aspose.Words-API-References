---
title: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth"
linktitle: "get_GapWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth. Obtiene o establece el porcentaje de ancho de espacio entre los elementos del gráfico en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Obtiene o establece el porcentaje del ancho de espacio entre los elementos del gráfico.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Observaciones


Se aplica solo a los grupos de series de los tipos de barra, columna, pastel-de-barra, pastel-de-pastel, histograma, caja y bigotes, cascada y embudo.

El rango de valores aceptables es de 0 a 500 inclusive. Para los grupos de series basados en barra/columna, la propiedad representa el espacio entre los grupos de barras como un porcentaje de su ancho. Para los gráficos de pastel-de-pastel y barra-de-pastel, este es el espacio entre las secciones primaria y secundaria del gráfico.

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
