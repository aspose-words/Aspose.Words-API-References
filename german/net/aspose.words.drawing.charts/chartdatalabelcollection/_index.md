---
title: Class ChartDataLabelCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartDataLabelCollection klas. Stellt eine Sammlung von darChartDataLabel .
type: docs
weight: 680
url: /de/net/aspose.words.drawing.charts/chartdatalabelcollection/
---
## ChartDataLabelCollection class

Stellt eine Sammlung von dar[`ChartDataLabel`](../chartdatalabel/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartDataLabelCollection : IEnumerable<ChartDataLabel>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatalabelcollection/count/) { get; } | Gibt die Anzahl zurück[`ChartDataLabel`](../chartdatalabel/) in dieser Sammlung. |
| [Font](../../aspose.words.drawing.charts/chartdatalabelcollection/font/) { get; } | Bietet Zugriff auf die Schriftartformatierung der Datenbeschriftungen der gesamten Serie. |
| [Format](../../aspose.words.drawing.charts/chartdatalabelcollection/format/) { get; } | Bietet Zugriff auf die Füll- und Zeilenformatierung der Datenbeschriftungen. |
| [Item](../../aspose.words.drawing.charts/chartdatalabelcollection/item/) { get; } | Gibt zurück[`ChartDataLabel`](../chartdatalabel/) für den angegebenen Index. |
| [NumberFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/numberformat/) { get; } | Ruft eine ab[`ChartNumberFormat`](../chartnumberformat/) Instanz, die es ermöglicht, das Zahlenformat für die Datenbeschriftungen der gesamten Serie festzulegen. |
| [Separator](../../aspose.words.drawing.charts/chartdatalabelcollection/separator/) { get; set; } | Ruft das für die Datenbeschriftungen der gesamten Serie verwendete Zeichenfolgentrennzeichen ab oder legt dieses fest. Der Standardwert ist ein Komma, außer bei Kreisdiagrammen, die nur den Kategorienamen und den Prozentsatz anzeigen, bei denen stattdessen ein Zeilenumbruch verwendet werden soll. |
| [ShowBubbleSize](../../aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/) { get; set; } | Ermöglicht die Angabe, ob die Blasengröße für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Gilt nur für Blasendiagramme. Der Standardwert ist`FALSCH` . |
| [ShowCategoryName](../../aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/) { get; set; } | Ermöglicht die Angabe, ob der Kategoriename für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowDataLabelsRange](../../aspose.words.drawing.charts/chartdatalabelcollection/showdatalabelsrange/) { get; set; } | Ermöglicht die Angabe, ob Werte aus dem Datenbeschriftungsbereich in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Der Standardwert ist`FALSCH` . |
| [ShowLeaderLines](../../aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/) { get; set; } | Ermöglicht die Angabe, ob Führungslinien für Datenbeschriftungen für die Datenbeschriftungen der gesamten Serie angezeigt werden müssen. Der Standardwert ist`FALSCH` . |
| [ShowLegendKey](../../aspose.words.drawing.charts/chartdatalabelcollection/showlegendkey/) { get; set; } | Ermöglicht die Angabe, ob der Legendenschlüssel für die Datenbeschriftungen der gesamten Serie angezeigt werden soll. Der Standardwert ist`FALSCH` . |
| [ShowPercentage](../../aspose.words.drawing.charts/chartdatalabelcollection/showpercentage/) { get; set; } | Ermöglicht die Angabe, ob Prozentwerte für die Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Der Standardwert ist`FALSCH` . Gilt nur für Kreisdiagramme. |
| [ShowSeriesName](../../aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/) { get; set; } | Gibt einen booleschen Wert zurück oder legt ihn fest, um das Anzeigeverhalten des Seriennamens für die Datenbeschriftungen der gesamten Serie anzugeben. `WAHR` um den Seriennamen anzuzeigen;`FALSCH` verstecken. Standardmäßig`FALSCH` . |
| [ShowValue](../../aspose.words.drawing.charts/chartdatalabelcollection/showvalue/) { get; set; } | Ermöglicht die Angabe, ob Werte in den Datenbeschriftungen der gesamten Serie angezeigt werden sollen. Der Standardwert ist`FALSCH` . |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatalabelcollection/clearformat/)() | Löscht das gesamte Format[`ChartDataLabel`](../chartdatalabel/) in dieser Sammlung. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatalabelcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |

### Beispiele

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

* class [ChartDataLabel](../chartdatalabel/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)


