---
title: "Método Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName"
linktitle: "get_ShowSeriesName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName. Devuelve o establece un Booleano para indicar el comportamiento de visualización del nombre de la serie en las etiquetas de datos de toda la serie. true para mostrar el nombre de la serie; false para ocultarlo. Por defecto, false en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showseriesname/
---
## ChartDataLabelCollection::get_ShowSeriesName method


Devuelve o establece un Booleano para indicar el comportamiento de visualización del nombre de la serie en las etiquetas de datos de toda la serie. **true** para mostrar el nombre de la serie; **false** para ocultarlo. Por defecto **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowSeriesName()
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

## Ver también

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
