---
title: ChartAxisTitle.Overlay
second_title: Aspose.Words für .NET-API-Referenz
description: ChartAxisTitle eigendom. Legt fest ob andere Diagrammelemente den Titel überlappen dürfen. Der Standardwert istFALSCH .
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartaxistitle/overlay/
---
## ChartAxisTitle.Overlay property

Legt fest, ob andere Diagrammelemente den Titel überlappen dürfen. Der Standardwert ist`FALSCH` .

```csharp
public bool Overlay { get; set; }
```

### Beispiele

Zeigt, wie der Titel der Diagrammachse festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Achsentitel festlegen.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Siehe auch

* class [ChartAxisTitle](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* Montage [Aspose.Words](../../../)


