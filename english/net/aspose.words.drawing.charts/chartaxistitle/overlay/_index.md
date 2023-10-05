---
title: ChartAxisTitle.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: Aspose.Words for .NET
description: ChartAxisTitle Overlay property. Determines whether other chart elements shall be allowed to overlap the title. The default value is false in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/chartaxistitle/overlay/
---
## ChartAxisTitle.Overlay property

Determines whether other chart elements shall be allowed to overlap the title. The default value is `false`.

```csharp
public bool Overlay { get; set; }
```

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
