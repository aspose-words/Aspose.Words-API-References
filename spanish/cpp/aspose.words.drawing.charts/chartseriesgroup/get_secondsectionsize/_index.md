---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize método"
linktitle: "get_SecondSectionSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize. Obtiene o establece el tamaño de la sección secundaria del gráfico circular como un porcentaje en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Obtiene o establece el tamaño de la sección secundaria del gráfico circular como un porcentaje.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Observaciones


Se aplica a los grupos de series de los tipos [PieOfPie](../../chartseriestype/) y [PieOfBar](../../chartseriestype/).

El rango de valores aceptables es de 5 a 200 inclusive. El valor predeterminado es 75.

## Ejemplos



Muestra cómo crear y formatear un gráfico de pastel de pastel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Elimina la serie generada por defecto.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Formatee el gráfico de pastel de pastel.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## Ver también

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
