---
title: ChartDataLabel
second_title: Aspose.Words for C++ API Reference
description: Represents data label on a chart point or trendline. To learn more, visit the  documentation article.
type: docs
weight: 66
url: /cpp/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class


Represents data label on a chart point or trendline. To learn more, visit the [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) documentation article.

```cpp
class ChartDataLabel : public Aspose::Words::Drawing::Charts::Core::INumberFormatProvider,
                       public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties
```

## Methods

| Method | Description |
| --- | --- |
| [ClearFormat](./clearformat/)() | Clears format of this data label. The properties are set to the default values defined in the parent data label collection. |
| [get_Font](./get_font/)() | Provides access to the font formatting of this data label. |
| [get_Index](./get_index/)() | Specifies the index of the containing element. This index shall determine which of the parent's children collection this element applies to. Default value is 0. |
| [get_IsHidden](./get_ishidden/)() | Gets/sets a flag indicating whether this label is hidden. The default value is **false**. |
| [get_IsVisible](./get_isvisible/)() | Returns **true** if this data label has something to display. |
| [get_NumberFormat](./get_numberformat/)() | Returns number format of the parent element. |
| [get_Separator](./get_separator/)() | Gets or sets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead. |
| [get_ShowBubbleSize](./get_showbubblesize/)() | Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is **false**. |
| [get_ShowCategoryName](./get_showcategoryname/)() | Allows to specify if category name is to be displayed for the data labels on a chart. Default value is **false**. |
| [get_ShowDataLabelsRange](./get_showdatalabelsrange/)() | Allows to specify if values from data labels range to be displayed in the data labels. Default value is **false**. |
| [get_ShowLeaderLines](./get_showleaderlines/)() | Allows to specify if data label leader lines need be shown. Default value is **false**. |
| [get_ShowLegendKey](./get_showlegendkey/)() | Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is **false**. |
| [get_ShowPercentage](./get_showpercentage/)() | Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is **false**. |
| [get_ShowSeriesName](./get_showseriesname/)() | Returns or sets a Boolean to indicate the series name display behavior for the data labels on a chart. **true** to show the series name; **false** to hide. By default **false**. |
| [get_ShowValue](./get_showvalue/)() | Allows to specify if values are to be displayed in the data labels. Default value is **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsHidden](./set_ishidden/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_IsHidden](./get_ishidden/). |
| [set_Separator](./set_separator/)(const System::String\&) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_Separator](./get_separator/). |
| [set_ShowBubbleSize](./set_showbubblesize/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowBubbleSize](./get_showbubblesize/). |
| [set_ShowCategoryName](./set_showcategoryname/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowCategoryName](./get_showcategoryname/). |
| [set_ShowDataLabelsRange](./set_showdatalabelsrange/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowDataLabelsRange](./get_showdatalabelsrange/). |
| [set_ShowLeaderLines](./set_showleaderlines/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowLeaderLines](./get_showleaderlines/). |
| [set_ShowLegendKey](./set_showlegendkey/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowLegendKey](./get_showlegendkey/). |
| [set_ShowPercentage](./set_showpercentage/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowPercentage](./get_showpercentage/). |
| [set_ShowSeriesName](./set_showseriesname/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowSeriesName](./get_showseriesname/). |
| [set_ShowValue](./set_showvalue/)(bool) | Setter for [Aspose::Words::Drawing::Charts::ChartDataLabel::get_ShowValue](./get_showvalue/). |
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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words](../../)
