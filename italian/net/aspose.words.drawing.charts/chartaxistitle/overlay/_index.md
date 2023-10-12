---
title: ChartAxisTitle.Overlay
second_title: Aspose.Words per .NET API Reference
description: ChartAxisTitle proprietà. Determina se altri elementi del grafico possono sovrapporsi al titolo. Il valore predefinito èfalso .
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartaxistitle/overlay/
---
## ChartAxisTitle.Overlay property

Determina se altri elementi del grafico possono sovrapporsi al titolo. Il valore predefinito è`falso` .

```csharp
public bool Overlay { get; set; }
```

### Esempi

Mostra come impostare il titolo dell'asse del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Elimina le serie generate predefinite.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// Imposta il titolo dell'asse.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Guarda anche

* class [ChartAxisTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartaxistitle/)
* assemblea [Aspose.Words](../../../)


