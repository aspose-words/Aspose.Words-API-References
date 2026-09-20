---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator método"
linktitle: "Método Aspose::Words::Fields::FieldMergeBarcode::get_ScalingFactor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator método. Obtiene o establece el separador de cadena usado para las etiquetas de datos de toda la serie. El valor predeterminado es una coma, excepto en los gráficos de pastel que muestran solo el nombre de la categoría y el porcentaje, cuando se debe usar un salto de línea en su lugar en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_separator/
---
## ChartDataLabelCollection::get_Separator method


Obtiene o establece el separador de cadena utilizado para las etiquetas de datos de toda la serie. El valor predeterminado es una coma, excepto en los gráficos de pastel que muestran solo el nombre de la categoría y el porcentaje, donde se debe usar un salto de línea.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Separator()
```


## Ejemplos



Muestra cómo trabajar con las etiquetas de datos de un gráfico de burbujas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Agrega una serie personalizada con coordenadas X/Y y el diámetro de cada una de las burbujas.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Habilita las etiquetas de datos y luego modifica su apariencia.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```


Muestra cómo trabajar con las etiquetas de datos de un gráfico de pastel.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Pie, 500, 300)->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Inserta una serie de gráfico personalizada con un nombre de categoría para cada uno de los sectores y su tabla de frecuencias.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel"}), System::MakeArray<double>({2.7, 3.2, 0.8}));

// Habilita las etiquetas de datos que mostrarán tanto el porcentaje como la frecuencia de cada sector y modifica su apariencia.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowLeaderLines(true);
dataLabels->set_ShowLegendKey(true);
dataLabels->set_ShowPercentage(true);
dataLabels->set_ShowValue(true);
dataLabels->set_Separator(u"; ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsPieChart.docx");
```

## Ver también

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
