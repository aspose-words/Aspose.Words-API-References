---
title: Chart.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words für .NET
description: Schalten Sie mit unserem Tool erweiterte Diagrammformatierungen frei! Passen Sie Füll- und Linienstile einfach an und erhalten Sie beeindruckende, professionelle Grafiken, die Ihre Datenpräsentation verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.drawing.charts/chart/format/
---
## Chart.Format property

Bietet Zugriff auf die Füll- und Linienformatierung des Diagramms.

```csharp
public ChartFormat Format { get; }
```

## Beispiele

Zeigt, wie die Diagrammformatierung verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Diagrammhintergrund formatieren.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Achsenmarkierungsbeschriftungen ausblenden.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Diagrammtitel formatieren.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Achsentitel formatieren.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Legende formatieren.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Siehe auch

* class [ChartFormat](../../chartformat/)
* class [Chart](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
