---
title: Aspose::Words::Drawing::Charts::ChartDataPoint::get_IsTotal method
linktitle: get_IsTotal
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataPoint::get_IsTotal method. Gets a flag indicating whether the data point is a total. Applies only to Waterfall charts in C++.'
type: docs
weight: 7500
url: /cpp/aspose.words.drawing.charts/chartdatapoint/get_istotal/
---
## ChartDataPoint::get_IsTotal method


Gets a flag indicating whether the data point is a total. Applies only to Waterfall charts.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataPoint::get_IsTotal()
```

## Remarks

 In a waterfall chart, total columns represent intermediate or final totals. If this property returns true, the data point is such a total column. 
## Examples


Shows how to determine whether a data point is a total in a waterfall chart.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a Waterfall chart.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(ChartType::Waterfall, static_cast<double>(450), static_cast<double>(450));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Title()->set_Text(u"New Zealand GDP");

// Delete default generated series.
chart->get_Series()->Clear();

// Add a series where the start value, the subtotal and the final value are totals.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"New Zealand GDP", System::MakeArray<System::String>({u"2018", u"2019 growth", u"2020 growth", u"2020", u"2021 growth", u"2022 growth", u"2022"}), System::MakeArray<double>({100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62}), System::MakeArray<bool>({true, false, false, true, false, false, true}));

// Print the type of each data point.
for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    if (series->IsTotal(i))
    {
        std::cout << System::String::Format(u"Data point {0} is Subtotal", i) << std::endl;
    }
    else if (series->get_YValues()->idx_get(i)->get_DoubleValue() > 0)
    {
        std::cout << System::String::Format(u"Data point {0} is Increase", i) << std::endl;
    }
    else
    {
        std::cout << System::String::Format(u"Data point {0} is Decrease", i) << std::endl;
    }
}

// The same flag is available on the data point itself.
std::cout << System::String::Format(u"Data point 3 is total: {0}", series->get_DataPoints()->idx_get(3)->get_IsTotal()) << std::endl;

doc->Save(get_ArtifactsDir() + u"Charts.ChartSeriesAndDataPointIsTotal.docx");
```
## See Also

* Class [ChartDataPoint](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
