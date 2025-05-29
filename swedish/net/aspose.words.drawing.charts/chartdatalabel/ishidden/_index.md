---
title: ChartDataLabel.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartDataLabel IsHidden för att enkelt kontrollera etiketternas synlighet i dina diagram. Förbättra din datapresentation med den här enkla funktionen!
type: docs
weight: 40
url: /sv/net/aspose.words.drawing.charts/chartdatalabel/ishidden/
---
## ChartDataLabel.IsHidden property

Hämtar/ställer in en flagga som anger om denna etikett är dold. Standardvärdet är`falsk` .

```csharp
public bool IsHidden { get; set; }
```

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

* class [ChartDataLabel](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
