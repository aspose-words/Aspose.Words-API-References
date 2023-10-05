---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: ChartAxisTitle Text property. Gets or sets the text of the axis title. If null or empty value is specified auto generated title will be shown in C#.
type: docs
weight: 40
url: /net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Gets or sets the text of the axis title. If `null` or empty value is specified, auto generated title will be shown.

```csharp
public string Text { get; set; }
```

## Remarks

Use [`Show`](../show/) option if you need to show the title.

## Examples

Shows how to set chart axis title.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Delete default generated series.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisTitle = chart.AxisX.Title;
chartAxisTitle.Text = "Categories";
chartAxisTitle.Show = true;
chartAxisTitle.Text = "Values";
chartAxisTitle.Show = true;
chartAxisTitle.Overlay = true;
chartAxisTitle.Font.Size = 12;
chartAxisTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### See Also

* class [ChartAxisTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
