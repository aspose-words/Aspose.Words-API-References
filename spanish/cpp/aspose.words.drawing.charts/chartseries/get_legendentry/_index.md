---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry método"
linktitle: "get_LegendEntry"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry método. Obtiene una entrada de leyenda para esta serie de gráfico en C++."
type: docs
weight: 9000
url: /es/cpp/aspose.words.drawing.charts/chartseries/get_legendentry/
---
## ChartSeries::get_LegendEntry method


Obtiene una entrada de leyenda para esta serie de gráfico.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> Aspose::Words::Drawing::Charts::ChartSeries::get_LegendEntry()
```


## Ejemplos



Muestra cómo trabajar con una fuente de leyenda.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Reporting engine template - Chart series.docx");
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> chartLegend = chart->get_Legend();
// Establezca el tamaño de fuente predeterminado para todas las entradas de leyenda.
chartLegend->get_Font()->set_Size(14);
// Cambie la fuente para una entrada de leyenda específica.
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Italic(true);
chartLegend->get_LegendEntries()->idx_get(1)->get_Font()->set_Size(12);
// Obtenga la entrada de leyenda para la serie de gráfico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntry> legendEntry = chart->get_Series()->idx_get(0)->get_LegendEntry();

doc->Save(get_ArtifactsDir() + u"Charts.LegendFont.docx");
```

## Ver también

* Class [ChartLegendEntry](../../chartlegendentry/)
* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
