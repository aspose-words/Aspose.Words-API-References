---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartSeriesGroup, che semplifica la gestione delle proprietà delle serie di grafici per una visualizzazione e un'analisi dei dati ottimizzate.
type: docs
weight: 1090
url: /it/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Rappresenta le proprietà di un gruppo di serie di grafici, ovvero le proprietà di serie di grafici dello stesso tipo associate agli stessi assi.

```csharp
public class ChartSeriesGroup
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Ottiene o imposta il gruppo di assi a cui appartiene questo gruppo di serie. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Fornisce l'accesso alle proprietà dell'asse X di questo gruppo di serie. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Fornisce l'accesso alle proprietà dell'asse Y di questo gruppo di serie. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Ottiene o imposta la dimensione delle bolle come percentuale della loro dimensione predefinita. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Ottiene o imposta la dimensione del foro del grafico a ciambella padre come percentuale. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Ottiene o imposta l'angolo, in gradi, della prima fetta del grafico a torta padre. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Ottiene o imposta la percentuale di larghezza dello spazio tra gli elementi del grafico. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Ottiene o imposta la percentuale di sovrapposizione delle barre o delle colonne della serie. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Ottiene o imposta la dimensione della sezione secondaria del grafico a torta in percentuale. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Ottiene una raccolta di serie che appartengono a questo gruppo di serie. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Ottiene il tipo di serie di grafici inclusa in questo gruppo. |

## Osservazioni

I grafici combinati contengono più gruppi di serie di grafici, con un gruppo separato per ogni tipo di serie.

È inoltre possibile creare un gruppo di serie di grafici per assegnare assi secondari a una o più serie di grafici.

Per saperne di più, visita il[ Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
