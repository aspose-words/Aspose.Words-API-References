---
title: ChartAxisTitle.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxisTitle Text per personalizzare facilmente i titoli degli assi. Imposta o ottieni titoli dinamici per una visualizzazione dei dati migliorata.
type: docs
weight: 50
url: /it/net/aspose.words.drawing.charts/chartaxistitle/text/
---
## ChartAxisTitle.Text property

Ottiene o imposta il testo del titolo dell'asse. Se`null` o se viene specificato un valore vuoto, verrà mostrato il titolo generato automaticamente.

```csharp
public string Text { get; set; }
```

## Osservazioni

Utilizzo[`Show`](../show/)opzione se devi mostrare il titolo.

## Esempi

Mostra come impostare il titolo dell'asse del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// Elimina la serie generata di default.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

ChartAxisTitle chartAxisXTitle = chart.AxisX.Title;
chartAxisXTitle.Text = "Categories";
chartAxisXTitle.Show = true;
ChartAxisTitle chartAxisYTitle = chart.AxisY.Title;
chartAxisYTitle.Text = "Values";
chartAxisYTitle.Show = true;
chartAxisYTitle.Overlay = true;
chartAxisYTitle.Font.Size = 12;
chartAxisYTitle.Font.Color = Color.Blue;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### Guarda anche

* class [ChartAxisTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
