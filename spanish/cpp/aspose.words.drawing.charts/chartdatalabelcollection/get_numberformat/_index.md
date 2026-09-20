---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat método"
linktitle: "get_NumberFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat método. Obtiene una instancia de ChartNumberFormat que permite establecer el formato numérico para las etiquetas de datos de toda la serie en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_numberformat/
---
## ChartDataLabelCollection::get_NumberFormat method


Obtiene una instancia de [ChartNumberFormat](../../chartnumberformat/) que permite establecer el formato numérico para las etiquetas de datos de toda la serie.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_NumberFormat()
```


## Ejemplos



Muestra cómo habilitar y configurar etiquetas de datos para una serie de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agrega un gráfico de líneas, luego elimina su serie de datos de demostración para comenzar con un gráfico limpio,
// y luego establece un título.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Inserta una serie de gráfico personalizada con los meses como categorías para el eje X,
// y los respectivos importes decimales para el eje Y.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Habilita las etiquetas de datos y luego aplica un formato numérico personalizado para los valores mostrados en las etiquetas de datos.
// Este formato tratará los valores decimales mostrados como millones de dólares estadounidenses.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## Ver también

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
