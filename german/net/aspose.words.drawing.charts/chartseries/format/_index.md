---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words für .NET
description: ChartSeries Format eigendom. Bietet Zugriff auf die Füll und Zeilenformatierung der Serie in C#.
type: docs
weight: 60
url: /de/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Bietet Zugriff auf die Füll- und Zeilenformatierung der Serie.

```csharp
public ChartFormat Format { get; }
```

## Beispiele

Hier erfahren Sie, wie Sie die Serienfarbe festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

// Kategorienamen-Array erstellen.
string[] categories = new[] { "Category 1", "Category 2" };

// Neue Serie hinzufügen. Wert- und Kategoriearrays müssen dieselbe Größe haben.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Serienfarbe festlegen.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Siehe auch

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
