---
title: "Aspose::Words::Drawing::Charts::Chart clase"
linktitle: "Gráfico"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::Charts::Chart clase. Proporciona acceso a las propiedades de la forma del gráfico. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Proporciona acceso a las propiedades de la forma del gráfico. Para obtener más información, visite el artículo de documentación [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Axes](./get_axes/)() | Obtiene una colección de todos los ejes de este gráfico. |
| [get_AxisX](./get_axisx/)() | Proporciona acceso a las propiedades del eje X principal del gráfico. |
| [get_AxisY](./get_axisy/)() | Proporciona acceso a las propiedades del eje Y principal del gráfico. |
| [get_AxisZ](./get_axisz/)() | Proporciona acceso a las propiedades del eje Z del gráfico. |
| [get_DataTable](./get_datatable/)() | Proporciona acceso a las propiedades de una tabla de datos de este gráfico. La tabla de datos puede mostrarse usando la propiedad [Show](../chartdatatable/get_show/). |
| [get_Format](./get_format/)() | Proporciona acceso al formato de relleno y de línea del gráfico. |
| [get_Legend](./get_legend/)() | Proporciona acceso a las propiedades de la leyenda del gráfico. |
| [get_Series](./get_series/)() | Proporciona acceso a la colección de series. |
| [get_SeriesGroups](./get_seriesgroups/)() | Proporciona acceso a una colección de grupos de series de este gráfico. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtiene la ruta y el nombre de un archivo xls/xlsx al que está vinculado este gráfico. |
| [get_Style](./get_style/)() | Obtiene el estilo del gráfico. |
| [get_Title](./get_title/)() | Proporciona acceso a las propiedades del título del gráfico. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Establecedor para [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Establece el estilo del gráfico. |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo insertar un gráfico y establecer un título.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta una forma de gráfico con un DocumentBuilder y obtén su gráfico.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Utiliza la propiedad "Title" para dar a nuestro gráfico un título, que aparece en la parte superior central del área del gráfico.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Establece la propiedad "Show" a "true" para que el título sea visible.
title->set_Show(true);

// Establece la propiedad "Overlay" a "true". Da más espacio a otros elementos del gráfico permitiendo que se superpongan al título.
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
