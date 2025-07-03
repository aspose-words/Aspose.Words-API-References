---
title: Aspose::Words::Drawing::Charts::ChartDataTable::get_Show method
linktitle: get_Show
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataTable::get_Show method. Gets or sets a flag indicating whether the data table will be shown for the chart. Default value is false in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/chartdatatable/get_show/
---
## ChartDataTable::get_Show method


Gets or sets a flag indicating whether the data table will be shown for the chart. Default value is **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataTable::get_Show() const
```


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

* Class [ChartDataTable](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
