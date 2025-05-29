---
title: ChartSeries.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: Aspose.Words für .NET
description: Entdecken Sie die ChartSeries Explosion-Eigenschaft, um Kreisdiagramm-Datenpunkte anzupassen. Passen Sie die Positionierung für wirkungsvolle Visualisierungen an – perfekt für Data Storytelling!
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartseries/explosion/
---
## ChartSeries.Explosion property

Gibt den Betrag an, um den der Datenpunkt von der Mitte des Kreisdiagramms verschoben werden soll. Kann negativ sein. Negativ bedeutet, dass die Eigenschaft nicht festgelegt ist und keine Explosion angewendet werden soll. Gilt nur für Kreisdiagramme.

```csharp
public int Explosion { get; set; }
```

## Beispiele

Zeigt, wie Datenpunkten in einem Liniendiagramm Beschriftungen zugewiesen werden.

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

    // Datenbeschriftungen auf jede Reihe im Diagramm anwenden.
    // Diese Beschriftungen werden neben jedem Datenpunkt im Diagramm angezeigt und zeigen dessen Wert an.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Ändern Sie die Trennzeichenfolge für jede Datenbeschriftung in einer Reihe.
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

    // Für ein übersichtlicheres Diagramm können wir die Datenbeschriftungen einzeln entfernen.
    dataLabel.ClearFormat();

    // Wir können auch eine ganze Reihe ihrer Datenbeschriftungen auf einmal entfernen.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Wenden Sie Datenbeschriftungen mit benutzerdefiniertem Zahlenformat und Trennzeichen auf mehrere Datenpunkte in einer Reihe an.
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

### Siehe auch

* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
