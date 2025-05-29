---
title: ChartDataLabelCollection Class
linktitle: ChartDataLabelCollection
articleTitle: ChartDataLabelCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.ChartDataLabelCollection zur effizienten Verwaltung von Diagrammdatenbeschriftungen. Verbessern Sie noch heute die visuelle Attraktivität Ihres Dokuments!
type: docs
weight: 940
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Stellt eine Sammlung von[`ChartDataLabel`](../chartdatalabel/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Gibt die Anzahl der[`ChartDataLabel`](../chartdatalabel/) in dieser Sammlung. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Bietet Zugriff auf die Schriftformatierung der Datenbeschriftungen der gesamten Serie. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung der Datenbeschriftungen. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Rückgaben[`ChartDataLabel`](../chartdatalabel/) für den angegebenen Index. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Erhält eine[`ChartNumberFormat`](../chartnumberformat/) Instanz, die das Festlegen des Zahlenformats für die Datenbeschriftungen der gesamten Serie ermöglicht. |
| [Orientation](../../aspose.words.drawing.charts/chartdatalabelcollection/orientation/) { get; set; } | Ruft die Textausrichtung der Datenbeschriftungen der gesamten Reihe ab oder legt sie fest. |
| [Position](../../aspose.words.drawing.charts/chartdatalabelcollection/position/) { get; set; } | Ruft die Position der Datenbeschriftungen ab oder legt sie fest. |
| [Rotation](../../aspose.words.drawing.charts/chartdatalabelcollection/rotation/) { get; set; } | Ruft die Drehung der Datenbeschriftungen der gesamten Reihe in Grad ab oder legt sie fest. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Ruft das für die Datenbeschriftungen der gesamten Reihe verwendete Zeichenfolgentrennzeichen ab oder legt es fest. Der Standardwert ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, bei denen stattdessen ein Zeilenumbruch verwendet werden soll. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen der gesamten Reihe angezeigt werden soll. Gilt nur für Blasendiagramme. Der Standardwert ist`FALSCH` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen der gesamten Reihe angezeigt werden sollen. Der Standardwert ist`FALSCH` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Ermöglicht die Angabe, ob Führungslinien für die Datenbeschriftungen der gesamten Reihe angezeigt werden sollen. Der Standardwert ist`FALSCH` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Ermöglicht die Angabe, ob der Legendenschlüssel für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Ermöglicht die Angabe, ob der Prozentwert für die Datenbeschriftungen der gesamten Reihe angezeigt werden soll. Der Standardwert ist`FALSCH` . Gilt nur für Kreisdiagramme. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Gibt einen Booleschen Wert zurück oder legt ihn fest, um das Anzeigeverhalten des Seriennamens für die Datenbeschriftungen der gesamten Serie anzugeben. `WAHR` um den Seriennamen anzuzeigen;`FALSCH` zu verbergen. Standardmäßig`FALSCH` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen der gesamten Reihe angezeigt werden sollen. Der Standardwert ist`FALSCH` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Löscht das Format aller[`ChartDataLabel`](../chartdatalabel/) in dieser Sammlung. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

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

* class [ChartDataLabel](../chartdatalabel/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
