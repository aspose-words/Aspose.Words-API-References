---
title: "Método Aspose::Words::Drawing::Charts::ChartLegend::get_Font"
linktitle: "get_Font"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Drawing::Charts::ChartLegend::get_Font. Proporciona acceso al formato de fuente predeterminado de las entradas de la leyenda. Para sobrescribir el formato de fuente de una entrada de leyenda específica, use la propiedad Font en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.drawing.charts/chartlegend/get_font/
---
## ChartLegend::get_Font method


Proporciona acceso al formato de fuente predeterminado de las entradas de la leyenda. Para sobrescribir el formato de fuente de una entrada de leyenda específica, use la propiedad [Font](../../chartlegendentry/get_font/).

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Drawing::Charts::ChartLegend::get_Font()
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

* Class [Font](../../../aspose.words/font/)
* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
