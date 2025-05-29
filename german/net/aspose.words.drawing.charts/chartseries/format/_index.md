---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartSeries-Formateigenschaft für mühelosen Zugriff auf anpassbare Füll- und Linienstile und verbessern Sie so Ihr Datenvisualisierungserlebnis.
type: docs
weight: 60
url: /de/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Bietet Zugriff auf die Füll- und Linienformatierung der Serie.

```csharp
public ChartFormat Format { get; }
```

## Beispiele

Zeigt, wie die Serienfarbe eingestellt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Standardmäßig generierte Serien löschen.
seriesColl.Clear();

// Array mit Kategorienamen erstellen.
string[] categories = new[] { "Category 1", "Category 2" };

// Neue Serie hinzufügen. Werte- und Kategorie-Arrays müssen dieselbe Größe haben.
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
