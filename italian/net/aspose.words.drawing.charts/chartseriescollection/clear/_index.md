---
title: ChartSeriesCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: ChartSeriesCollection Clear metodo. Rimuove tuttoChartSeries da questa collezione in C#.
type: docs
weight: 40
url: /it/net/aspose.words.drawing.charts/chartseriescollection/clear/
---
## ChartSeriesCollection.Clear method

Rimuove tutto[`ChartSeries`](../../chartseries/) da questa collezione.

```csharp
public void Clear()
```

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

* class [ChartSeriesCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
