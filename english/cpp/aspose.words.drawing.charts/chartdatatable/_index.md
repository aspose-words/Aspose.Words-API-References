---
title: Aspose::Words::Drawing::Charts::ChartDataTable class
linktitle: ChartDataTable
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataTable class. Allows to specify properties of a chart data table in C++.'
type: docs
weight: 9500
url: /cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Allows to specify properties of a chart data table.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [get_Font](./get_font/)() | Provides access to font formatting of the data table. |
| [get_Format](./get_format/)() | Provides access to fill of text background and border formatting of the data table. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Gets or sets a flag indicating whether a horizontal border of the data table is displayed. The default value is **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Gets or sets a flag indicating whether legend keys are displayed in the data table. The default value is **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Gets or sets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. The default value is **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Gets or sets a flag indicating whether a vertical border of the data table is displayed. The default value is **true**. |
| [get_Show](./get_show/)() const | Gets or sets a flag indicating whether the data table will be shown for the chart. Default value is **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## Examples



Shows how to show data table with chart series data. 
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

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
