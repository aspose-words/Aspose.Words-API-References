---
title: ChartAxisTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: ChartAxisTitle Font property. Provides access to the font formatting of the axis title in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing.charts/chartaxistitle/font/
---
## ChartAxisTitle.Font property

Provides access to the font formatting of the axis title.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartAxisTitle](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
