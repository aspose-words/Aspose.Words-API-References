---
title: IChartDataPoint Interface
linktitle: IChartDataPoint
articleTitle: IChartDataPoint
second_title: Aspose.Words per .NET
description: Esplora l'interfaccia Aspose.Words.Drawing.Charts.IChartDataPoint per informazioni dettagliate sulle proprietà dei punti dati dei grafici. Migliora la visualizzazione dei tuoi dati senza sforzo!
type: docs
weight: 1220
url: /it/net/aspose.words.drawing.charts/ichartdatapoint/
---
## IChartDataPoint interface

Contiene le proprietà di un singolo punto dati sul grafico.

```csharp
public interface IChartDataPoint
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/ichartdatapoint/bubble3d/) { get; set; } | Specifica se alle bolle nel grafico a bolle deve essere applicato un effetto 3D. |
| [Explosion](../../aspose.words.drawing.charts/ichartdatapoint/explosion/) { get; set; } | Specifica di quanto deve essere spostato il punto dati dal centro della torta. Può essere negativo, negativo significa che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| [InvertIfNegative](../../aspose.words.drawing.charts/ichartdatapoint/invertifnegative/) { get; set; } | Specifica se l'elemento padre deve invertire i suoi colori se il valore è negativo. |
| [Marker](../../aspose.words.drawing.charts/ichartdatapoint/marker/) { get; } | Specifica un marcatore di dati. Il marcatore viene creato automaticamente quando richiesto. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
