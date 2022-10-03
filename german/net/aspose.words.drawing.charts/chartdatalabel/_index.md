---
title: ChartDataLabel
second_title: Aspose.Words für .NET-API-Referenz
description: Stellt eine Datenbeschriftung auf einem Diagrammpunkt oder einer Trendlinie dar.
type: docs
weight: 630
url: /de/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Stellt eine Datenbeschriftung auf einem Diagrammpunkt oder einer Trendlinie dar.

```csharp
public class ChartDataLabel
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Gibt den Index des enthaltenden Elements an. Dieser Index bestimmt, auf welche der untergeordneten Sammlungen des übergeordneten Elements sich dieses Element bezieht. Der Standardwert ist 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Ruft/setzt ein Flag, das angibt, ob dieses Label ausgeblendet ist. Der Standardwert ist **FALSCH** . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Gibt wahr zurück, wenn diese Datenbeschriftung etwas anzuzeigen hat. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Gibt das Zahlenformat des übergeordneten Elements zurück. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Ermittelt oder legt das Zeichenfolgentrennzeichen fest, das für die Datenbeschriftungen in einem Diagramm verwendet wird. Der Standardwert ist ein Komma, außer bei Tortendiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, wenn stattdessen ein Zeilenumbruch verwendet werden soll. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Gilt nur für Blasendiagramme. Standardwert ist falsch. |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist falsch. |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen angezeigt werden sollen. Standardwert ist falsch. |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Ermöglicht die Angabe, ob Datenbeschriftungs-Führungslinien angezeigt werden müssen. Standardwert ist falsch. |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Ermöglicht die Angabe, ob der Legendenschlüssel für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Standardwert ist falsch. |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Ermöglicht die Angabe, ob Prozentwerte für die Datenbeschriftungen in einem Diagramm angezeigt werden sollen. Standardwert ist falsch. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Gibt einen booleschen Wert zurück oder legt ihn fest, um das Verhalten der Reihennamenanzeige für die Datenbeschriftungen in einem Diagramm anzugeben. True, um den Seriennamen anzuzeigen. Falsch zu verstecken. Standardmäßig false. |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen angezeigt werden sollen. Standardwert ist falsch. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Löscht das Format dieses Datenlabels. Die Eigenschaften werden auf die Standardwerte gesetzt, die in der übergeordneten Etikettensammlung data definiert sind. |

### Bemerkungen

Auf einer Reihe, die[`ChartDataLabel`](./chartdatalabel/) Objekt ist ein Mitglied von[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Die[`ChartDataLabelCollection`](../chartdatalabelcollection/) enthält ein[`ChartDataLabel`](./chartdatalabel/) Objekt für jeden Punkt.

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

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
