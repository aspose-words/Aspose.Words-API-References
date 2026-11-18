---
title: Aspose::Words::Drawing::Charts::ChartLegendEntry::set_IsHidden method
linktitle: set_IsHidden
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartLegendEntry::set_IsHidden method. Sets a value indicating whether this entry is hidden in the chart legend. The default value is false in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.drawing.charts/chartlegendentry/set_ishidden/
---
## ChartLegendEntry::set_IsHidden method


Sets a value indicating whether this entry is hidden in the chart legend. The default value is false.

```cpp
void Aspose::Words::Drawing::Charts::ChartLegendEntry::set_IsHidden(bool value)
```

## Remarks

 When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that is still displayed on the chart. 
## Examples


Shows how to work with a legend entry for chart series.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(ChartType::Column, static_cast<double>(432), static_cast<double>(252));

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();

auto categories = System::MakeArray<System::String>({u"AW Category 1", u"AW Category 2"});

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series1 = series->Add(u"Series 1", categories, System::MakeArray<double>({1, 2}));
series->Add(u"Series 2", categories, System::MakeArray<double>({3, 4}));
series->Add(u"Series 3", categories, System::MakeArray<double>({5, 6}));
series->Add(u"Series 4", categories, System::MakeArray<double>({0, 0}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartLegendEntryCollection> legendEntries = chart->get_Legend()->get_LegendEntries();
legendEntries->idx_get(3)->set_IsHidden(true);

doc->Save(get_ArtifactsDir() + u"Charts.LegendEntries.docx");
```
## See Also

* Class [ChartLegendEntry](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
