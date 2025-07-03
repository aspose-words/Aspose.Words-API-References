---
title: Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode method
linktitle: get_LeftMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode method. Gets or sets the interpretation mode of the Left property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its Position property in C++.'
type: docs
weight: 6667
url: /cpp/aspose.words.drawing.charts/chartdatalabel/get_leftmode/
---
## ChartDataLabel::get_LeftMode method


Gets or sets the interpretation mode of the [Left](../get_left/) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [Position](../get_position/) property.

```cpp
Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode Aspose::Words::Drawing::Charts::ChartDataLabel::get_LeftMode()
```


## Examples



Shows how to place data labels of doughnut chart outside doughnut. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const int32_t chartWidth = 432;
const int32_t chartHeight = 252;
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, chartWidth, chartHeight);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> seriesColl = chart->get_Series();
// Delete default generated series.
seriesColl->Clear();

// Hide the legend.
chart->get_Legend()->set_Position(Aspose::Words::Drawing::Charts::LegendPosition::None);

// Generate data.
const int32_t dataLength = 20;
double totalValue = 0;
auto categories = System::MakeArray<System::String>(dataLength);
auto values = System::MakeArray<double>(dataLength, 0);

for (int32_t i = 0; i < dataLength; i++)
{
    categories[i] = System::String::Format(u"Category {0}", i);
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = seriesColl->Add(u"Series 1", categories, values);
series->set_HasDataLabels(true);

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->set_ShowLeaderLines(true);

// The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
// properties around a circle outside of the chart doughnut.
// The origin is in the upper left corner of the chart.

const double titleAreaHeight = 25.5;
// This can be calculated using title text and font.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2.0;
const double labelHeight = 16.5;
// This can be calculated using label font.
const double oneCharLabelWidth = 12.75;
// This can be calculated for each label using its text and font.
const double twoCharLabelWidth = 17.25;
// This can be calculated for each label using its text and font.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Because the data points start at the top, the X coordinates used in the Left and Top properties of
// the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
double totalAngle = -System::Math::PI / 2;
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> previousLabel;

for (int32_t i = 0; i < series->get_YValues()->get_Count(); i++)
{
    System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabel> dataLabel = dataLabels->idx_get(i);

    double value = series->get_YValues()->idx_get(i)->get_DoubleValue();
    double labelWidth;
    if (value < 10)
    {
        labelWidth = oneCharLabelWidth;
    }
    else
    {
        labelWidth = twoCharLabelWidth;
    }
    double labelSegmentAngle = value / totalValue * 2 * System::Math::PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System::Math::Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System::Math::Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // If the current data label overlaps other labels, move it horizontally.
    if ((previousLabel != nullptr) && (System::Math::Abs(previousLabel->get_Top() - labelTop) < labelHeight) && (System::Math::Abs(previousLabel->get_Left() - labelLeft) < labelWidth))
    {
        // Move right on the top, left on the bottom.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System::Math::PI);
        int32_t factor;
        if (isOnTop)
        {
            factor = 1;
        }
        else
        {
            factor = -1;
        }

        labelLeft = previousLabel->get_Left() + labelWidth * factor + labelMargin;
    }

    dataLabel->set_Left(labelLeft);
    dataLabel->set_LeftMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);
    dataLabel->set_Top(labelTop);
    dataLabel->set_TopMode(Aspose::Words::Drawing::Charts::ChartDataLabelLocationMode::Absolute);

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChartLabelPosition.docx");
```

## See Also

* Enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* Class [ChartDataLabel](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
