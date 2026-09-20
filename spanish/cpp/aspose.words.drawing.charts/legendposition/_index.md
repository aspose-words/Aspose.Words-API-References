---
title: "Aspose::Words::Drawing::Charts::LegendPosition enumeración"
linktitle: "LegendPosition"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::LegendPosition enumeración. Especifica las posiciones posibles para una leyenda de gráfico en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enum


Especifica las posibles posiciones para la leyenda del gráfico.

```cpp
enum class LegendPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | No se mostrará ninguna leyenda para el gráfico. |
| Inferior | 1 | Especifica que la leyenda se dibujará en la parte inferior del gráfico. |
| Izquierda | 2 | Especifica que la leyenda se dibujará a la izquierda del gráfico. |
| Derecha | 3 | Especifica que la leyenda se dibujará a la derecha del gráfico. |
| Superior | 4 | Especifica que la leyenda se dibujará en la parte superior del gráfico. |
| TopRight | 5 | Especifica que la leyenda se dibujará en la esquina superior derecha del gráfico. |


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
