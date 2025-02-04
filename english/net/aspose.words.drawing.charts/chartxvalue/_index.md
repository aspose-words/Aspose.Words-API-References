---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartXValue class. Represents an X value for a chart series in C#.
type: docs
weight: 1150
url: /net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Represents an X value for a chart series.

```csharp
public class ChartXValue
```

## Properties

| Name | Description |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Gets the stored datetime value. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Gets the stored numeric value. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Gets the stored multilevel value. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Gets the stored string value. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Gets the stored time value. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Gets the type of the X value stored in the object. |

## Methods

| Name | Description |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Creates a `ChartXValue` instance of the DateTime type. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Creates a `ChartXValue` instance of the Double type. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Creates a `ChartXValue` instance of the Multilevel type. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Creates a `ChartXValue` instance of the String type. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Creates a `ChartXValue` instance of the Time type. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Gets a flag indicating whether the specified object is equal to the current X value object. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Gets a hash code for the current X value object. |

## Remarks

This class contains a number of static methods for creating an X value of a particular type. The [`ValueType`](./valuetype/) property allows you to determine the type of an existing X value.

All non-null X values of a chart series must be of the same [`ChartXValueType`](../chartxvaluetype/) type.

## Examples

Shows how to populate chart series with data.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Clear X and Y values of the first series.
series1.ClearValues();

// Populate the series with data.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Clear X and Y values of the second series.
series2.Clear();

// Populate the series with data.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
