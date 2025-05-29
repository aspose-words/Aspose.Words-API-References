---
title: ChartSeries Class
linktitle: ChartSeries
articleTitle: ChartSeries
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartSeries, Ihren Schlüssel zur Verbesserung der Diagrammreiheneigenschaften für die dynamische Dokumenterstellung und -visualisierung.
type: docs
weight: 1070
url: /de/net/aspose.words.drawing.charts/chartseries/
---
## ChartSeries class

Stellt die Eigenschaften der Diagrammreihe dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartSeries : IChartDataPoint
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartseries/bubble3d/) { get; set; } | Gibt an, ob auf die Blasen im Blasendiagramm ein 3D-Effekt angewendet werden soll. |
| [BubbleSizes](../../aspose.words.drawing.charts/chartseries/bubblesizes/) { get; } | Ruft eine Sammlung von Blasengrößen für diese Diagrammreihe ab. |
| [DataLabels](../../aspose.words.drawing.charts/chartseries/datalabels/) { get; } | Gibt die Einstellungen für die Datenbeschriftungen für die gesamte Reihe an. |
| [DataPoints](../../aspose.words.drawing.charts/chartseries/datapoints/) { get; } | Gibt eine Sammlung von Formatierungsobjekten für alle Datenpunkte in dieser Reihe zurück. |
| [Explosion](../../aspose.words.drawing.charts/chartseries/explosion/) { get; set; } | Gibt den Betrag an, um den der Datenpunkt von der Mitte des Kreisdiagramms verschoben werden soll. Kann negativ sein. Negativ bedeutet, dass die Eigenschaft nicht festgelegt ist und keine Explosion angewendet werden soll. Gilt nur für Kreisdiagramme. |
| [Format](../../aspose.words.drawing.charts/chartseries/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung der Serie. |
| [HasDataLabels](../../aspose.words.drawing.charts/chartseries/hasdatalabels/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, ob Datenbeschriftungen für die Reihe angezeigt werden. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartseries/invertifnegative/) { get; set; } | Gibt an, ob das übergeordnete Element seine Farben invertieren soll, wenn der Wert negativ ist. |
| [LegendEntry](../../aspose.words.drawing.charts/chartseries/legendentry/) { get; } | Ruft einen Legendeneintrag für diese Diagrammreihe ab. |
| [Marker](../../aspose.words.drawing.charts/chartseries/marker/) { get; } | Gibt eine Datenmarkierung an. Die Markierung wird bei Bedarf automatisch erstellt. |
| [Name](../../aspose.words.drawing.charts/chartseries/name/) { get; set; } | Ruft den Namen der Serie ab oder legt ihn fest. Wenn der Name nicht explizit festgelegt wird, wird er mithilfe des Index generiert. Standardmäßig wird „Serie plus eins basierend auf dem Index“ zurückgegeben. |
| [SeriesType](../../aspose.words.drawing.charts/chartseries/seriestype/) { get; } | Ruft den Typ dieser Diagrammreihe ab. |
| [Smooth](../../aspose.words.drawing.charts/chartseries/smooth/) { get; set; } | Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mit Catmull-Rom-Splines geglättet werden soll. |
| [XValues](../../aspose.words.drawing.charts/chartseries/xvalues/) { get; } | Ruft eine Sammlung von X-Werten für diese Diagrammreihe ab. |
| [YValues](../../aspose.words.drawing.charts/chartseries/yvalues/) { get; } | Ruft eine Sammlung von Y-Werten für diese Diagrammreihe ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add)(*[ChartXValue](../chartxvalue/)*) | Fügt den angegebenen X-Wert zur Diagrammreihe hinzu. Wenn die Reihe Y-Werte und Blasengrößen unterstützt, sind diese für den X-Wert leer. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_1)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Fügt der Diagrammreihe die angegebenen X- und Y-Werte hinzu. |
| [Add](../../aspose.words.drawing.charts/chartseries/add/#add_2)(*[ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Fügt der Diagrammreihe den angegebenen X-Wert, Y-Wert und die Blasengröße hinzu. |
| [Clear](../../aspose.words.drawing.charts/chartseries/clear/)() | Entfernt alle Datenwerte aus der Diagrammreihe. Das Format aller einzelnen Datenpunkte und Datenbeschriftungen wird gelöscht. |
| [ClearValues](../../aspose.words.drawing.charts/chartseries/clearvalues/)() | Entfernt alle Datenwerte aus der Diagrammreihe, wobei das Format der Datenpunkte und Datenbeschriftungen erhalten bleibt. |
| [CopyFormatFrom](../../aspose.words.drawing.charts/chartseries/copyformatfrom/)(*int*) | Kopiert das Standarddatenpunktformat vom Datenpunkt mit dem angegebenen Index. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert)(*int, [ChartXValue](../chartxvalue/)*) | Fügt den angegebenen X-Wert am angegebenen Index in die Diagrammreihe ein. Wenn die Reihe Y-Werte und Blasengrößen unterstützt, sind diese für den X-Wert leer. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_1)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/)*) | Fügt die angegebenen X- und Y-Werte am angegebenen Index in die Diagrammreihe ein. |
| [Insert](../../aspose.words.drawing.charts/chartseries/insert/#insert_2)(*int, [ChartXValue](../chartxvalue/), [ChartYValue](../chartyvalue/), double*) | Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße am angegebenen Index in die Diagrammreihe ein. |
| [Remove](../../aspose.words.drawing.charts/chartseries/remove/)(*int*) | Entfernt den X-Wert, den Y-Wert und die Blasengröße (sofern unterstützt) aus der Diagrammreihe am angegebenen Index. Der entsprechende Datenpunkt und die Datenbeschriftung werden ebenfalls entfernt. |

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

* interface [IChartDataPoint](../ichartdatapoint/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
