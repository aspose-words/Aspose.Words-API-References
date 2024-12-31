---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabelPosition enum. Specifies the position for a chart data label in C#.
type: docs
weight: 950
url: /net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Specifies the position for a chart data label.

```csharp
public enum ChartDataLabelPosition
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Center | `0` | Specifies that a data label should be displayed centered on a data marker. |
| Left | `1` | Specifies that a data label should be displayed to the left of a data marker. |
| Right | `2` | Specifies that a data label should be displayed to the right of a data marker. |
| Above | `3` | Specifies that a data label should be displayed above a data marker. |
| Below | `4` | Specifies that a data label should be displayed below a data marker. |
| InsideBase | `5` | Specifies that a data label should be displayed inside the base of a data marker. |
| InsideEnd | `6` | Specifies that a data label should be displayed inside the end of a data marker. |
| OutsideEnd | `7` | Specifies that a data label should be displayed outside the end of a data marker. |
| BestFit | `8` | Specifies that a data label should be displayed in the most appropriate position. |

## Remarks

Not all series types allow you to specify label positions. And those that do, do not support all values.

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

* namespace [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../)
