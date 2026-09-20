---
title: "Aspose::Words::Drawing::Charts::ChartDataTable clase"
linktitle: "ChartDataTable"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Drawing::Charts::ChartDataTable. Permite especificar propiedades de una tabla de datos de gráfico en C++."
type: docs
weight: 9500
url: /es/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Permite especificar las propiedades de una tabla de datos del gráfico.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_Font](./get_font/)() | Proporciona acceso al formato de fuente de la tabla de datos. |
| [get_Format](./get_format/)() | Proporciona acceso al relleno del fondo de texto y al formato de borde de la tabla de datos. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Obtiene o establece una bandera que indica si se muestra un borde horizontal de la tabla de datos. El valor predeterminado es **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Obtiene o establece una bandera que indica si se muestran las claves de leyenda en la tabla de datos. El valor predeterminado es **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Obtiene o establece una bandera que indica si se muestra un borde de contorno, es decir, un borde alrededor de los nombres de series y categorías. El valor predeterminado es **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Obtiene o establece una bandera que indica si se muestra un borde vertical de la tabla de datos. El valor predeterminado es **true**. |
| [get_Show](./get_show/)() const | Obtiene o establece una bandera que indica si la tabla de datos se mostrará para el gráfico. El valor predeterminado es **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Método set para [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo mostrar la tabla de datos con los datos de series del gráfico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## Ver también

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
