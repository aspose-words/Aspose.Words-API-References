---
title: Enum MarkerSymbol
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.MarkerSymbol enum. Specifica lo stile del simbolo dellindicatore.
type: docs
weight: 790
url: /it/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Specifica lo stile del simbolo dell'indicatore.

```csharp
public enum MarkerSymbol
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica un simbolo di indicatore predefinito da disegnare in ogni punto dati. |
| Circle | `1` | Specifica un cerchio da disegnare in ogni punto dati. |
| Dash | `2` | Specifica un trattino da disegnare in ogni punto dati. |
| Diamond | `3` | Specifica un diamante da disegnare in ogni punto dati. |
| Dot | `4` | Specifica un punto da disegnare in ogni punto dati. |
| None | `5` | Specifica che non deve essere disegnato nulla in ogni punto dati. |
| Picture | `6` | Specifica che deve essere disegnata un'immagine in ogni punto dati. |
| Plus | `7` | Specifica un segno più da disegnare in ogni punto dati. |
| Square | `8` | Specifica un quadrato da disegnare in ogni punto dati. |
| Star | `9` | Specifica che deve essere disegnata una stella in ogni punto dati. |
| Triangle | `10` | Specifica un triangolo da disegnare in ogni punto dati. |
| X | `11` | Specifica che deve essere disegnata una X in ogni punto dati. |

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


