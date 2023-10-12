---
title: Class ChartDataPoint
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartDataPoint classe. Permette di specificare la formattazione di un singolo punto dati sul grafico.
type: docs
weight: 690
url: /it/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Permette di specificare la formattazione di un singolo punto dati sul grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Specifica se alle bolle nel grafico a bolle deve essere applicato un effetto 3D. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Specifica di quanto il punto dati deve essere spostato dal centro della torta. Può essere negativo, negativo significa che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Fornisce l'accesso al riempimento e alla formattazione della linea di questo punto dati. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Indice del punto dati a cui questo oggetto applica la formattazione. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Specifica se l'elemento genitore deve invertire i suoi colori se il valore è negativo. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Specifica l'indicatore dei dati del grafico. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Cancella il formato di questo punto dati. Le proprietà vengono impostate sui valori predefiniti definiti nella serie principale. |

### Osservazioni

In una serie, il`ChartDataPoint` l'oggetto è un membro di[`ChartDataPointCollection`](../chartdatapointcollection/) . Il[`ChartDataPointCollection`](../chartdatapointcollection/) contiene un`ChartDataPoint` oggetto per ogni punto.

### Esempi

Mostra come utilizzare i punti dati su un grafico a linee.

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

    // Enfatizza i punti dati del grafico facendoli apparire come forme di diamante.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Appianare la linea che rappresenta la prima serie di dati.
    chart.Series[0].Smooth = true;

    // Verifica che i punti dati per la prima serie non invertano i colori se il valore è negativo.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Per un grafico dall'aspetto più pulito, possiamo cancellare il formato individualmente.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Possiamo anche eliminare un'intera serie di punti dati contemporaneamente.
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

* interface [IChartDataPoint](../ichartdatapoint/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


