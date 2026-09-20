---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines método"
linktitle: "get_ShowLeaderLines"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines método. Permite especificar si las líneas guía de las etiquetas de datos deben mostrarse para las etiquetas de datos de toda la serie. El valor predeterminado es false en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showleaderlines/
---
## ChartDataLabelCollection::get_ShowLeaderLines method


Permite especificar si se deben mostrar líneas guía de etiquetas de datos para las etiquetas de datos de toda la serie. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLeaderLines()
```

## Observaciones


Se aplica solo a gráficos de pastel. Las líneas guía crean una conexión visual entre una etiqueta de datos y su punto de datos correspondiente.

El valor definido para esta propiedad puede ser sobrescrito para una etiqueta de datos individual usando la propiedad [ShowLeaderLines](../../chartdatalabel/get_showleaderlines/).

## Ejemplos



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
