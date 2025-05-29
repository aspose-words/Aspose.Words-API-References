---
title: ChartTitle.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words per .NET
description: Esplora la proprietà Formato ChartTitle per uno stile di riempimento e linea migliorato, che conferisce ai tuoi grafici un aspetto professionale e curato.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/charttitle/format/
---
## ChartTitle.Format property

Fornisce accesso al riempimento e alla formattazione delle linee del titolo del grafico.

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
* class [ChartTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
