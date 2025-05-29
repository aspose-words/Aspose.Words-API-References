---
title: ChartAxisTitle Class
linktitle: ChartAxisTitle
articleTitle: ChartAxisTitle
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.ChartAxisTitle per gestire facilmente le proprietà dei titoli degli assi e migliorare l'impatto visivo del tuo documento.
type: docs
weight: 910
url: /it/net/aspose.words.drawing.charts/chartaxistitle/
---
## ChartAxisTitle class

Fornisce l'accesso alle proprietà del titolo dell'asse.

Per saperne di più, visita il[Lavorare con i grafici ](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartAxisTitle
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartaxistitle/font/) { get; } | Fornisce accesso alla formattazione del carattere del titolo dell'asse. |
| [Format](../../aspose.words.drawing.charts/chartaxistitle/format/) { get; } | Fornisce accesso al riempimento e alla formattazione della linea del titolo dell'asse. |
| [Overlay](../../aspose.words.drawing.charts/chartaxistitle/overlay/) { get; set; } | Determina se altri elementi del grafico possono sovrapporsi al titolo. Il valore predefinito è`falso` . |
| [Show](../../aspose.words.drawing.charts/chartaxistitle/show/) { get; set; } | Determina se il titolo deve essere visualizzato per l'asse. Il valore predefinito è`falso` . |
| [Text](../../aspose.words.drawing.charts/chartaxistitle/text/) { get; set; } | Ottiene o imposta il testo del titolo dell'asse. Se`null` o se viene specificato un valore vuoto, verrà mostrato il titolo generato automaticamente. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
