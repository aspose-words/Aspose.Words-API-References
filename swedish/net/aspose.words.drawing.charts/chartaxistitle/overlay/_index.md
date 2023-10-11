---
title: ChartAxisTitle.Overlay
second_title: Aspose.Words för .NET API Referens
description: ChartAxisTitle fast egendom. Bestämmer om andra diagramelement ska tillåtas överlappa titeln. Standardvärdet ärfalsk .
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartaxistitle/overlay/
---
## ChartAxisTitle.Overlay property

Bestämmer om andra diagramelement ska tillåtas överlappa titeln. Standardvärdet är`falsk` .

```csharp
public bool Overlay { get; set; }
```

### Exempel

Visar hur man ställer in diagramaxelns titel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Ta bort standardgenererade serier.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Ställ in axeltitel.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Se även

* class [ChartAxisTitle](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* hopsättning [Aspose.Words](../../../)


