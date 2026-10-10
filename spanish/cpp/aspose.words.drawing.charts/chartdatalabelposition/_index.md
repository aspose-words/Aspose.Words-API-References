---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum"
linktitle: "ChartDataLabelPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelPosition enum. Especifica la posición de una etiqueta de datos de gráfico en C++."
type: docs
weight: 27334
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enum


Especifica la posición de una etiqueta de datos del gráfico.

```cpp
enum class ChartDataLabelPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Centro | 0 | Especifica que una etiqueta de datos debe mostrarse centrada en un marcador de datos. |
| Izquierda | 1 | Especifica que una etiqueta de datos debe mostrarse a la izquierda de un marcador de datos. |
| Derecha | 2 | Especifica que una etiqueta de datos debe mostrarse a la derecha de un marcador de datos. |
| Encima | 3 | Especifica que una etiqueta de datos debe mostrarse encima de un marcador de datos. |
| Debajo | 4 | Especifica que una etiqueta de datos debe mostrarse debajo de un marcador de datos. |
| InsideBase | 5 | Especifica que una etiqueta de datos debe mostrarse dentro de la base de un marcador de datos. |
| InsideEnd | 6 | Especifica que una etiqueta de datos debe mostrarse dentro del extremo de un marcador de datos. |
| OutsideEnd | 7 | Especifica que una etiqueta de datos debe mostrarse fuera del extremo de un marcador de datos. |
| BestFit | 8 | Especifica que una etiqueta de datos debe mostrarse en la posición más adecuada. |


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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
