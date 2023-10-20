---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabel klass. Representerar dataetikett på en diagrampunkt eller trendlinje i C#.
type: docs
weight: 670
url: /sv/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Representerar dataetikett på en diagrampunkt eller trendlinje.

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartDataLabel
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Ger tillgång till teckensnittsformateringen för denna dataetikett. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Ger tillgång till fyllnings- och radformatering av dataetiketten. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Anger indexet för det innehållande elementet. Detta index ska avgöra vilken av förälderns barnsamling detta element gäller. Standardvärdet är 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Hämtar/ställer in en flagga som indikerar om denna etikett är dold. Standardvärdet är`falsk` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Returnerar`Sann` om denna dataetikett har något att visa. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Returnerar talformatet för det överordnade elementet. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Hämtar eller ställer in strängseparator som används för dataetiketterna i ett diagram. Standard är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procent, då en radbrytning ska användas istället. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Gör det möjligt att ange om bubbelstorlek ska visas för dataetiketterna i ett diagram. Gäller endast för bubbeldiagram. Standardvärdet är`falsk` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Gör det möjligt att ange om kategorinamnet ska visas för dataetiketterna på ett diagram. Standardvärdet är`falsk` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Gör det möjligt att ange om värden från dataetikettområdet ska visas i dataetiketterna. Standardvärdet är`falsk` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Tillåter att ange om dataetikettens ledarlinjer behöver visas. Standardvärdet är`falsk` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Tillåter att ange om förklaringsnyckeln ska visas för dataetiketterna på ett diagram. Standardvärdet är`falsk` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Gör det möjligt att ange om ett procentvärde ska visas för dataetiketterna i ett diagram. Standardvärdet är`falsk` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Returnerar eller ställer in en boolesk för att indikera visningsbeteendet för serienamnet för dataetiketterna i ett diagram. `Sann` för att visa serienamnet;`falsk` att gömma. Som standard`falsk` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Gör det möjligt att ange om värden ska visas i dataetiketterna. Standardvärdet är`falsk` . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Rensar formatet för denna dataetikett. Egenskaperna är inställda på standardvärdena som definieras i den överordnade data etikettsamlingen. |

## Anmärkningar

På en serie`ChartDataLabel` objektet är medlem i[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Den[`ChartDataLabelCollection`](../chartdatalabelcollection/) innehåller en`ChartDataLabel` objekt för varje punkt.

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

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
