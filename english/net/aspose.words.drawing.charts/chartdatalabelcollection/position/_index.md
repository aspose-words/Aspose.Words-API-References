---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: Discover the ChartDataLabelCollection Position property to easily customize your data label positions for enhanced data visualization and clarity.
type: docs
weight: 70
url: /net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

Gets or sets the position of the data labels.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Remarks

The position can be set for data labels of the following chart series types:

- Bar, Column, Histogram, Pareto, Waterfall; allowed values: Center, InsideBase, InsideEnd and OutsideEnd;

- BarStacked, BarPercentStacked, ColumnStacked, ColumnPercentStacked; allowed values: Center, InsideBase and InsideEnd;

- Bubble, Bubble3D, Line, LineStacked, LinePercentStacked, Scatter, Stock; allowed values: Center, Left, Right, Above and Below;

- Pie, Pie3D, PieOfBar, PieOfPie; allowed values: Center, InsideEnd, OutsideEnd and BestFit;

- BoxAndWhisker; allowed values: Left, Right, Above and Below.

## Examples

Shows how to set the position of the data label.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert column chart.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Delete default generated series.
seriesColl.Clear();

// Add series.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Show data labels and set font color.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Set data label position.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### See Also

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
