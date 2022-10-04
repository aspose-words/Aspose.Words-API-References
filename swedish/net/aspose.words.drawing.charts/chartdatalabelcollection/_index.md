---
title: ChartDataLabelCollection
second_title: Aspose.Words för .NET API Referens
description: Representerar en samling avChartDataLabel./chartdatalabel/ .
type: docs
weight: 640
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Representerar en samling av[`ChartDataLabel`](../chartdatalabel/) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Returnerar antalet[`ChartDataLabel`](../chartdatalabel/) i den här samlingen. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Returnerar[`ChartDataLabel`](../chartdatalabel/) för det angivna indexet. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Får en[`ChartNumberFormat`](../chartnumberformat/) instans som gör det möjligt att ställa in nummerformat för dataetiketterna för hela serien. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Hämtar eller ställer in strängseparator som används för dataetiketterna för hela serien. Standard är ett kommatecken, förutom för cirkeldiagram som endast visar kategorinamn och procent, då en radbrytning ska användas istället. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Tillåter att ange om bubbelstorlek ska visas för dataetiketterna för hela serien. Gäller endast bubbeldiagram. Standardvärdet är **falsk** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Gör det möjligt att ange om kategorinamnet ska visas för dataetiketterna för hela serien. Standardvärdet är **falsk** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Gör det möjligt att ange om värden från dataetikettintervallet ska visas i dataetiketterna för hela serien. Standardvärdet är **falsk** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Tillåter att ange om dataetikettledarlinjer behöver visas för dataetiketterna för hela serien. Standardvärdet är **falsk** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Gör det möjligt att ange om förklaringsnyckeln ska visas för dataetiketterna för hela serien. Standardvärdet är **falsk** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Gör det möjligt att ange om ett procentvärde ska visas för dataetiketterna för hela serien. Standardvärdet är **falsk** . Gäller endast cirkeldiagram. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Returnerar eller ställer in en boolesk för att indikera visningsbeteendet för serienamnet för dataetiketterna för hela serien.  **Sann**för att visa serienamnet. **Falsk** att gömma. Som standard **falsk** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Gör det möjligt att ange om värden ska visas i dataetiketterna för hela serien. Standardvärdet är **falsk** . |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Rensar alla format[`ChartDataLabel`](../chartdatalabel/) i den här samlingen. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt. |

### Exempel

Visar hur man applicerar etiketter på datapunkter i ett linjediagram.

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

* class [ChartDataLabel](../chartdatalabel/)
* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
