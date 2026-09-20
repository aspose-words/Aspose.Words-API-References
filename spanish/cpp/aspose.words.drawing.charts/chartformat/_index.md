---
title: "Aspose::Words::Drawing::Charts::ChartFormat clase"
linktitle: "ChartFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::ChartFormat clase. Representa el formato de un elemento de gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class


Representa el formato de un elemento del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class ChartFormat : public Aspose::Words::Drawing::Core::IFillable,
                    public Aspose::Words::Drawing::Core::IStrokable
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Fill](./get_fill/)() | Obtiene el formato de relleno del elemento de gráfico principal. |
| [get_IsDefined](./get_isdefined/)() | Obtiene una bandera que indica si se ha definido algún formato. |
| [get_ShapeType](./get_shapetype/)() | Obtiene o establece el tipo de forma del elemento de gráfico principal. |
| [get_Stroke](./get_stroke/)() | Obtiene el formato de línea del elemento de gráfico principal. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ShapeType](./set_shapetype/)(Aspose::Words::Drawing::Charts::ChartShapeType) | Método setter para [Aspose::Words::Drawing::Charts::ChartFormat::get_ShapeType](./get_shapetype/). |
| [SetDefaultFill](./setdefaultfill/)() | Restablece el relleno del elemento de gráfico al valor predeterminado. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo usar el formateo de gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Eliminar series generadas por defecto.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2"});
series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));

// Formatear el fondo del gráfico.
chart->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_DarkSlateGray());

// Ocultar etiquetas de marcas del eje.
chart->get_AxisX()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);
chart->get_AxisY()->get_TickLabels()->set_Position(Aspose::Words::Drawing::Charts::AxisTickLabelPosition::None);

// Formatear el título del gráfico.
chart->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatear el título del eje.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

// Formatear la leyenda.
chart->get_Legend()->get_Format()->get_Fill()->Solid(System::Drawing::Color::get_LightGoldenrodYellow());

doc->Save(get_ArtifactsDir() + u"Charts.ChartFormat.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
