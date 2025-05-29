---
title: ChartAxisTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartAxisTitle Show per controllare la visibilità del titolo degli assi. Arricchisci i tuoi grafici con titoli chiari e informativi per una migliore comprensione dei dati.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

Determina se il titolo deve essere visualizzato per l'asse. Il valore predefinito è`falso` .

```csharp
public bool Show { get; set; }
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

* class [ChartAxisTitle](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
