---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey método"
linktitle: "get_ShowLegendKey"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey método. Permite especificar si la clave de leyenda debe mostrarse para las etiquetas de datos de toda la serie. El valor predeterminado es false en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showlegendkey/
---
## ChartDataLabelCollection::get_ShowLegendKey method


Permite especificar si se debe mostrar la clave de leyenda en las etiquetas de datos de toda la serie. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowLegendKey()
```


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
