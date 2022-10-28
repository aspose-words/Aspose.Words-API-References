---
title: idx_get
second_title: Aspose.Words for C++ API Reference
description: Returns a ChartSeries at the specified index.
type: docs
weight: 53
url: /cpp/aspose.words.drawing.charts/chartseriescollection/idx_get/
---
## ChartSeriesCollection.idx_get method


Returns a [ChartSeries](../../chartseries/) at the specified index.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> Aspose::Words::Drawing::Charts::ChartSeriesCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | An index into the collection. |

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

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

