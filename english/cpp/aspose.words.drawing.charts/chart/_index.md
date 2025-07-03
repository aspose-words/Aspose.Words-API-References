---
title: Aspose::Words::Drawing::Charts::Chart class
linktitle: Chart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::Chart class. Provides access to the chart shape properties. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.drawing.charts/chart/
---
## Chart class


Provides access to the chart shape properties. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class Chart : public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_Axes](./get_axes/)() | Gets a collection of all axes of this chart. |
| [get_AxisX](./get_axisx/)() | Provides access to properties of the primary X axis of the chart. |
| [get_AxisY](./get_axisy/)() | Provides access to properties of the primary Y axis of the chart. |
| [get_AxisZ](./get_axisz/)() | Provides access to properties of the Z axis of the chart. |
| [get_DataTable](./get_datatable/)() | Provides access to properties of a data table of this chart. The data table can be shown using the [Show](../chartdatatable/get_show/) property. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of the chart. |
| [get_Legend](./get_legend/)() | Provides access to the chart legend properties. |
| [get_Series](./get_series/)() | Provides access to series collection. |
| [get_SeriesGroups](./get_seriesgroups/)() | Provides access to a series group collection of this chart. |
| [get_SourceFullName](./get_sourcefullname/)() | Gets the path and name of an xls/xlsx file this chart is linked to. |
| [get_Style](./get_style/)() | Gets the style of the chart. |
| [get_Title](./get_title/)() | Provides access to the chart title properties. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::Chart::get_SourceFullName](./get_sourcefullname/). |
| [set_Style](./set_style/)(Aspose::Words::Drawing::Charts::ChartStyle) | Sets the style of the chart. |
| static [Type](./type/)() |  |

## Examples



Shows how to insert a chart and set a title. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a chart shape with a document builder and get its chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bar, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartTitle> title = chart->get_Title();
title->set_Text(u"My Chart");
title->get_Font()->set_Size(15);
title->get_Font()->set_Color(System::Drawing::Color::get_Blue());

// Set the "Show" property to "true" to make the title visible.
title->set_Show(true);

// Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
title->set_Overlay(true);

doc->Save(get_ArtifactsDir() + u"Charts.ChartTitle.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
