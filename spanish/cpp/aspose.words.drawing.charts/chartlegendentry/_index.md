---
title: "Aspose::Words::Drawing::Charts::ChartLegendEntry clase"
linktitle: "ChartLegendEntry"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartLegendEntry clase. Representa una entrada de leyenda de gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class


Representa una entrada de la leyenda del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegendEntry : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                         public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de esta entrada de leyenda. |
| [get_IsHidden](./get_ishidden/)() const | Obtiene o establece un valor que indica si esta entrada está oculta en la leyenda del gráfico. El valor predeterminado es **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Setter para [Aspose::Words::Drawing::Charts::ChartLegendEntry::get_IsHidden](./get_ishidden/). |
| static [Type](./type/)() |  |
## Observaciones


Una entrada de leyenda corresponde a una serie de gráfico o línea de tendencia específica.

El texto de la entrada es el nombre de la serie o línea de tendencia. El texto no se puede cambiar.

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
