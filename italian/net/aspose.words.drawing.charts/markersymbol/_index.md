---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.Charts.MarkerSymbol enum. Specifica lo stile del simbolo del contrassegno in C#.
type: docs
weight: 920
url: /it/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Specifica lo stile del simbolo del contrassegno.

```csharp
public enum MarkerSymbol
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Default | `0` | Specifica che un simbolo indicatore predefinito deve essere disegnato in ciascun punto dati. |
| Circle | `1` | Specifica che verrà disegnato un cerchio in corrispondenza di ciascun punto dati. |
| Dash | `2` | Specifica che deve essere tracciato un trattino in corrispondenza di ciascun punto dati. |
| Diamond | `3` | Specifica che deve essere disegnato un diamante in ogni punto dati. |
| Dot | `4` | Specifica che deve essere disegnato un punto in ogni punto dati. |
| None | `5` | Specifica che non deve essere disegnato nulla in ogni punto dati. |
| Picture | `6` | Specifica che verrà disegnata un'immagine in corrispondenza di ciascun punto dati. |
| Plus | `7` | Specifica che deve essere tracciato un segno più in ogni punto dati. |
| Square | `8` | Specifica che verrà disegnato un quadrato in corrispondenza di ciascun punto dati. |
| Star | `9` | Specifica che deve essere disegnata una stella in ogni punto dati. |
| Triangle | `10` | Specifica che verrà disegnato un triangolo in corrispondenza di ciascun punto dati. |
| X | `11` | Specifica che deve essere disegnata una X in corrispondenza di ciascun punto dati. |

## Esempi

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
