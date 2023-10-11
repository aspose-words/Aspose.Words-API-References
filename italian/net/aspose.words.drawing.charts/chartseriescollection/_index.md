---
title: Class ChartSeriesCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartSeriesCollection classe. Rappresenta la raccolta di aChartSeries .
type: docs
weight: 790
url: /it/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Rappresenta la raccolta di a[`ChartSeries`](../chartseries/) .

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Restituisce il numero di[`ChartSeries`](../chartseries/) in questa raccolta. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Restituisce a[`ChartSeries`](../chartseries/) all'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(string, DateTime[], double[]) | Aggiunge nuovo[`ChartSeries`](../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico ad area, radar e azionario. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(string, double[], double[]) | Aggiunge nuovo[`ChartSeries`](../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico a dispersione. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(string, string[], double[]) | Aggiunge nuovo[`ChartSeries`](../chartseries/) a questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico a barre, a colonne, a linee e a superficie. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(string, double[], double[], double[]) | Aggiunge nuovo[`ChartSeries`](../chartseries/) questa raccolta. Utilizza questo metodo per aggiungere serie a qualsiasi tipo di grafico a bolle. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Rimuove tutto[`ChartSeries`](../chartseries/) da questa collezione. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(int) | Rimuove a[`ChartSeries`](../chartseries/) all'indice specificato. |

### Esempi

Mostra come aggiungere e rimuovere i dati delle serie in un grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un istogramma che conterrà tre serie di dati dimostrativi per impostazione predefinita.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Ogni serie ha quattro valori decimali: uno per ciascuna delle quattro categorie.
// Quattro gruppi di tre colonne rappresenteranno questi dati.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Stampa il nome di ogni serie nel grafico.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Questi sono i nomi delle categorie nel grafico.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Possiamo aggiungere una serie con nuovi valori per le categorie esistenti.
// Questo grafico ora conterrà quattro gruppi di quattro colonne.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Una serie di grafici può anche essere rimossa tramite indice, in questo modo.
// Ciò rimuoverà una delle tre serie demo fornite con il grafico.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Con questo metodo possiamo anche cancellare tutti i dati del grafico contemporaneamente.
// Quando si crea un nuovo grafico, questo è il modo per cancellare tutti i dati demo
// prima di poter iniziare a lavorare su un grafico vuoto.
chartData.Clear();
```

### Guarda anche

* class [ChartSeries](../chartseries/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


