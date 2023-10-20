---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabel classe. Rappresenta letichetta dati su un punto del grafico o su una linea di tendenza in C#.
type: docs
weight: 670
url: /it/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Rappresenta l'etichetta dati su un punto del grafico o su una linea di tendenza.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartDataLabel
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Fornisce l'accesso alla formattazione dei caratteri di questa etichetta dati. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Fornisce l'accesso al riempimento e alla formattazione della riga dell'etichetta dati. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Specifica l'indice dell'elemento contenitore. Questo indice determinerà a quale delle raccolte figli del genitore si applica questo elemento. Il valore predefinito è 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Ottiene/imposta un flag che indica se questa etichetta è nascosta. Il valore predefinito è`falso` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Restituisce`VERO` se questa etichetta dati ha qualcosa da visualizzare. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Restituisce il formato numerico dell'elemento genitore. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Ottiene o imposta il separatore di stringa utilizzato per le etichette dei dati su un grafico. Il valore predefinito è una virgola, ad eccezione dei grafici a torta che mostrano solo il nome della categoria e la percentuale, quando invece deve essere utilizzata un'interruzione di riga . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Permette di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati su un grafico. Si applica solo ai grafici a bolle. Il valore predefinito è`falso` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Permette di specificare se il nome della categoria deve essere visualizzato per le etichette dati su un grafico. Il valore predefinito è`falso` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Permette di specificare se i valori dell'intervallo delle etichette dati devono essere visualizzati nelle etichette dati. Il valore predefinito è`falso` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Permette di specificare se è necessario mostrare le linee guida dell'etichetta dati. Il valore predefinito è`falso` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Permette di specificare se visualizzare la chiave della legenda per le etichette dati su un grafico. Il valore predefinito è`falso` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Permette di specificare se il valore percentuale deve essere visualizzato per le etichette dati su un grafico. Il valore predefinito è`falso` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Restituisce o imposta un valore booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati su un grafico. `VERO` per mostrare il nome della serie;`falso` nascondere. Per impostazione predefinita`falso` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Permette di specificare se i valori devono essere visualizzati nelle etichette dati. Il valore predefinito è`falso` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Cancella il formato di questa etichetta dati. Le proprietà vengono impostate sui valori predefiniti definiti nella raccolta di etichette padre data . |

## Osservazioni

In una serie, il`ChartDataLabel` l'oggetto è un membro di[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Il[`ChartDataLabelCollection`](../chartdatalabelcollection/) contiene un`ChartDataLabel` oggetto per ogni punto.

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
