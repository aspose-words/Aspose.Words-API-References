---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
articleTitle: ChartXValueCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartXValueCollection class. Represents a collection of X values for a chart series in C#.
type: docs
weight: 1160
url: /net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Represents a collection of X values for a chart series.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Properties

| Name | Description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Gets the number of items in this collection. |
| [FormatCode](../../aspose.words.drawing.charts/chartxvaluecollection/formatcode/) { get; set; } | Gets or sets the format code applied to the X values. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Gets or sets the X value at the specified index. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Returns an enumerator object. |

## Remarks

All items of the collection other than **null** must have the same [`ValueType`](../chartxvalue/valuetype/).

The collection allows only changing X values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [`ChartSeries`](../chartseries/) class can be used.

## Examples

Shows how to get chart series data.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Clear individual format of all data points.
    // Data points and data values are one-to-one in column charts.
    series.DataPoints[i].ClearFormat();

    // Get Y value.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Change colors of the max and min values.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### See Also

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
