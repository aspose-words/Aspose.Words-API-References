---
title: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize"
linktitle: "get_DoughnutHoleSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize. Obtiene o establece el tamaño del agujero del gráfico de rosquilla principal como un porcentaje en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/get_doughnutholesize/
---
## ChartSeriesGroup::get_DoughnutHoleSize method


Obtiene o establece el tamaño del agujero del gráfico de rosquilla principal como un porcentaje.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_DoughnutHoleSize()
```

## Observaciones


Se aplica solo a los grupos de series del tipo [Doughnut](../../chartseriestype/).

El rango de valores aceptables es de 0 a 90 inclusive. El valor predeterminado es 75.

## Ejemplos



Muestra cómo crear y formatear un gráfico de dona.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Elimina la serie generada por defecto.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Formatea el gráfico de dona.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## Ver también

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
