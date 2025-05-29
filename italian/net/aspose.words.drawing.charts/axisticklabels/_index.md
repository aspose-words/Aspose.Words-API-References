---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.AxisTickLabels, progettata per migliorare le etichette dei segni di spunta degli assi del tuo grafico con proprietà personalizzabili per una migliore visualizzazione dei dati.
type: docs
weight: 840
url: /it/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

Rappresenta le proprietà delle etichette dei segni di graduazione degli assi.

```csharp
public class AxisTickLabels
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | Ottiene o imposta l'allineamento del testo delle etichette delle tacche degli assi. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | Fornisce accesso alla formattazione del carattere delle etichette di spunta. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | Ottiene o imposta un flag che indica se utilizzare l'intervallo automatico per disegnare le etichette di spunta. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | Ottiene o imposta la distanza delle etichette di spunta dall'asse. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | Ottiene o imposta l'orientamento del testo dell'etichetta di spunta. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | Ottiene o imposta la posizione delle etichette di spunta sull'asse. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | Ottiene o imposta la rotazione delle etichette delle tacche in gradi. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | Ottiene o imposta l'intervallo in cui vengono disegnate le etichette di spunta. |

## Esempi

Mostra come inserire un grafico e modificare l'aspetto dei suoi assi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Cancella la serie di dati demo del grafico per iniziare con un grafico pulito.
chart.Series.Clear();

// Inserire una serie di grafici con categorie per l'asse X e rispettivi valori numerici per l'asse Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Gli assi del grafico hanno varie opzioni che possono modificarne l'aspetto,
// come la loro direzione, le tacche delle unità maggiori/minori e i segni di graduazione.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// I grafici a colonne non hanno l'asse Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
