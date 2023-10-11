---
title: Class ChartDataLabelCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection classe. Rappresenta una raccolta diChartDataLabel .
type: docs
weight: 680
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Rappresenta una raccolta di[`ChartDataLabel`](../chartdatalabel/) .

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Restituisce il numero di[`ChartDataLabel`](../chartdatalabel/) in questa raccolta. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Fornisce l'accesso alla formattazione dei caratteri delle etichette dati dell'intera serie. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Fornisce l'accesso al riempimento e alla formattazione della riga delle etichette dati. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Restituisce[`ChartDataLabel`](../chartdatalabel/) per l'indice specificato. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Ottiene un[`ChartNumberFormat`](../chartnumberformat/) istanza che consente di impostare il formato numerico per le etichette dati dell' intera serie. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Ottiene o imposta il separatore di stringa utilizzato per le etichette dati dell'intera serie. Il valore predefinito è una virgola, ad eccezione dei grafici a torta che mostrano solo il nome della categoria e la percentuale, quando invece deve essere utilizzata un'interruzione di riga . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Permette di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati dell'intera serie. Si applica solo ai grafici a bolle. Il valore predefinito è`falso` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Permette di specificare se il nome della categoria deve essere visualizzato per le etichette dati dell'intera serie. Il valore predefinito è`falso` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Permette di specificare se i valori delle etichette dati devono essere visualizzati nelle etichette dati dell'intera serie. Il valore predefinito è`falso` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Permette di specificare se le linee guida dell'etichetta dati devono essere mostrate per le etichette dati dell'intera serie. Il valore predefinito è`falso` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Permette di specificare se la legenda deve essere visualizzata per le etichette dati dell'intera serie. Il valore predefinito è`falso` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Permette di specificare se visualizzare il valore percentuale per le etichette dati dell'intera serie. Il valore predefinito è`falso` . Si applica solo ai grafici a torta. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Restituisce o imposta un valore booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati dell'intera serie. `VERO` per mostrare il nome della serie;`falso` nascondere. Per impostazione predefinita`falso` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Permette di specificare se i valori devono essere visualizzati nelle etichette dati dell'intera serie. Il valore predefinito è`falso` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Cancella tutto il formato[`ChartDataLabel`](../chartdatalabel/) in questa raccolta. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Restituisce un oggetto enumeratore. |

### Esempi

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
    // Queste etichette appariranno accanto a ciascun punto dati nel grafico e ne visualizzeranno il valore.
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

    // Per un grafico dall'aspetto più pulito, possiamo rimuovere le etichette dei dati individualmente.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Possiamo anche rimuovere un'intera serie di etichette dati contemporaneamente.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Applica etichette dati con formato numerico personalizzato e separatore a diversi punti dati in una serie.
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

* class [ChartDataLabel](../chartdatalabel/)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)


