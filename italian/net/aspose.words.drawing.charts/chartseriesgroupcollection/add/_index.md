---
title: ChartSeriesGroupCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words per .NET
description: Scopri il metodo ChartSeriesGroupCollection Add per aggiungere senza sforzo nuovi gruppi di serie, migliorando le tue capacità di visualizzazione dei dati.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---
## ChartSeriesGroupCollection.Add method

Aggiunge un nuovo gruppo di serie del tipo di serie specificato a questa raccolta.

```csharp
public ChartSeriesGroup Add(ChartSeriesType seriesType)
```

## Osservazioni

I grafici combinati possono contenere gruppi di serie solo dei seguenti tipi: area, barre, colonne, linee, torta, dispersione, radar e azioni (ad eccezione dei tipi di serie 3D corrispondenti).

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

* class [ChartSeriesGroup](../../chartseriesgroup/)
* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroupCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
