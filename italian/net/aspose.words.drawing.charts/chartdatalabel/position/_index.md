---
title: ChartDataLabel.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words per .NET
description: Scopri la proprietà Posizione ChartDataLabel per personalizzare facilmente la posizione dell'etichetta dati per una visualizzazione e una chiarezza dei dati ottimizzate.
type: docs
weight: 100
url: /it/net/aspose.words.drawing.charts/chartdatalabel/position/
---
## ChartDataLabel.Position property

Ottiene o imposta la posizione dell'etichetta dati.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Osservazioni

È possibile impostare la posizione per le etichette dati dei seguenti tipi di serie di grafici:

-Bar ,Column , Histogram ,Pareto , Waterfall ; valori consentiti:Center , InsideBase ,InsideEnd e OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; valori consentiti :Center ,InsideBase eInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock ; valori consentiti:Center , Left ,Right , Above EBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie ; valori consentiti: Center ,InsideEnd , OutsideEnd EBestFit;

-BoxAndWhisker ; valori consentiti: Left ,Right , Above EBelow.

## Esempi

Mostra come impostare la posizione dell'etichetta dati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un grafico a colonne.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Elimina la serie generata di default.
seriesColl.Clear();

// Aggiungi serie.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Mostra le etichette dei dati e imposta il colore del carattere.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Imposta la posizione dell'etichetta dati.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Guarda anche

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabel](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
