---
title: ChartSeriesCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words per .NET
description: Scopri la proprietà ChartSeriesCollection Count, che fornisce il numero totale di ChartSeries nella tua raccolta per una visualizzazione avanzata dei dati.
type: docs
weight: 10
url: /it/net/aspose.words.drawing.charts/chartseriescollection/count/
---
## ChartSeriesCollection.Count property

Restituisce il numero di[`ChartSeries`](../../chartseries/) in questa raccolta.

```csharp
public int Count { get; }
```

## Esempi

Mostra come aggiungere e rimuovere dati di serie in un grafico.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un grafico a colonne che conterrà per impostazione predefinita tre serie di dati demo.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Ogni serie ha quattro valori decimali: uno per ciascuna delle quattro categorie.
// Questi dati saranno rappresentati da quattro cluster di tre colonne.
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
// Questo grafico conterrà ora quattro cluster di quattro colonne.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Una serie di grafici può anche essere rimossa tramite indice, in questo modo.
// Questa operazione rimuoverà una delle tre serie demo fornite con il grafico.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Con questo metodo possiamo anche cancellare tutti i dati del grafico in una volta sola.
// Quando si crea un nuovo grafico, questo è il modo per cancellare tutti i dati demo
// prima di poter iniziare a lavorare su un grafico vuoto.
chartData.Clear();
```

### Guarda anche

* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
