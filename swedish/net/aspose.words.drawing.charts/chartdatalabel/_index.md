---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Drawing.Charts.ChartDataLabel för förbättrad datavisualisering i diagram. Förbättra dina presentationer med exakta dataetiketter!
type: docs
weight: 930
url: /sv/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Representerar dataetiketten på en diagrampunkt eller trendlinje.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartDataLabel
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Ger åtkomst till teckensnittsformateringen för denna dataetikett. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering av dataetiketten. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Anger indexet för det innehållande elementet. Detta index ska avgöra vilken av de överordnade och underordnade samlingarna detta element gäller för. Standardvärdet är 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Hämtar/ställer in en flagga som anger om denna etikett är dold. Standardvärdet är`falsk` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Returer`sann` om den här dataetiketten har något att visa. |
| [Left](../../aspose.words.drawing.charts/chartdatalabel/left/) { get; set; } | Hämtar eller anger avståndet för dataetiketten i punkter från diagrammets vänstra kant eller från positionen som anges av dess[`Position`](./position/) egendom, beroende på värdet av[`LeftMode`](./leftmode/) egenskap. |
| [LeftMode](../../aspose.words.drawing.charts/chartdatalabel/leftmode/) { get; set; } | Hämtar eller ställer in tolkningsläget för[`Left`](./left/) egenskapsvärde: om den anger location för dataetiketten från diagrammets vänstra kant eller från den position som anges av dess[`Position`](./position/) egenskap. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Returnerar talformatet för det överordnade elementet. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabel/orientation/) { get; set; } | Hämtar eller anger orienteringen för etikettexten. |
| [Position](../../aspose.words.drawing.charts/chartdatalabel/position/) { get; set; } | Hämtar eller anger positionen för dataetiketten. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabel/rotation/) { get; set; } | Hämtar eller ställer in rotationen av etiketten i grader. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Hämtar eller ställer in strängavgränsare som används för dataetiketter i ett diagram. Standardvärdet är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procentandel, då en radbrytning ska användas istället. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Gör det möjligt att ange om bubbelstorlek ska visas för dataetiketterna i ett diagram. Gäller endast bubbeldiagram. Standardvärdet är`falsk` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Gör det möjligt att ange om kategorinamnet ska visas för dataetiketterna i ett diagram. Standardvärdet är`falsk` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Gör det möjligt att ange om värden från dataetikettintervallet ska visas i dataetiketterna. Standardvärdet är`falsk` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Gör det möjligt att ange om riktlinjer för dataetiketter behöver visas. Standardvärdet är`falsk` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Gör det möjligt att ange om förklaringsnyckeln ska visas för dataetiketterna i ett diagram. Standardvärdet är`falsk` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Gör det möjligt att ange om procentvärde ska visas för dataetiketterna i ett diagram. Standardvärdet är`falsk` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Returnerar eller anger ett booleskt värde för att ange visningsbeteendet för serienamn för dataetiketterna i ett diagram. `sann` för att visa seriens namn;`falsk` att dölja. Som standard`falsk` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Gör det möjligt att ange om värden ska visas i dataetiketterna. Standardvärdet är`falsk` . |
| [Top](../../aspose.words.drawing.charts/chartdatalabel/top/) { get; set; } | Hämtar eller ställer in dataetikettens avstånd i punkter från diagrammets överkant eller från positionen som anges av dess[`Position`](./position/) egendom, beroende på värdet av[`TopMode`](./topmode/) egenskap. |
| [TopMode](../../aspose.words.drawing.charts/chartdatalabel/topmode/) { get; set; } | Hämtar eller ställer in tolkningsläget för[`Top`](./top/) egenskapsvärde: om den anger location för dataetiketten från diagrammets överkant eller från den position som anges av dess[`Position`](./position/) egenskap. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Rensar formatet för denna dataetikett. Egenskaperna ställs in på standardvärdena som definierats i den överordnade data etikettsamlingen. |

## Anmärkningar

På en serie, den`ChartDataLabel` objektet är medlem i[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Den[`ChartDataLabelCollection`](../chartdatalabelcollection/) innehåller en`ChartDataLabel` objekt för varje punkt.

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

    // Ändra avgränsningssträngen för varje dataetikett i en serie.
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

    // För en renare graf kan vi ta bort dataetiketter individuellt.
    dataLabel.ClearFormat();

    // Vi kan också ta bort en hel serie av dess dataetiketter samtidigt.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Använd dataetiketter med anpassat talformat och avgränsare på flera datapunkter i en serie.
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

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
