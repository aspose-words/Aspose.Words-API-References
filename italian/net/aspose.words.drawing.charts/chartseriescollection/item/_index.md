---
title: ChartSeriesCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: ChartSeriesCollection Item proprietà. Restituisce aChartSeries allindice specificato in C#.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

Restituisce a[`ChartSeries`](../../chartseries/) all'indice specificato.

```csharp
public ChartSeries this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nella raccolta. |

## Osservazioni

L'indice è a base zero.

Gli indici negativi sono consentiti e indicano l'accesso dal retro della raccolta. Ad esempio -1 significa l'ultimo elemento, -2 significa il penultimo e così via.

Se indice è maggiore o uguale al numero di elementi nell'elenco, restituisce un riferimento null.

Se indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, restituisce un riferimento null.

## Esempi

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
