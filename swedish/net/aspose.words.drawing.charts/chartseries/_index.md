---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Charts.ChartSeries klass. Representerar diagramserieegenskaper i C#.
type: docs
weight: 780
url: /sv/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Representerar diagramserieegenskaper.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartSeries : IChartDataPoint
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Anger om bubblorna i bubbeldiagrammet ska ha en 3D-effekt på dem. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Får en samling bubbelstorlekar för denna diagramserie. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Anger inställningarna för dataetiketterna för hela serien. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Returnerar en samling formateringsobjekt för alla datapunkter i denna serie. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Anger hur mycket datapunkten ska flyttas från mitten av cirkeln. Kan vara negativ, negativ betyder att egenskapen inte är inställd och ingen explosion ska tillämpas. Gäller endast cirkeldiagram. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Ger tillgång till fyllnings- och radformatering av serien. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Hämtar eller ställer in en flagga som indikerar om dataetiketter visas för serien. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Anger om det överordnade elementet ska invertera sina färger om värdet är negativt. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Får en legendpost för denna diagramserie. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Anger en datamarkör. Markör skapas automatiskt vid begäran. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Hämtar eller ställer in namnet på serien, om namnet inte anges explicit genereras det med index. Som standard returnerar Series plus ett baserat index. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Hämtar typen av denna diagramserie. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Gör det möjligt att ange om linjen som förbinder punkterna på diagrammet ska jämnas ut med Catmull-Rom splines. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Får en samling X-värden för denna diagramserie. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Får en samling Y-värden för denna diagramserie. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Lägger till det angivna X-värdet till diagramserien. Om serien stöder Y-värden och bubbelstorlekar kommer de att vara tomma för X-värdet. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Lägger till de angivna X- och Y-värdena till diagramserien. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Lägger till det angivna X-värdet, Y-värdet och bubbelstorleken till diagramserien. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Tar bort alla datavärden från diagramserien. Formatet för alla individuella datapunkter och dataetiketter rensas. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Tar bort alla datavärden från diagramserien med att bevara formatet för datapunkterna och dataetiketterna. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Infogar det angivna X-värdet i diagramserien vid det angivna indexet. Om serien stöder Y-värden och bubbelstorlekar kommer de att vara tomma för X-värdet. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Infogar de angivna X- och Y-värdena i diagramserien vid det angivna indexet. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Infogar det angivna X-värdet, Y-värdet och bubbelstorleken i diagramserien vid det angivna indexet. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Tar bort X-värdet, Y-värdet och bubbelstorleken, om det stöds, från diagramserien vid det angivna indexet. Motsvarande datapunkt och dataetikett tas också bort. |

## Exempel

Visar hur man applicerar etiketter på datapunkter i ett linjediagram.

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

    // Använd dataetiketter på varje serie i diagrammet.
    // Dessa etiketter visas bredvid varje datapunkt i grafen och visar dess värde.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Ändra separatorsträngen för varje dataetikett i en serie.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // För en renare graf kan vi ta bort dataetiketter individuellt.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Vi kan också ta bort en hel serie av dess dataetiketter på en gång.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Använd dataetiketter med anpassat nummerformat och separator på flera datapunkter i en serie.
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

### Se även

* interface [IChartDataPoint](../ichartdatapoint/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
