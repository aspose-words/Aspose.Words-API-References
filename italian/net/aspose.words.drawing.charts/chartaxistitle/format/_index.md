---
title: ChartAxisTitle.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxisTitle Format per personalizzare facilmente il riempimento del titolo dell'asse e gli stili delle linee, migliorando la visualizzazione dei dati.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartaxistitle/format/
---
## ChartAxisTitle.Format property

Fornisce accesso al riempimento e alla formattazione della linea del titolo dell'asse.

```csharp
public ChartFormat Format { get; }
```

## Esempi

Mostra come utilizzare la formattazione dei grafici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Elimina le serie generate di default.
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// Formatta lo sfondo del grafico.
chart.Format.Fill.Solid(Color.DarkSlateGray);

// Nascondi le etichette delle tacche degli assi.
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// Formatta il titolo del grafico.
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatta il titolo dell'asse.
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// Formatta la legenda.
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### Guarda anche

* class [ChartFormat](../../chartformat/)
* class [ChartAxisTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
