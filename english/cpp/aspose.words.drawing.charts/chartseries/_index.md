---
title: Aspose::Words::Drawing::Charts::ChartSeries class
linktitle: ChartSeries
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartSeries class. Represents chart series properties. To learn more, visit the  documentation article in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class


Represents chart series properties. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartSeries : public Aspose::Words::Drawing::Charts::IChartDataPoint,
                    public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Adds the specified X and Y values to the chart series. |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Adds the specified X value, Y value and bubble size to the chart series. |
| [Clear](./clear/)() | Removes all data values from the chart series. Format of all individual data points and data labels is cleared. |
| [ClearValues](./clearvalues/)() | Removes all data values from the chart series with preserving the format of the data points and data labels. |
| [CopyFormatFrom](./copyformatfrom/)(int32_t) | Copies default data point format from the data point with the specified index. |
| [get_Bubble3D](./get_bubble3d/)() override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [get_BubbleSizes](./get_bubblesizes/)() | Gets a collection of bubble sizes for this chart series. |
| [get_DataLabels](./get_datalabels/)() | Specifies the settings for the data labels for the entire series. |
| [get_DataPoints](./get_datapoints/)() const | Returns a collection of formatting objects for all data points in this series. |
| [get_Explosion](./get_explosion/)() override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [get_Format](./get_format/)() | Provides access to fill and line formatting of the series. |
| [get_HasDataLabels](./get_hasdatalabels/)() const | Gets a flag indicating whether data labels are displayed for the series. |
| [get_InvertIfNegative](./get_invertifnegative/)() override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [get_LegendEntry](./get_legendentry/)() | Gets a legend entry for this chart series. |
| [get_Marker](./get_marker/)() override | Specifies a data marker. Marker is automatically created when requested. |
| [get_Name](./get_name/)() | Gets or sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index. |
| [get_SeriesType](./get_seriestype/)() | Gets the type of this chart series. |
| [get_Smooth](./get_smooth/)() const | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [get_XValues](./get_xvalues/)() | Gets a collection of X values for this chart series. |
| [get_YValues](./get_yvalues/)() | Gets a collection of Y values for this chart series. |
| [GetType](./gettype/)() const override |  |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&) | Inserts the specified X value into the chart series at the specified index. If the series supports Y values and bubble sizes, they will be empty for the X value. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&) | Inserts the specified X and Y values into the chart series at the specified index. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartXValue\>\&, const System::SharedPtr\<Aspose::Words::Drawing::Charts::ChartYValue\>\&, double) | Inserts the specified X value, Y value and bubble size into the chart series at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(int32_t) | Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. The corresponding data point and data label are also removed. |
| [set_Bubble3D](./set_bubble3d/)(bool) override | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [set_Explosion](./set_explosion/)(int32_t) override | Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts. |
| [set_HasDataLabels](./set_hasdatalabels/)(bool) | Sets a flag indicating whether data labels are displayed for the series. |
| [set_InvertIfNegative](./set_invertifnegative/)(bool) override | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartSeries::get_Name](./get_name/). |
| [set_Smooth](./set_smooth/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartSeries::get_Smooth](./get_smooth/). |
| static [Type](./type/)() |  |

## Examples



Shows how to apply labels to data points in a line chart. 
```cpp
void DataLabels()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    SharedPtr<Shape> chartShape = builder->InsertChart(ChartType::Line, 400, 300);
    SharedPtr<Chart> chart = chartShape->get_Chart();

    ASSERT_EQ(3, chart->get_Series()->get_Count());
    ASSERT_EQ(u"Series 1", chart->get_Series()->idx_get(0)->get_Name());
    ASSERT_EQ(u"Series 2", chart->get_Series()->idx_get(1)->get_Name());
    ASSERT_EQ(u"Series 3", chart->get_Series()->idx_get(2)->get_Name());

    // Apply data labels to every series in the chart.
    // These labels will appear next to each data point in the graph and display its value.
    for (const auto& series : System::IterateOver(chart->get_Series()))
    {
        ApplyDataLabels(series, 4, u"000.0", u", ");
        ASSERT_EQ(4, series->get_DataLabels()->get_Count());
    }

    // Change the separator string for every data label in a series.
    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<ChartDataLabel>>> enumerator =
            chart->get_Series()->idx_get(0)->get_DataLabels()->GetEnumerator();
        while (enumerator->MoveNext())
        {
            ASSERT_EQ(u", ", enumerator->get_Current()->get_Separator());
            enumerator->get_Current()->set_Separator(u" & ");
        }
    }

    // For a cleaner looking graph, we can remove data labels individually.
    chart->get_Series()->idx_get(1)->get_DataLabels()->idx_get(2)->ClearFormat();

    // We can also strip an entire series of its data labels at once.
    chart->get_Series()->idx_get(2)->get_DataLabels()->ClearFormat();

    doc->Save(ArtifactsDir + u"Charts.DataLabels.docx");
}

static void ApplyDataLabels(SharedPtr<ChartSeries> series, int labelsCount, String numberFormat, String separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series->set_HasDataLabels(true);

        ASSERT_FALSE(series->get_DataLabels()->idx_get(i)->get_IsVisible());

        series->get_DataLabels()->idx_get(i)->set_ShowCategoryName(true);
        series->get_DataLabels()->idx_get(i)->set_ShowSeriesName(true);
        series->get_DataLabels()->idx_get(i)->set_ShowValue(true);
        series->get_DataLabels()->idx_get(i)->set_ShowLeaderLines(true);
        series->get_DataLabels()->idx_get(i)->set_ShowLegendKey(true);
        series->get_DataLabels()->idx_get(i)->set_ShowPercentage(false);
        series->get_DataLabels()->idx_get(i)->set_IsHidden(false);
        ASSERT_FALSE(series->get_DataLabels()->idx_get(i)->get_ShowDataLabelsRange());

        series->get_DataLabels()->idx_get(i)->get_NumberFormat()->set_FormatCode(numberFormat);
        series->get_DataLabels()->idx_get(i)->set_Separator(separator);

        ASSERT_FALSE(series->get_DataLabels()->idx_get(i)->get_ShowDataLabelsRange());
        ASSERT_TRUE(series->get_DataLabels()->idx_get(i)->get_IsVisible());
        ASSERT_FALSE(series->get_DataLabels()->idx_get(i)->get_IsHidden());
    }
}
```

## See Also

* Interface [IChartDataPoint](../ichartdatapoint/)
* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
