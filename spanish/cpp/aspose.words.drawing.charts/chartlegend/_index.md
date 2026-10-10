---
title: "Aspose::Words::Drawing::Charts::ChartLegend clase"
linktitle: "ChartLegend"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend clase. Representa las propiedades de la leyenda del gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class


Representa las propiedades de la leyenda del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartLegend : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource,
                    public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente predeterminado de las entradas de la leyenda. Para sobrescribir el formato de fuente de una entrada de leyenda específica, use el[Font](../chartlegendentry/get_font/) propiedad. |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y línea de la leyenda. |
| [get_LegendEntries](./get_legendentries/)() const | Devuelve una colección de entradas de leyenda para todas las series y líneas de tendencia del gráfico principal. |
| [get_Overlay](./get_overlay/)() const | Determina si se permite que otros elementos del gráfico se superpongan a la leyenda. El valor predeterminado es **false**. |
| [get_Position](./get_position/)() | Especifica la posición de la leyenda en un gráfico. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Overlay](./set_overlay/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay](./get_overlay/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::LegendPosition) | Método set para [Aspose::Words::Drawing::Charts::ChartLegend::get_Position](./get_position/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo editar la apariencia de la leyenda de un gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

ASSERT_EQ(3, chart->get_Series()->get_Count());
ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

// Mueva la leyenda del gráfico a la esquina superior derecha.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegend> legend = chart->get_Legend();
legend->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::TopRight);

// Dé a otros elementos del gráfico, como el diagrama, más espacio permitiendo que se superpongan a la leyenda.
legend->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartLegend.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
