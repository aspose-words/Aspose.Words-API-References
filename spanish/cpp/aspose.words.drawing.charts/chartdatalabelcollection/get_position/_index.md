---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position método"
linktitle: "get_Position"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position método. Obtiene o establece la posición de las etiquetas de datos en C++."
type: docs
weight: 5501
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_position/
---
## ChartDataLabelCollection::get_Position method


Obtiene o establece la posición de las etiquetas de datos.

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelPosition Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Position()
```

## Observaciones


La posición se puede establecer para las etiquetas de datos de los siguientes tipos de series de gráfico:

* [Bar](../../chartseriestype/), [Column](../../chartseriestype/), [Histogram](../../chartseriestype/), [Pareto](../../chartseriestype/), [Waterfall](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [InsideBase](../../chartdatalabelposition/), [InsideEnd](../../chartdatalabelposition/) and [OutsideEnd](../../chartdatalabelposition/);
* [BarStacked](../../chartseriestype/), [BarPercentStacked](../../chartseriestype/), [ColumnStacked](../../chartseriestype/), [ColumnPercentStacked](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [InsideBase](../../chartdatalabelposition/) and [InsideEnd](../../chartdatalabelposition/);
* [Bubble](../../chartseriestype/), [Bubble3D](../../chartseriestype/), [Line](../../chartseriestype/), [LineStacked](../../chartseriestype/), [LinePercentStacked](../../chartseriestype/), [Scatter](../../chartseriestype/), [Stock](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [Left](../../chartdatalabelposition/), [Right](../../chartdatalabelposition/), [Above](../../chartdatalabelposition/) and [Below](../../chartdatalabelposition/);
* [Pie](../../chartseriestype/), [Pie3D](../../chartseriestype/), [PieOfBar](../../chartseriestype/), [PieOfPie](../../chartseriestype/); allowed values: [Center](../../chartdatalabelposition/), [InsideEnd](../../chartdatalabelposition/), [OutsideEnd](../../chartdatalabelposition/) and [BestFit](../../chartdatalabelposition/);
* [BoxAndWhisker](../../chartseriestype/); allowed values: [Left](../../chartdatalabelposition/), [Right](../../chartdatalabelposition/), [Above](../../chartdatalabelposition/) and [Below](../../chartdatalabelposition/).



## Ejemplos



Muestra cómo establecer la posición de la etiqueta de datos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insertar gráfico de columnas.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();

// Eliminar la serie generada por defecto.
seriesColl->Clear();

// Agregar serie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"}), System::MakeArray<double>({4, 5, 6}));

// Mostrar etiquetas de datos y establecer el color de fuente.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_Font()->set_Color(System::Drawing::Color::get_White());

// Establecer la posición de la etiqueta de datos.
dataLabels->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::InsideBase);
dataLabels->idx_get(0)->set_Position(Aspose::Words::Drawing::Charts::ChartDataLabelPosition::OutsideEnd);
dataLabels->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_DarkRed());

doc->Save(get_ArtifactsDir() + u"Charts.LabelPosition.docx");
```

## Ver también

* Enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
