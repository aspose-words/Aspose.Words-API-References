---
title: ChartFormat Class
linktitle: ChartFormat
articleTitle: ChartFormat
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.ChartFormat per uno stile avanzato degli elementi dei grafici. Arricchisci i tuoi documenti con design professionali e personalizzabili.
type: docs
weight: 1000
url: /it/net/aspose.words.drawing.charts/chartformat/
---
## ChartFormat class

Rappresenta la formattazione di un elemento del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Fill](../../aspose.words.drawing.charts/chartformat/fill/) { get; } | Ottiene la formattazione di riempimento per l'elemento del grafico padre. |
| [IsDefined](../../aspose.words.drawing.charts/chartformat/isdefined/) { get; } | Ottiene un flag che indica se è definito un formato. |
| [ShapeType](../../aspose.words.drawing.charts/chartformat/shapetype/) { get; set; } | Ottiene o imposta il tipo di forma dell'elemento del grafico padre. |
| [Stroke](../../aspose.words.drawing.charts/chartformat/stroke/) { get; } | Ottiene la formattazione della linea per l'elemento del grafico padre. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetDefaultFill](../../aspose.words.drawing.charts/chartformat/setdefaultfill/)() | Reimposta il riempimento dell'elemento del grafico in modo che abbia il valore predefinito. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
