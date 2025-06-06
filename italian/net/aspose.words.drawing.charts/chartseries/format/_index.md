---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartSeries Format per accedere senza sforzo a stili di riempimento e linea personalizzabili, migliorando la tua esperienza di visualizzazione dei dati.
type: docs
weight: 60
url: /it/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Fornisce accesso al riempimento e alla formattazione delle linee della serie.

```csharp
public ChartFormat Format { get; }
```

## Esempi

Seminare come impostare il colore della serie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Elimina la serie generata di default.
seriesColl.Clear();

// Crea un array di nomi di categoria.
string[] categories = new[] { "Category 1", "Category 2" };

// Aggiunta di nuove serie. Gli array di valori e categorie devono avere le stesse dimensioni.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Imposta il colore della serie.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Guarda anche

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
