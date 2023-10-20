---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.Charts.ChartAxisTitle classe. Fornisce laccesso alle proprietà del titolo dellasse in C#.
type: docs
weight: 650
url: /it/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Fornisce l'accesso alle proprietà del titolo dell'asse.

Per saperne di più, visita il[Lavorare con grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartAxisTitle
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Determina se altri elementi del grafico possono sovrapporsi al titolo. Il valore predefinito è`falso` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Determina se il titolo deve essere mostrato per l'asse. Il valore predefinito è`falso` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Ottiene o imposta il testo del titolo dell'asse. If`nullo` o viene specificato un valore vuoto, verrà mostrato il titolo generato automaticamente. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
