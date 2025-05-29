---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words per .NET
description: Esplora l'enum Aspose.Words.Drawing.Charts.MarkerSymbol per stili di marcatore personalizzabili che migliorano la visualizzazione dei grafici e la presentazione dei dati.
type: docs
weight: 1240
url: /it/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Specifica lo stile del simbolo del marcatore.

```csharp
public enum MarkerSymbol
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica che un simbolo di marcatore predefinito deve essere disegnato su ogni punto dati. |
| Circle | `1` | Specifica che deve essere disegnato un cerchio in ogni punto dati. |
| Dash | `2` | Specifica che deve essere disegnato un trattino su ogni punto dati. |
| Diamond | `3` | Specifica che un diamante deve essere disegnato su ogni punto dati. |
| Dot | `4` | Specifica che deve essere disegnato un punto su ogni punto dati. |
| None | `5` | Specifica che non verrà disegnato nulla in ogni punto dati. |
| Picture | `6` | Specifica che un'immagine deve essere disegnata in ogni punto dati. |
| Plus | `7` | Specifica che deve essere disegnato un segno più su ogni punto dati. |
| Square | `8` | Specifica che deve essere disegnato un quadrato in ogni punto dati. |
| Star | `9` | Specifica che una stella deve essere disegnata su ogni punto dati. |
| Triangle | `10` | Specifica che deve essere disegnato un triangolo in ogni punto dati. |
| X | `11` | Specifica che una X deve essere disegnata su ogni punto dati. |

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
