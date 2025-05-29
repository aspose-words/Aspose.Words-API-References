---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.ChartSeriesGroupCollection, la soluzione ideale per gestire e organizzare gli oggetti ChartSeriesGroup senza sforzo.
type: docs
weight: 1100
url: /it/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Rappresenta una raccolta di[`ChartSeriesGroup`](../chartseriesgroup/) oggetti.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Restituisce il numero di gruppi di serie in questa raccolta. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Restituisce un[`ChartSeriesGroup`](../chartseriesgroup/) all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Aggiunge un nuovo gruppo di serie del tipo di serie specificato a questa raccolta. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Rimuove un gruppo di serie all'indice specificato. Tutte le serie figlie verranno rimosse dal grafico. |

## Osservazioni

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
