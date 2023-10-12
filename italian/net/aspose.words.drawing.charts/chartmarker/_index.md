---
title: Class ChartMarker
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartMarker classe. Rappresenta un indicatore di dati del grafico.
type: docs
weight: 750
url: /it/net/aspose.words.drawing.charts/chartmarker/
---
## ChartMarker class

Rappresenta un indicatore di dati del grafico.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartMarker
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Format](../../aspose.words.drawing.charts/chartmarker/format/) { get; } | Fornisce l'accesso al riempimento e alla formattazione della linea di questo indicatore. |
| [Size](../../aspose.words.drawing.charts/chartmarker/size/) { get; set; } | Ottiene o imposta la dimensione dell'indicatore del grafico. Il valore predefinito è 7. |
| [Symbol](../../aspose.words.drawing.charts/chartmarker/symbol/) { get; set; } | Ottiene o imposta il simbolo dell'indicatore del grafico. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


