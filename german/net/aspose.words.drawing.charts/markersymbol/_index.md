---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words für .NET
description: Erkunden Sie die Aufzählung Aspose.Words.Drawing.Charts.MarkerSymbol für anpassbare Markierungsstile, die Ihre Diagrammdarstellung verbessern und die Datenpräsentation verbessern.
type: docs
weight: 1240
url: /de/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Gibt den Stil des Markierungssymbols an.

```csharp
public enum MarkerSymbol
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Default | `0` | Gibt an, dass an jedem Datenpunkt ein Standardmarkierungssymbol gezeichnet werden soll. |
| Circle | `1` | Gibt an, dass an jedem Datenpunkt ein Kreis gezeichnet werden soll. |
| Dash | `2` | Gibt an, dass an jedem Datenpunkt ein Strich gezeichnet werden soll. |
| Diamond | `3` | Gibt an, dass an jedem Datenpunkt eine Raute gezeichnet werden soll. |
| Dot | `4` | Gibt an, dass an jedem Datenpunkt ein Punkt gezeichnet werden soll. |
| None | `5` | Gibt an, dass an jedem Datenpunkt nichts gezeichnet werden soll. |
| Picture | `6` | Gibt an, dass an jedem Datenpunkt ein Bild gezeichnet werden soll. |
| Plus | `7` | Gibt an, dass an jedem Datenpunkt ein Pluszeichen angezeigt werden soll. |
| Square | `8` | Gibt an, dass an jedem Datenpunkt ein Quadrat gezeichnet werden soll. |
| Star | `9` | Gibt an, dass an jedem Datenpunkt ein Stern gezeichnet werden soll. |
| Triangle | `10` | Gibt an, dass an jedem Datenpunkt ein Dreieck gezeichnet werden soll. |
| X | `11` | Gibt an, dass an jedem Datenpunkt ein X gezeichnet werden soll. |

## Beispiele

Zeigt, wie mit Datenpunkten in einem Liniendiagramm gearbeitet wird.

```csharp
public void ChartDataPoint()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    Shape shape = builder.InsertChart(ChartType.Line, 500, 350);
    Chart chart = shape.Chart;

    Assert.AreEqual(3, chart.Series.Count);
    Assert.AreEqual("Series 1", chart.Series[0].Name);
    Assert.AreEqual("Series 2", chart.Series[1].Name);
    Assert.AreEqual("Series 3", chart.Series[2].Name);

    // Heben Sie die Datenpunkte des Diagramms hervor, indem Sie sie als Rautenformen darstellen.
    foreach (ChartSeries series in chart.Series)
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Glätten Sie die Linie, die die erste Datenreihe darstellt.
    chart.Series[0].Smooth = true;

    // Überprüfen Sie, ob die Datenpunkte der ersten Reihe ihre Farben nicht invertieren, wenn der Wert negativ ist.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    ChartDataPoint dataPoint = chart.Series[1].DataPoints[2];
    dataPoint.Format.Fill.Color = Color.Red;

    // Für ein übersichtlicheres Diagramm können wir das Format einzeln löschen.
    dataPoint.ClearFormat();

    // Wir können auch eine ganze Reihe von Datenpunkten auf einmal entfernen.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Wendet eine Anzahl Datenpunkte auf eine Reihe an.
/// </summary>
private static void ApplyDataPoints(ChartSeries series, int dataPointsCount, MarkerSymbol markerSymbol, int dataPointSize)
{
    for (int i = 0; i < dataPointsCount; i++)
    {
        ChartDataPoint point = series.DataPoints[i];
        point.Marker.Symbol = markerSymbol;
        point.Marker.Size = dataPointSize;

        Assert.AreEqual(i, point.Index);
    }
}
```

### Siehe auch

* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
