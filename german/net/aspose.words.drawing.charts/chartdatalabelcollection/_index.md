---
title: ChartDataLabelCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert eine Sammlung vonChartDataLabel./chartdatalabel .
type: docs
weight: 640
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Repräsentiert eine Sammlung von[`ChartDataLabel`](../chartdatalabel) .

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count) { get; } | Gibt die Anzahl von zurück[`ChartDataLabel`](../chartdatalabel) in dieser Sammlung. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item) { get; } | gibt zurück[`ChartDataLabel`](../chartdatalabel) für den angegebenen Index. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat) { get; } | Ruft ein[`ChartNumberFormat`](../chartnumberformat) Instanz, die es ermöglicht, das Zahlenformat für die Datenetiketten der gesamten Serie festzulegen. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator) { get; set; } | Ermittelt oder setzt Zeichenfolgentrennzeichen, die für die Datenbeschriftungen der gesamten Serie verwendet werden. Der Standardwert ist ein Komma, außer bei Tortendiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, wenn stattdessen ein Zeilenumbruch verwendet werden soll. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize) { get; set; } | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Gilt nur für Blasendiagramme. Standardwert ist **FALSCH** . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname) { get; set; } | Ermöglicht die Angabe, ob der Kategoriename für die Datenetiketten der gesamten Serie angezeigt werden soll. Standardwert ist **FALSCH** . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange) { get; set; } | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Standardwert ist **FALSCH** . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines) { get; set; } | Ermöglicht die Angabe, ob Führungslinien der Datenbeschriftung für die Datenbeschriftungen der gesamten Serie angezeigt werden müssen. Der Standardwert ist **FALSCH** . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey) { get; set; } | Ermöglicht die Angabe, ob der Legendenschlüssel für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Standardwert ist **FALSCH** . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage) { get; set; } | Ermöglicht die Angabe, ob Prozentwerte für die Datenetiketten der gesamten Serie angezeigt werden sollen. Standardwert ist **FALSCH** . Gilt nur für Kreisdiagramme. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname) { get; set; } | Gibt einen booleschen Wert zurück oder legt ihn fest, um das Anzeigeverhalten der Reihennamen für die Datenbeschriftungen der gesamten Reihe anzugeben.  **WAHR**um den Seriennamen anzuzeigen. **FALSCH** verstecken. Standardmäßig **FALSCH** . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue) { get; set; } | Ermöglicht die Angabe, ob Werte in den Datenetiketten der gesamten Serie angezeigt werden sollen. Standardwert ist **FALSCH** . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat)() | Löscht alle Formate[`ChartDataLabel`](../chartdatalabel) in dieser Sammlung. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator)() | Gibt ein Aufzählungsobjekt zurück. |

### Beispiele

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

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

    // Datenbeschriftungen auf jede Reihe im Diagramm anwenden.
    // Diese Beschriftungen erscheinen neben jedem Datenpunkt im Diagramm und zeigen seinen Wert an.
    foreach (ChartSeries series in chart.Series)
    {
        ApplyDataLabels(series, 4, "000.0", ", ");
        Assert.AreEqual(4, series.DataLabels.Count);
    }

    // Ändern Sie die Trennzeichenfolge für jedes Datenlabel in einer Reihe.
    using (IEnumerator<ChartDataLabel> enumerator = chart.Series[0].DataLabels.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.AreEqual(", ", enumerator.Current.Separator);
            enumerator.Current.Separator = " & ";
        }
    }

    // Für ein sauberer aussehendes Diagramm können wir Datenbeschriftungen einzeln entfernen.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Wir können auch eine ganze Reihe ihrer Datenetiketten auf einmal entfernen.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Wenden Sie Datenetiketten mit benutzerdefiniertem Zahlenformat und Trennzeichen auf mehrere Datenpunkte in einer Reihe an.
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

### Siehe auch

* class [ChartDataLabel](../chartdatalabel)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
