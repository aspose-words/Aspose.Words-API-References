---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_BubbleSizes method"
linktitle: "get_BubbleSizes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_BubbleSizes method. Obtiene una colección de tamaños de burbuja para esta serie del gráfico en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.drawing.charts/chartseries/get_bubblesizes/
---
## ChartSeries::get_BubbleSizes method


Obtiene una colección de tamaños de burbujas para esta serie del gráfico.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::BubbleSizeCollection> Aspose::Words::Drawing::Charts::ChartSeries::get_BubbleSizes()
```


## Ejemplos



Muestra cómo trabajar con el código de formato de los datos del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un gráfico de burbujas.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Eliminar la serie generada por defecto.
chart->get_Series()->Clear();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Series1", System::MakeArray<double>({1, 1.9, 2.45, 3}), System::MakeArray<double>({1, -0.9, 1.82, 0}), System::MakeArray<double>({2, 1.1, 2.95, 2}));

// Mostrar etiquetas de datos.
series->set_HasDataLabels(true);
series->get_DataLabels()->set_ShowCategoryName(true);
series->get_DataLabels()->set_ShowValue(true);
series->get_DataLabels()->set_ShowBubbleSize(true);

// Establece códigos de formato de datos.
series->get_XValues()->set_FormatCode(u"#,##0.0#");
series->get_YValues()->set_FormatCode(u"#,##0.0#;[Red]\\-#,##0.0#");
series->get_BubbleSizes()->set_FormatCode(u"#,##0.0#");

doc->Save(get_ArtifactsDir() + u"Charts.FormatCode.docx");
```

## Ver también

* Class [BubbleSizeCollection](../../bubblesizecollection/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
