---
title: ChartSeries.Format
second_title: Aspose.Words für .NET-API-Referenz
description: ChartSeries eigendom. Bietet Zugriff auf die Füll und Zeilenformatierung der Serie.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Bietet Zugriff auf die Füll- und Zeilenformatierung der Serie.

```csharp
public ChartFormat Format { get; }
```

### Beispiele

Sauen, wie man Serienfarbe einstellt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Standardmäßig generierte Serie löschen.
seriesColl.Clear();

// Kategorienamen-Array erstellen.
string[] categories = new[] { "Category 1", "Category 2" };

// Neue Serie hinzufügen. Wert- und Kategoriearrays müssen dieselbe Größe haben.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Serienfarbe setzen.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Siehe auch

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../chartseries/)
* Montage [Aspose.Words](../../../)


