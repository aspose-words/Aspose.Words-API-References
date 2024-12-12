---
title: Aspose::Words::Drawing::Charts::ChartSeriesCollection class
linktitle: ChartSeriesCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeriesCollection class. Represents collection of a ChartSeries. To learn more, visit the  documentation article in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class


Represents collection of a [ChartSeries](../chartseries/). To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartSeriesCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Scatter charts. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::DateTime\>\&, const System::ArrayPtr\<double\>\&) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<double\>\&) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to any type of Bubble charts. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartMultilevelValue\>\>\&, const System::ArrayPtr\<double\>\&) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series that have multi-level data categories. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<double\>\&) | Adds new [ChartSeries](../chartseries/) to this collection. Use this method to add series to Histogram charts. |
| [Add](./add/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<double\>\&, const System::ArrayPtr\<bool\>\&) |  |
| [Clear](./clear/)() | Removes all [ChartSeries](../chartseries/) from this collection. |
| [get_Count](./get_count/)() | Returns the number of [ChartSeries](../chartseries/) in this collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Returns a [ChartSeries](../chartseries/) at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Removes a [ChartSeries](../chartseries/) at the specified index. |
| static [Type](./type/)() |  |

## Examples



Shows how to add and remove series data in a chart. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a column chart that will contain three series of demo data by default.
SharedPtr<Shape> chartShape = builder->InsertChart(ChartType::Column, 400, 300);
SharedPtr<Chart> chart = chartShape->get_Chart();

// Each series has four decimal values: one for each of the four categories.
// Four clusters of three columns will represent this data.
SharedPtr<ChartSeriesCollection> chartData = chart->get_Series();

ASSERT_EQ(3, chartData->get_Count());

// Print the name of every series in the chart.
{
    SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<ChartSeries>>> enumerator = chart->get_Series()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current()->get_Name() << std::endl;
    }
}

// These are the names of the categories in the chart.
ArrayPtr<String> categories = MakeArray<String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});

// We can add a series with new values for existing categories.
// This chart will now contain four clusters of four columns.
chart->get_Series()->Add(u"Series 4", categories, MakeArray<double>({4.4, 7.0, 3.5, 2.1}));

// A chart series can also be removed by index, like this.
// This will remove one of the three demo series that came with the chart.
chartData->RemoveAt(2);

ASSERT_FALSE(chartData->LINQ_Any([](SharedPtr<ChartSeries> s) { return s->get_Name() == u"Series 3"; }));

// We can also clear all the chart's data at once with this method.
// When creating a new chart, this is the way to wipe all the demo data
// before we can begin working on a blank chart.
chartData->Clear();
```

## See Also

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
