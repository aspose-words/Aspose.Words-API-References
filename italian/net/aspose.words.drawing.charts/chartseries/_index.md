---
title: Class ChartSeries
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartSeries classe. Rappresenta le proprietà della serie di grafici.
type: docs
weight: 730
url: /it/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Rappresenta le proprietà della serie di grafici.

```csharp
public class ChartSeries : IChartDataPoint
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } |  |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Specifica le impostazioni per le etichette dati per l'intera serie. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Restituisce una raccolta di oggetti di formattazione per tutti i punti dati in questa serie. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } |  |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Fornisce l'accesso al riempimento e alla formattazione della linea della serie. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Ottiene o imposta un flag che indica se vengono visualizzate le etichette dei dati per la serie. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } |  |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Ottiene una voce di legenda per questa serie di grafici. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } |  |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Ottiene o imposta il nome della serie, se il nome non è impostato in modo esplicito viene generato utilizzando index. Per impostazione predefinita restituisce Series più un indice basato. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Consente di specificare se la linea che collega i punti sulla carta deve essere smussata utilizzando le spline Catmull-Rom. |

### Esempi

Mostra come applicare etichette ai punti dati in un grafico a linee.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape chartShape = builder.InsertChart(ChartType.Line, 400, 300);
    Chart chart = chartShape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Applica etichette dati a ogni serie nel grafico.
    // Queste etichette appariranno accanto a ciascun punto dati nel grafico e ne visualizzeranno il valore.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Modifica la stringa di separazione per ogni etichetta di dati in una serie.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // Per un grafico dall'aspetto più pulito, possiamo rimuovere le etichette dei dati individualmente.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Possiamo anche rimuovere un'intera serie di etichette dati contemporaneamente.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Applica etichette dati con formato numerico personalizzato e separatore a più punti dati di una serie.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    for (int i = 0; i < labelsCount; i++)
    {
        series.HasDataLabels = true;

        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        series.DataLabels[i].IsHidden = false;
        Assert.False(series.DataLabels[i].ShowDataLabelsRange);

        series.DataLabels[i].NumberFormat.FormatCode = numberFormat;
        series.DataLabels[i].Separator = separator;

        Assert.False(series.DataLabels[i].ShowDataLabelsRange);
        Assert.True(series.DataLabels[i].IsVisible);
        Assert.False(series.DataLabels[i].IsHidden);
    }
}
```

### Guarda anche

* interface [IChartDataPoint](../ichartdatapoint/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


