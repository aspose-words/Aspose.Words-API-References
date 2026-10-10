---
title: "Enumeración Aspose::Words::Drawing::Charts::ChartStyle"
linktitle: "ChartStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartStyle enum. Especifica estilos predefinidos de un gráfico en C++."
type: docs
weight: 27875
url: /es/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Especifica estilos predefinidos de un gráfico.

```cpp
enum class ChartStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Normal | 0 | Representa el estilo de gráfico predeterminado. |
| Muted | 1 | Un estilo con colores apagados. |
| Saturated | 2 | Un estilo con colores más saturados. |
| Shaded | 3 | Un estilo con puntos de datos sombreados. |
| Plano | 4 | Un estilo con puntos de datos planos sin degradado. |
| Shadowed | 5 | Un estilo con puntos de datos que tienen una sombra. |
| Degradado | 6 | Un estilo con relleno degradado de los puntos de datos. |
| Original | 7 | Un estilo con una apariencia original de un gráfico. |
| Transparent1 | 8 | Un estilo con puntos de datos transparentes. |
| Transparent2 | 9 | Un estilo con puntos de datos transparentes. |
| Outline | 10 | Un estilo con puntos de datos sin relleno, solo con contorno. |
| OutlineBlack | 11 | Un estilo con fondo de gráfico negro, en el que los puntos de datos no tienen relleno, solo contorno. |
| Negro | 12 | Un estilo con fondo de gráfico negro. |
| Grey | 13 | Un estilo con fondo de gráfico gris degradado. |
| Azul | 14 | Un estilo con fondo de gráfico azul. |
| ShadedPlot | 15 | Un estilo, en el que el área del gráfico está sombreada. |


## Ejemplos



Muestra cómo establecer y obtener el estilo del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un gráfico con el estilo Negro.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Obtener un gráfico para actualizar.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Obtener el estilo del gráfico.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
