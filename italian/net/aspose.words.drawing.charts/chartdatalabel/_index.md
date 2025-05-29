---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Drawing.Charts.ChartDataLabel per una visualizzazione avanzata dei dati nei grafici. Migliora le tue presentazioni con etichette dati precise!
type: docs
weight: 930
url: /it/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Rappresenta l'etichetta dati su un punto del grafico o una linea di tendenza.

Per saperne di più, visita il[Lavorare con i grafici](https://docs.aspose.com/words/net/working-with-charts/) articolo di documentazione.

```csharp
public class ChartDataLabel
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Fornisce l'accesso alla formattazione del carattere di questa etichetta dati. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Fornisce accesso al riempimento e alla formattazione della riga dell'etichetta dati. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Specifica l'indice dell'elemento contenitore. Questo indice determina a quale delle raccolte figlie del genitore si applica questo elemento. Il valore predefinito è 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Ottiene/imposta un flag che indica se questa etichetta è nascosta. Il valore predefinito è`falso` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Restituisce`VERO` se questa etichetta dati ha qualcosa da visualizzare. |
| [Left](../../aspose.words.drawing.charts/chartdatalabel/left/) { get; set; } | Ottiene o imposta la distanza dell'etichetta dati in punti dal bordo sinistro del grafico o dalla posizione specificata dal suo[`Position`](./position/) proprietà, a seconda del valore della[`LeftMode`](./leftmode/) Proprietà . |
| [LeftMode](../../aspose.words.drawing.charts/chartdatalabel/leftmode/) { get; set; } | Ottiene o imposta la modalità di interpretazione del[`Left`](./left/) valore della proprietà: se imposta la posizione dell'etichetta dati dal bordo sinistro del grafico o dalla posizione specificata dal suo[`Position`](./position/) Proprietà . |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Restituisce il formato numerico dell'elemento padre. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabel/orientation/) { get; set; } | Ottiene o imposta l'orientamento del testo dell'etichetta. |
| [Position](../../aspose.words.drawing.charts/chartdatalabel/position/) { get; set; } | Ottiene o imposta la posizione dell'etichetta dati. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabel/rotation/) { get; set; } | Ottiene o imposta la rotazione dell'etichetta in gradi. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Ottiene o imposta il separatore di stringa utilizzato per le etichette dati su un grafico. Il valore predefinito è una virgola, ad eccezione dei grafici a torta che mostrano solo il nome della categoria e la percentuale, in tal caso deve essere utilizzata un'interruzione di riga . |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Consente di specificare se la dimensione della bolla deve essere visualizzata per le etichette dati su un grafico. Si applica solo ai grafici a bolle. Il valore predefinito è `falso` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Consente di specificare se il nome della categoria deve essere visualizzato per le etichette dati su un grafico. Il valore predefinito è `falso` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Consente di specificare se i valori dell'intervallo delle etichette dati devono essere visualizzati nelle etichette dati. Il valore predefinito è `falso` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Consente di specificare se è necessario visualizzare le linee guida dell'etichetta dati. Il valore predefinito è `falso` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Consente di specificare se la legenda deve essere visualizzata per le etichette dati su un grafico. Il valore predefinito è `falso` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Consente di specificare se il valore percentuale deve essere visualizzato per le etichette dati su un grafico. Il valore predefinito è `falso` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Restituisce o imposta un valore booleano per indicare il comportamento di visualizzazione del nome della serie per le etichette dati su un grafico. `VERO` per mostrare il nome della serie;`falso` per nascondere. Per impostazione predefinita`falso` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Consente di specificare se i valori devono essere visualizzati nelle etichette dati. Il valore predefinito è `falso` . |
| [Top](../../aspose.words.drawing.charts/chartdatalabel/top/) { get; set; } | Ottiene o imposta la distanza dell'etichetta dati in punti dal bordo superiore del grafico o dalla posizione specificata dal suo[`Position`](./position/) proprietà, a seconda del valore della[`TopMode`](./topmode/) Proprietà . |
| [TopMode](../../aspose.words.drawing.charts/chartdatalabel/topmode/) { get; set; } | Ottiene o imposta la modalità di interpretazione del[`Top`](./top/) valore della proprietà: se imposta la posizione dell'etichetta dati dal bordo superiore del grafico o dalla posizione specificata dal suo[`Position`](./position/) Proprietà . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Cancella il formato di questa etichetta dati. Le proprietà vengono impostate sui valori predefiniti definiti nella raccolta di etichette data padre. |

## Osservazioni

In una serie, il`ChartDataLabel` l'oggetto è un membro del[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Il[`ChartDataLabelCollection`](../chartdatalabelcollection/) contiene un`ChartDataLabel` oggetto per ogni punto.

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

* spazio dei nomi [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../)
