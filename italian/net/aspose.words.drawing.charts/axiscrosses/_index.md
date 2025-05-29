---
title: AxisCrosses Enum
linktitle: AxisCrosses
articleTitle: AxisCrosses
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.Charts.AxisCrosses per definire i punti di incrocio degli assi, migliorando così le tue capacità di creazione di grafici senza sforzo.
type: docs
weight: 780
url: /it/net/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enumeration

Specifica i possibili punti di attraversamento per un asse.

```csharp
public enum AxisCrosses
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Automatic | `0` | L'asse delle categorie incrocia il punto zero dell'asse dei valori (se possibile), oppure il valore minimo se il minimo è maggiore di zero, oppure il valore massimo se il massimo è minore di zero. |
| Maximum | `1` | Un asse perpendicolare attraversa il valore massimo dell'asse. |
| Minimum | `2` | Un asse perpendicolare attraversa il valore minimo dell'asse. |
| Custom | `3` | Un asse perpendicolare attraversa il valore specificato dell'asse. |

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
