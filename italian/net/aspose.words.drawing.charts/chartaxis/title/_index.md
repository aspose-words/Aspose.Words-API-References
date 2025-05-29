---
title: ChartAxis.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words per .NET
description: Scopri la proprietà Titolo di ChartAxis per un facile accesso e personalizzazione dei titoli degli assi, migliorando la visualizzazione e la presentazione dei tuoi dati.
type: docs
weight: 250
url: /it/net/aspose.words.drawing.charts/chartaxis/title/
---
## ChartAxis.Title property

Fornisce l'accesso alle proprietà del titolo dell'asse.

```csharp
public ChartAxisTitle Title { get; }
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

* class [ChartAxisTitle](../../chartaxistitle/)
* class [ChartAxis](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
