---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: Aspose.Words for .NET
description: Explore the Aspose.Words.Drawing.Charts.ChartType enum to discover various chart types and enhance your document's data visualization effortlessly.
type: docs
weight: 1140
url: /net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Specifies type of a chart.

```csharp
public enum ChartType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Area | `0` | Area chart. |
| AreaStacked | `1` | Stacked Area chart. |
| AreaPercentStacked | `2` | 100% Stacked Area chart. |
| Area3D | `3` | 3D Area chart. |
| Area3DStacked | `4` | 3D Stacked Area chart. |
| Area3DPercentStacked | `5` | 3D 100% Stacked Area chart. |
| Bar | `6` | Bar chart. |
| BarStacked | `7` | Stacked Bar chart. |
| BarPercentStacked | `8` | 100% Stacked Bar chart. |
| Bar3D | `9` | 3D Bar chart. |
| Bar3DStacked | `10` | 3D Stacked Bar chart. |
| Bar3DPercentStacked | `11` | 3D 100% Stacked Bar chart. |
| Bubble | `12` | Bubble chart. |
| Bubble3D | `13` | 3D Bubble chart. |
| Column | `14` | Column chart. |
| ColumnStacked | `15` | Stacked Column chart. |
| ColumnPercentStacked | `16` | 100% Stacked Column chart. |
| Column3D | `17` | 3D Column chart. |
| Column3DStacked | `18` | 3D Stacked Column chart. |
| Column3DPercentStacked | `19` | 3D 100% Stacked Column chart. |
| Column3DClustered | `20` | 3D Clustered Column chart. |
| Doughnut | `21` | Doughnut chart. |
| Line | `22` | Line chart. |
| LineStacked | `23` | Stacked Line chart. |
| LinePercentStacked | `24` | 100% Stacked Line chart. |
| Line3D | `25` | 3D Line chart. |
| Pie | `26` | Pie chart. |
| Pie3D | `27` | 3D Pie chart. |
| PieOfBar | `28` | Pie of Bar chart. |
| PieOfPie | `29` | Pie of Pie chart. |
| Radar | `30` | Radar chart. |
| Scatter | `31` | Scatter chart. |
| Stock | `32` | Stock chart. |
| Surface | `33` | Surface chart. |
| Surface3D | `34` | 3D Surface chart. |
| Treemap | `35` | Treemap chart. |
| Sunburst | `36` | Sunburst chart. |
| Histogram | `37` | Histogram chart. |
| Pareto | `38` | Pareto chart. |
| BoxAndWhisker | `39` | Box and Whisker chart. |
| Waterfall | `40` | Waterfall chart. |
| Funnel | `41` | Funnel chart. |

## Examples

Shows how to create an appropriate type of chart series for a graph type.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // There are several ways of populating a chart's series collection.
    // Different series schemas are intended for different chart types.
    // 1 -  Column chart with columns grouped and banded along the X-axis by category:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insert two series of decimal values containing a value for each respective category.
    // This column chart will have three groups, each with two columns.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 -  Area chart with dates distributed along the X-axis:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insert a series with a decimal value for each respective date.
    // The dates will be distributed along a linear X-axis,
    // and the values added to this series will create data points.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 -  2D scatter plot:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Each series will need two decimal arrays of equal length.
    // The first array contains X-values, and the second contains corresponding Y-values
    // of data points on the chart's graph.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 -  Bubble chart:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Each series will need three decimal arrays of equal length.
    // The first array contains X-values, the second contains corresponding Y-values,
    // and the third contains diameters for each of the graph's data points.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### See Also

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
