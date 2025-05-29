---
title: ChartSeriesGroup.Series
linktitle: Series
articleTitle: Series
second_title: Aspose.Words per .NET
description: Scopri la proprietà Serie ChartSeriesGroup per accedere a una raccolta unica di serie correlate, migliorando la tua esperienza di visualizzazione dei dati.
type: docs
weight: 100
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/series/
---
## ChartSeriesGroup.Series property

Ottiene una raccolta di serie che appartengono a questo gruppo di serie.

```csharp
public ChartSeriesCollection Series { get; }
```

## Esempi

Mostra come lavorare con l'asse secondario del grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Elimina la serie generata di default.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Crea un gruppo di serie aggiuntivo, anch'esso di tipo linea.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Specificare l'uso di assi secondari per il nuovo gruppo di serie.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Nascondi l'asse X secondario.
newSeriesGroup.AxisX.Hidden = true;
// Definisce il titolo dell'asse Y secondario.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Aggiunge una serie al nuovo gruppo di serie.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Guarda anche

* class [ChartSeriesCollection](../../chartseriescollection/)
* class [ChartSeriesGroup](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
