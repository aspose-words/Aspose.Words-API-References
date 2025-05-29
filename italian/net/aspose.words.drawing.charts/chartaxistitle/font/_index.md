---
title: ChartAxisTitle.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: Personalizza il tuo ChartAxisTitle con versatili opzioni di font. Migliora la visualizzazione dei dati con una formattazione unica dei titoli degli assi per informazioni più chiare.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartaxistitle/font/
---
## ChartAxisTitle.Font property

Fornisce accesso alla formattazione del carattere del titolo dell'asse.

```csharp
public Font Font { get; }
```

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

* class [Font](../../../aspose.words/font/)
* class [ChartAxisTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
