---
title: ChartDataPointCollection.ClearFormat
second_title: Aspose.Words per .NET API Reference
description: ChartDataPointCollection metodo. Cancella tutto il formatoChartDataPoint in questa raccolta.
type: docs
weight: 30
url: /it/net/aspose.words.drawing.charts/chartdatapointcollection/clearformat/
---
## ChartDataPointCollection.ClearFormat method

Cancella tutto il formato[`ChartDataPoint`](../../chartdatapoint/) in questa raccolta.

```csharp
public void ClearFormat()
```

### Esempi

Mostra come lavorare con i punti dati su un grafico a linee.

```csharp
[Test]
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

    // Appiana la linea che rappresenta la prima serie di dati.
    chart.Series[0].Smooth = true;

    // Verifica che i punti dati per la prima serie non invertano i loro colori se il valore è negativo.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Per un grafico dall'aspetto più pulito, possiamo cancellare il formato individualmente.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Possiamo anche rimuovere un'intera serie di punti dati contemporaneamente.
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

* class [ChartDataPointCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../chartdatapointcollection/)
* assemblea [Aspose.Words](../../../)


