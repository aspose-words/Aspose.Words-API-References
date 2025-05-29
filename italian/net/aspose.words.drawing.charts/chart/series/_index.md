---
title: Chart.Series
linktitle: Series
articleTitle: Series
second_title: Aspose.Words per .NET
description: Scopri la proprietà Chart Series per accedere in esclusiva a una collezione unica di serie. Migliora la tua esperienza di visualizzazione dati oggi stesso!
type: docs
weight: 80
url: /it/net/aspose.words.drawing.charts/chart/series/
---
## Chart.Series property

Fornisce accesso alla raccolta di serie.

```csharp
public ChartSeriesCollection Series { get; }
```

## Esempi

Mostra come creare un tipo appropriato di serie di grafici per un tipo di grafico.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Esistono diversi modi per popolare la raccolta di serie di un grafico.
    // Diversi schemi di serie sono pensati per diversi tipi di grafici.
    // 1 - Grafico a colonne con colonne raggruppate e disposte lungo l'asse X per categoria:
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Inserire due serie di valori decimali contenenti un valore per ciascuna rispettiva categoria.
    // Questo grafico a colonne avrà tre gruppi, ciascuno con due colonne.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Le categorie sono distribuite lungo l'asse X e i valori sono distribuiti lungo l'asse Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Grafico ad area con date distribuite lungo l'asse X:
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Inserire una serie con un valore decimale per ogni rispettiva data.
    // Le date saranno distribuite lungo un asse X lineare,
    // e i valori aggiunti a questa serie creeranno punti dati.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Diagramma di dispersione 2D:
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Ogni serie necessiterà di due array decimali di uguale lunghezza.
    // Il primo array contiene i valori X e il secondo contiene i corrispondenti valori Y
    // dei punti dati sul grafico del grafico.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Grafico a bolle:
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Ogni serie necessiterà di tre array decimali di uguale lunghezza.
    // Il primo array contiene i valori X, il secondo contiene i corrispondenti valori Y,
    // e il terzo contiene i diametri per ciascuno dei punti dati del grafico.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Inserire un grafico utilizzando un generatore di documenti con un ChartType, larghezza e altezza specificati e rimuovere i relativi dati demo.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Guarda anche

* class [ChartSeriesCollection](../../chartseriescollection/)
* class [Chart](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
