---
title: Aspose::Words::Drawing::Charts::ChartDataPoint class
linktitle: ChartDataPoint
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataPoint class. Allows to specify formatting of a single data point on the chart. To learn more, visit the  documentation article in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class


Allows to specify formatting of a single data point on the chart. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartDataPoint : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Clears format of this data point. The properties are set to the default values defined in the parent series. |
| [get_Bubble3D](./get_bubble3d/)() override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [get_Explosion](./get_explosion/)() override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of this data point. |
| [get_Index](./get_index/)() | Index of the data point this object applies formatting to. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [get_Marker](./get_marker/)() override | Specifies chart data marker. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [set_Explosion](./set_explosion/)(int32_t) override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| static [Type](./type/)() |  |

## Examples



Shows how to work with data points on a line chart. 
```cpp
void ChartDataPoint_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    SharedPtr<Shape> shape = builder->InsertChart(ChartType::Line, 500, 350);
    SharedPtr<Chart> chart = shape->get_Chart();

    ASSERT_EQ(3, chart->get_Series()->get_Count());
    ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
    ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
    ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

    // Emphasize the chart's data points by making them appear as diamond shapes.
    for (const auto& series : System::IterateOver(chart->get_Series()))
    {
        ApplyDataPoints(series, 4, MarkerSymbol::Diamond, 15);
    }

    // Smooth out the line that represents the first data series.
    chart->get_Series()->idx_get(0)->set_Smooth(true);

    // Verify that data points for the first series will not invert their colors if the value is negative.
    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<ChartDataPoint>>> enumerator =
            chart->get_Series()->idx_get(0)->get_DataPoints()->GetEnumerator();
        while (enumerator->MoveNext())
        {
            ASSERT_FALSE(enumerator->get_Current()->get_InvertIfNegative());
        }
    }

    // For a cleaner looking graph, we can clear format individually.
    chart->get_Series()->idx_get(1)->get_DataPoints()->idx_get(2)->ClearFormat();

    // We can also strip an entire series of data points at once.
    chart->get_Series()->idx_get(2)->get_DataPoints()->ClearFormat();

    doc->Save(ArtifactsDir + u"Charts.ChartDataPoint.docx");
}

static void ApplyDataPoints(SharedPtr<ChartSeries> series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        SharedPtr<ChartDataPoint> point = series->get_DataPoints()->idx_get(i);
        point->get_Marker()->set_Symbol(markerSymbol);
        point->get_Marker()->set_Size(dataPointSize);

        ASSERT_EQ(i, point->get_Index());
    }
}
```

## See Also

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
