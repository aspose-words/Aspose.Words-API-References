---
title: get_ShowCategoryName
second_title: Aspose.Words for C++ API Reference
description: Allows to specify if category name is to be displayed for the data labels on a chart. Default value is false.
type: docs
weight: 92
url: /cpp/aspose.words.drawing.charts/chartdatalabel/get_showcategoryname/
---
## ChartDataLabel.get_ShowCategoryName method


Allows to specify if category name is to be displayed for the data labels on a chart. Default value is false.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowCategoryName()
```


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

