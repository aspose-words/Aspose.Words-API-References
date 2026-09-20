---
title: "Clase Aspose::Words::Drawing::Charts::AxisTickLabels"
linktitle: "AxisTickLabels"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::AxisTickLabels. Representa las propiedades de las etiquetas de marcas de graduación del eje en C++."
type: docs
weight: 3250
url: /es/cpp/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class


Representa las propiedades de las etiquetas de marcas de graduación del eje.

```cpp
class AxisTickLabels : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Alignment](./get_alignment/)() | Obtiene o establece la alineación del texto de las etiquetas de marcas de graduación del eje. |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de las etiquetas de marcas de graduación. |
| [get_IsAutoSpacing](./get_isautospacing/)() | Obtiene o establece una bandera que indica si se debe usar un intervalo automático para dibujar las etiquetas de marcas de graduación. |
| [get_Offset](./get_offset/)() | Obtiene o establece la distancia de las etiquetas de marcas de graduación al eje. |
| [get_Orientation](./get_orientation/)() | Obtiene o establece la orientación del texto de la etiqueta de la marca de graduación. |
| [get_Position](./get_position/)() | Obtiene o establece la posición de las etiquetas de marcas de graduación en el eje. |
| [get_Rotation](./get_rotation/)() | Obtiene o establece la rotación de las etiquetas de marcas de graduación en grados. |
| [get_Spacing](./get_spacing/)() | Obtiene o establece el intervalo en el que se dibujan las etiquetas de los marcadores. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Alignment](./set_alignment/)(Aspose::Words::ParagraphAlignment) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Alignment](./get_alignment/). |
| [set_IsAutoSpacing](./set_isautospacing/)(bool) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_IsAutoSpacing](./get_isautospacing/). |
| [set_Offset](./set_offset/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Offset](./get_offset/). |
| [set_Orientation](./set_orientation/)(Aspose::Words::Drawing::ShapeTextOrientation) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation](./get_orientation/). |
| [set_Position](./set_position/)(Aspose::Words::Drawing::Charts::AxisTickLabelPosition) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Position](./get_position/). |
| [set_Rotation](./set_rotation/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Rotation](./get_rotation/). |
| [set_Spacing](./set_spacing/)(int32_t) | Establecedor para [Aspose::Words::Drawing::Charts::AxisTickLabels::get_Spacing](./get_spacing/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo insertar un gráfico y modificar la apariencia de sus ejes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Borre la serie de datos de demostración del gráfico para comenzar con un gráfico limpio.
chart->get_Series()->Clear();

// Inserte una serie de gráfico con categorías para el eje X y los valores numéricos respectivos para el eje Y.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({640, 320, 280, 120, 150}));

// Los ejes del gráfico tienen varias opciones que pueden cambiar su apariencia,
// como su dirección, marcas de unidad mayor/menor y marcas de graduación.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> xAxis = chart->get_AxisX();
xAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Category);
xAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Minimum);
xAxis->set_ReverseOrder(false);
xAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
xAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
xAxis->set_MajorUnit(10.0);
xAxis->set_MinorUnit(15.0);
xAxis->get_TickLabels()->set_Offset(50);
xAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::Low);
xAxis->get_TickLabels()->set_IsAutoSpacing(false);
xAxis->set_TickMarkSpacing(1);

ASPOSE_ASSERT_EQ(doc, xAxis->get_Document());

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxis> yAxis = chart->get_AxisY();
yAxis->set_CategoryType(Aspose::Words::Drawing::Charts::AxisCategoryType::Automatic);
yAxis->set_Crosses(Aspose::Words::Drawing::Charts::AxisCrosses::Maximum);
yAxis->set_ReverseOrder(true);
yAxis->set_MajorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Inside);
yAxis->set_MinorTickMark(Aspose::Words::Drawing::Charts::AxisTickMark::Cross);
yAxis->set_MajorUnit(100.0);
yAxis->set_MinorUnit(20.0);
yAxis->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::NextToAxis);
yAxis->get_TickLabels()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
yAxis->get_TickLabels()->get_Font()->set_Color(System::Drawing::Color::get_Red());
yAxis->get_TickLabels()->set_Spacing(1);

// Los gráficos de columnas no tienen eje Z.
ASSERT_TRUE(System::TestTools::IsNull(chart->get_AxisZ()));

doc->Save(get_ArtifactsDir() + u"Charts.AxisProperties.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
