---
title: ChartDataPointCollection Class
linktitle: ChartDataPointCollection
articleTitle: ChartDataPointCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartDataPointCollection, la chiave per gestire senza sforzo le raccolte ChartDataPoint per una visualizzazione avanzata dei dati.
type: docs
weight: 980
url: /it/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Rappresenta la raccolta di un[`ChartDataPoint`](../chartdatapoint/) .

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | Restituisce il numero di[`ChartDataPoint`](../chartdatapoint/) in questa raccolta. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Restituisce[`ChartDataPoint`](../chartdatapoint/) per l'indice specificato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Cancella il formato di tutti[`ChartDataPoint`](../chartdatapoint/) in questa raccolta. |
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(*int, int*) | Copia il formato dal punto dati di origine al punto dati di destinazione. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(*int*) | Ottiene un flag che indica se il punto dati all'indice specificato ha un formato predefinito. |

## Esempi

Mostra come lavorare con i punti dati su un grafico a linee.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Metti in risalto i punti dati del grafico facendoli apparire come rombi.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Smussa la linea che rappresenta la prima serie di dati.
    chart.Series[0].Smooth = true;

    // Verificare che i punti dati per la prima serie non invertano i loro colori se il valore è negativo.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Per ottenere un grafico più pulito, possiamo cancellare il formato singolarmente.
    dataPoint.ClearFormat();

    // Possiamo anche eliminare un'intera serie di punti dati in una volta sola.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Applica un numero di punti dati a una serie.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Guarda anche

* class [ChartDataPoint](../chartdatapoint/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
