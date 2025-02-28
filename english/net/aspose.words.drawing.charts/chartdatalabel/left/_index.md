---
title: ChartDataLabel.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words for .NET
description: Adjust the ChartDataLabel Left property to control data label positioning on your chart. Enhance clarity and presentation with precise distance settings.
type: docs
weight: 60
url: /net/aspose.words.drawing.charts/chartdatalabel/left/
---
## ChartDataLabel.Left property

Gets or sets the distance of the data label in points from the left edge of the chart or from the position specified by its [`Position`](../position/) property, depending on the value of the [`LeftMode`](../leftmode/) property.

```csharp
public double Left { get; set; }
```

## Remarks

The value of the property changes proportionally if the chart shape is resized.

The property cannot be set in a Word 2016 chart.

## Examples

Shows how to place data labels of doughnut chart outside doughnut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Delete default generated series.
seriesColl.Clear();

// Hide the legend.
chart.Legend.Position = LegendPosition.None;

// Generate data.
const int dataLength = 20;
double totalValue = 0;
string[] categories = new string[dataLength];
double[] values = new double[dataLength];

for (int i = 0; i < dataLength; i++)
{
    categories[i] = $"Category {i}";
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

ChartSeries series = seriesColl.Add("Series 1", categories, values);
series.HasDataLabels = true;

ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.ShowLeaderLines = true;

// The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
// properties around a circle outside of the chart doughnut.
// The origin is in the upper left corner of the chart.

const double titleAreaHeight = 25.5; // This can be calculated using title text and font.
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // This can be calculated using label font.
const double oneCharLabelWidth = 12.75; // This can be calculated for each label using its text and font.
const double twoCharLabelWidth = 17.25; // This can be calculated for each label using its text and font.
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// Because the data points start at the top, the X coordinates used in the Left and Top properties of
// the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
double totalAngle = -System.Math.PI / 2;
ChartDataLabel previousLabel = null;

for (int i = 0; i < series.YValues.Count; i++)
{
    ChartDataLabel dataLabel = dataLabels[i];

    double value = series.YValues[i].DoubleValue;
    double labelWidth;
    if (value < 10)
        labelWidth = oneCharLabelWidth;
    else
        labelWidth = twoCharLabelWidth;
    double labelSegmentAngle = value / totalValue * 2 * System.Math.PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System.Math.Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System.Math.Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // If the current data label overlaps other labels, move it horizontally.
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // Move right on the top, left on the bottom.
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System.Math.PI);
        int factor;
        if (isOnTop)
            factor = 1;
        else
            factor = -1;

        labelLeft = previousLabel.Left + labelWidth * factor + labelMargin;
    }

    dataLabel.Left = labelLeft;
    dataLabel.LeftMode = ChartDataLabelLocationMode.Absolute;
    dataLabel.Top = labelTop;
    dataLabel.TopMode = ChartDataLabelLocationMode.Absolute;

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc.Save(ArtifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### See Also

* class [ChartDataLabel](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
