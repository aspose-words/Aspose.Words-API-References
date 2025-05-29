---
title: AxisTickLabels.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words per .NET
description: Controlla la spaziatura delle etichette degli assi senza sforzo! Imposta intervalli per le etichette dei tick per migliorare la visualizzazione dei dati e la chiarezza dei grafici.
type: docs
weight: 80
url: /it/net/aspose.words.drawing.charts/axisticklabels/spacing/
---
## AxisTickLabels.Spacing property

Ottiene o imposta l'intervallo in cui vengono disegnate le etichette di spunta.

```csharp
public int Spacing { get; set; }
```

## Osservazioni

La proprietà ha effetto sugli assi delle categorie di testo e delle serie. Non è supportata dai nuovi grafici di MS Office 2016 . L'intervallo valido di un valore è maggiore o uguale a 1.

L'impostazione di questa proprietà imposta il[`IsAutoSpacing`](../isautospacing/) proprietà a`falso`.

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

* class [AxisTickLabels](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
