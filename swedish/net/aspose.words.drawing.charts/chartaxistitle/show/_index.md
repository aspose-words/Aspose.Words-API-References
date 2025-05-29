---
title: ChartAxisTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartAxisTitle Show för att kontrollera synligheten av axelrubriker. Förbättra dina diagram med tydliga, informativa titlar för bättre datainsikter.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

Avgör om titeln ska visas för axeln. Standardvärdet är`falsk` .

```csharp
public bool Show { get; set; }
```

## Exempel

Visar hur man ställer in diagramaxelns titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Radera standardgenererad serie.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Se även

* class [ChartAxisTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
