---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartSeries, la chiave per migliorare le proprietà delle serie di grafici per la creazione e la visualizzazione dinamica di documenti.
type: docs
weight: 1070
url: /it/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Rappresenta le proprietà della serie di grafici.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartSeries : IChartDataPoint
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Specifica se alle bolle nel grafico a bolle deve essere applicato un effetto 3D. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Ottiene una raccolta di dimensioni delle bolle per questa serie di grafici. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Specifica le impostazioni per le etichette dati per l'intera serie. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Restituisce una raccolta di oggetti di formattazione per tutti i punti dati in questa serie. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Specifica di quanto deve essere spostato il punto dati dal centro della torta. Può essere negativo, negativo significa che la proprietà non è impostata e non deve essere applicata alcuna esplosione. Si applica solo ai grafici a torta. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Fornisce accesso al riempimento e alla formattazione delle linee della serie. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Ottiene o imposta un flag che indica se le etichette dati vengono visualizzate per la serie. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Specifica se l'elemento padre deve invertire i suoi colori se il valore è negativo. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Ottiene una voce di legenda per questa serie di grafici. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Specifica un marcatore di dati. Il marcatore viene creato automaticamente quando richiesto. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Ottiene o imposta il nome della serie, se il nome non è impostato esplicitamente viene generato utilizzando l'indice. Per impostazione predefinita, restituisce la serie più un indice basato su. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Ottiene il tipo di questa serie di grafici. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Consente di specificare se la linea che collega i punti sul grafico deve essere levigata utilizzando gli spline Catmull-Rom. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Ottiene una raccolta di valori X per questa serie di grafici. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Ottiene una raccolta di valori Y per questa serie di grafici. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Aggiunge il valore X specificato alla serie del grafico. Se la serie supporta valori Y e dimensioni delle bolle, saranno vuoti per il valore X. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Aggiunge i valori X e Y specificati alla serie del grafico. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Aggiunge il valore X, il valore Y e la dimensione della bolla specificati alla serie del grafico. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Rimuove tutti i valori dei dati dalla serie del grafico. Il formato di tutti i singoli punti dati e delle etichette dati viene cancellato. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Rimuove tutti i valori dei dati dalla serie del grafico preservando il formato dei punti dati e delle etichette dati. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | Copia il formato predefinito del punto dati dal punto dati con l'indice specificato. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Inserisce il valore X specificato nella serie del grafico all'indice specificato. Se la serie supporta valori Y e dimensioni delle bolle, saranno vuoti per il valore X. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Inserisce i valori X e Y specificati nella serie del grafico all'indice specificato. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Inserisce il valore X, il valore Y e la dimensione della bolla specificati nella serie del grafico all'indice specificato. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Rimuove il valore X, il valore Y e la dimensione della bolla, se supportati, dalla serie del grafico all'indice specificato. Vengono rimossi anche il punto dati e l'etichetta dati corrispondenti. |

## Esempi

Mostra come applicare etichette ai punti dati in un grafico a linee.

```csharp
public void DataLabels()
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
    // Queste etichette appariranno accanto a ciascun punto dati nel grafico e ne mostreranno il valore.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Modifica la stringa di separazione per ogni etichetta dati in una serie.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    ChartDataLabel dataLabel = chart.Series[1].DataLabels[2];
    dataLabel.Format.Fill.Color = Color.Red;

    // Per ottenere un grafico più pulito, possiamo rimuovere le etichette dei dati singolarmente.
    dataLabel.ClearFormat();

    // Possiamo anche rimuovere contemporaneamente un'intera serie di etichette dati.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Applica etichette dati con formato numerico personalizzato e separatore a più punti dati in una serie.
/// </summary>
private static void ApplyDataLabels(ChartSeries series, int labelsCount, string numberFormat, string separator)
{
    series.HasDataLabels = true;
    series.Explosion = 40;

    for (int i = 0; i < labelsCount; i++)
    {
        Assert.False(series.DataLabels[i].IsVisible);

        series.DataLabels[i].ShowCategoryName = true;
        series.DataLabels[i].ShowSeriesName = true;
        series.DataLabels[i].ShowValue = true;
        series.DataLabels[i].ShowLeaderLines = true;
        series.DataLabels[i].ShowLegendKey = true;
        series.DataLabels[i].ShowPercentage = false;
        Assert.False(series.DataLabels[i].IsHidden);
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
