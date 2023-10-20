---
title: ChartDataLabel Class
linktitle: ChartDataLabel
articleTitle: ChartDataLabel
second_title: Aspose.Words für .NET
description: Aspose.Words.Drawing.Charts.ChartDataLabel klas. Stellt die Datenbeschriftung auf einem Diagrammpunkt oder einer Trendlinie dar in C#.
type: docs
weight: 670
url: /de/net/aspose.words.drawing.charts/chartdatalabel/
---
## ChartDataLabel class

Stellt die Datenbeschriftung auf einem Diagrammpunkt oder einer Trendlinie dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartDataLabel
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartdatalabel/font/) { get; } | Bietet Zugriff auf die Schriftartformatierung dieser Datenbeschriftung. |
| [Format](../../aspose.words.drawing.charts/chartdatalabel/format/) { get; } | Bietet Zugriff auf die Füll- und Zeilenformatierung der Datenbeschriftung. |
| [Index](../../aspose.words.drawing.charts/chartdatalabel/index/) { get; } | Gibt den Index des enthaltenden Elements an. Dieser Index soll bestimmen, für welche untergeordnete Sammlung des übergeordneten Elements dieses Element gilt. Der Standardwert ist 0. |
| [IsHidden](../../aspose.words.drawing.charts/chartdatalabel/ishidden/) { get; set; } | Ruft/setzt ein Flag, das angibt, ob diese Bezeichnung ausgeblendet ist. Der Standardwert ist`FALSCH` . |
| [IsVisible](../../aspose.words.drawing.charts/chartdatalabel/isvisible/) { get; } | Gibt zurück`WAHR` ob dieses Datenetikett etwas anzuzeigen hat. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabel/numberformat/) { get; } | Gibt das Zahlenformat des übergeordneten Elements zurück. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabel/separator/) { get; set; } | Ruft das für die Datenbeschriftungen in einem Diagramm verwendete Zeichenfolgentrennzeichen ab oder legt dieses fest. Der Standardwert ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, bei denen stattdessen ein Zeilenumbruch verwendet werden soll. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabel/showbubblesize/) { get; set; } | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Gilt nur für Blasendiagramme. Der Standardwert ist`FALSCH` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabel/showcategoryname/) { get; set; } | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabel/showdatalabelsrange/) { get; set; } | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen angezeigt werden sollen. Der Standardwert ist`FALSCH` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabel/showleaderlines/) { get; set; } | Ermöglicht die Angabe, ob Führungslinien für Datenbeschriftungen angezeigt werden müssen. Der Standardwert ist`FALSCH` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabel/showlegendkey/) { get; set; } | Ermöglicht die Angabe, ob der Legendenschlüssel für die Datenbeschriftungen in einem Diagramm angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabel/showpercentage/) { get; set; } | Ermöglicht die Angabe, ob Prozentwerte für die Datenbeschriftungen in einem Diagramm angezeigt werden sollen. Der Standardwert ist`FALSCH` . |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabel/showseriesname/) { get; set; } | Gibt einen booleschen Wert zurück oder legt ihn fest, um das Anzeigeverhalten des Reihennamens für die Datenbeschriftungen in einem Diagramm anzugeben. `WAHR` um den Seriennamen anzuzeigen;`FALSCH` verstecken. Standardmäßig`FALSCH` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabel/showvalue/) { get; set; } | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen angezeigt werden sollen. Der Standardwert ist`FALSCH` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabel/clearformat/)() | Löscht das Format dieser Datenbeschriftung. Die Eigenschaften werden auf die Standardwerte gesetzt, die in der übergeordneten data Label-Sammlung definiert sind. |

## Bemerkungen

Auf einer Serie, die`ChartDataLabel` Das Objekt ist Mitglied von[`ChartDataLabelCollection`](../chartdatalabelcollection/) . Die[`ChartDataLabelCollection`](../chartdatalabelcollection/) enthält ein`ChartDataLabel` Objekt für jeden Punkt.

## Beispiele

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

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

    // Anwenden von Datenbeschriftungen auf jede Reihe im Diagramm.
    // Diese Beschriftungen werden neben jedem Datenpunkt im Diagramm angezeigt und zeigen seinen Wert an.
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

    // Für ein übersichtlicheres Diagramm können wir Datenbeschriftungen einzeln entfernen.
    chart.Series[1].DataLabels[2].ClearFormat();

    // Wir können auch eine ganze Reihe ihrer Datenbeschriftungen auf einmal entfernen.
    chart.Series[2].DataLabels.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.DataLabels.docx");
}

/// <summary>
/// Datenbeschriftungen mit benutzerdefiniertem Zahlenformat und Trennzeichen auf mehrere Datenpunkte in einer Reihe anwenden.
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
