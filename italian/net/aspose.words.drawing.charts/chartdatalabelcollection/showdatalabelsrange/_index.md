---
title: ChartDataLabelCollection.ShowDataLabelsRange
linktitle: ShowDataLabelsRange
articleTitle: ShowDataLabelsRange
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShowDataLabelsRange in ChartDataLabelCollection. Controlla la visibilità delle etichette dati per le tue serie e migliora la presentazione dei dati senza sforzo!
type: docs
weight: 120
url: /it/net/aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/
---
## ChartDataLabelCollection.ShowDataLabelsRange property

Consente di specificare se i valori dell'intervallo delle etichette dati devono essere visualizzati nelle etichette dati dell'intera serie. Il valore predefinito è`falso` .

```csharp
public bool ShowDataLabelsRange { get; set; }
```

## Osservazioni

Il valore definito per questa proprietà può essere sovrascritto per una singola etichetta dati utilizzando [`ShowDataLabelsRange`](../../chartdatalabel/showdatalabelsrange/) proprietà.

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

* class [ChartDataLabelCollection](../)
* spazio dei nomi [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assemblea [Aspose.Words](../../../)
