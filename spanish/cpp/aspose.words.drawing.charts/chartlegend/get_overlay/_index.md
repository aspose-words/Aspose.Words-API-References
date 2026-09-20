---
title: "Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay método"
linktitle: "get_Overlay"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay método. Determina si se permite que otros elementos del gráfico se superpongan a la leyenda. El valor predeterminado es false en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing.charts/chartlegend/get_overlay/
---
## ChartLegend::get_Overlay method


Determina si se permite que otros elementos del gráfico se superpongan a la leyenda. El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartLegend::get_Overlay() const
```


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

* Class [ChartLegend](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
