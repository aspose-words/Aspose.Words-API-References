---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.ChartDataLabelCollection för att effektivt hantera diagramdataetiketter. Förbättra ditt dokuments visuella attraktionskraft idag!
type: docs
weight: 940
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Representerar en samling av[`ChartDataLabel`](../chartdatalabel/) .

För att lära dig mer, besök[Arbeta med diagram](https://docs.aspose.com/words/net/working-with-charts/) dokumentationsartikel.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Returnerar antalet[`ChartDataLabel`](../chartdatalabel/) i den här samlingen. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Ger åtkomst till teckensnittsformateringen för dataetiketterna för hela serien. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Ger åtkomst till fyllnings- och linjeformatering av dataetiketterna. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Returer[`ChartDataLabel`](../chartdatalabel/) för det angivna indexet. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Får en[`ChartNumberFormat`](../chartnumberformat/) instans som tillåter att ställa in talformat för dataetiketterna för hela serien . |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabelcollection/orientation/) { get; set; } | Hämtar eller ställer in textorienteringen för dataetiketterna i hela serien. |
| [Position](../../aspose.words.drawing.charts/chartdatalabelcollection/position/) { get; set; } | Hämtar eller anger positionen för dataetiketterna. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabelcollection/rotation/) { get; set; } | Hämtar eller ställer in rotationen av dataetiketterna för hela serien i grader. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Hämtar eller ställer in strängavgränsare som används för dataetiketter för hela serien. Standardvärdet är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procentandel, då en radbrytning ska användas istället. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Gör det möjligt att ange om bubbelstorleken ska visas för dataetiketterna i hela serien. Gäller endast bubbeldiagram. Standardvärdet är`falsk` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Gör det möjligt att ange om kategorinamnet ska visas för dataetiketterna för hela serien. Standardvärdet är`falsk` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Gör det möjligt att ange om värden från dataetikettintervallet ska visas i dataetiketterna för hela serien. Standardvärdet är`falsk` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Gör det möjligt att ange om hänvisningslinjer för dataetiketter ska visas för dataetiketterna i hela serien. Standardvärdet är`falsk` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Gör det möjligt att ange om förklaringsnyckeln ska visas för dataetiketterna för hela serien. Standardvärdet är`falsk` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Gör det möjligt att ange om procentvärde ska visas för dataetiketterna för hela serien. Standardvärdet är`falsk` Gäller endast cirkeldiagram. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Returnerar eller anger ett booleskt värde för att ange visningsbeteendet för serienamnet för dataetiketterna för hela serien. `sann` för att visa seriens namn;`falsk` att dölja. Som standard`falsk` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Gör det möjligt att ange om värden ska visas i dataetiketterna för hela serien. Standardvärdet är`falsk` . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Rensar formatet för alla[`ChartDataLabel`](../chartdatalabel/) i den här samlingen. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Returnerar ett uppräknarobjekt. |

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

* class [ChartDataLabel](../chartdatalabel/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
