---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Series método"
linktitle: "get_Series"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Series método. Obtiene una colección de series que pertenecen a este grupo de series en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing.charts/chartseriesgroup/get_series/
---
## ChartSeriesGroup::get_Series method


Obtiene una colección de series que pertenecen a este grupo de series.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Series()
```


## Ejemplos



Muestra cómo trabajar con el eje secundario del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Eliminar la serie generada por defecto.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Crea un grupo de series adicional, también del tipo línea.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Especifique el uso de ejes secundarios para el nuevo grupo de series.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Oculta el eje X secundario.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Define el título del eje Y secundario.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Agrega una serie al nuevo grupo de series.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## Ver también

* Class [ChartSeriesCollection](../../chartseriescollection/)
* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
