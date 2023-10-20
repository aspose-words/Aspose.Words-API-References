---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: ChartAxisTitle Text proprietà. Ottiene o imposta il testo del titolo dellasse. Ifnullo o viene specificato un valore vuoto verrà mostrato il titolo generato automaticamente in C#.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Ottiene o imposta il testo del titolo dell'asse. If`nullo` o viene specificato un valore vuoto, verrà mostrato il titolo generato automaticamente.

```csharp
public string Text { get; set; }
```

## Osservazioni

Utilizzo[`Show`](../show/) opzione se è necessario mostrare il titolo.

## Esempi

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
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
