---
title: ChartDataPoint Class
linktitle: ChartDataPoint
articleTitle: ChartDataPoint
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartDataPoint, um einzelne Diagrammdatenpunkte einfach zu formatieren und so Ihre Datenvisualisierung präzise zu verbessern.
type: docs
weight: 970
url: /de/net/aspose.words.drawing.charts/chartdatapoint/
---
## ChartDataPoint class

Ermöglicht die Festlegung der Formatierung eines einzelnen Datenpunkts im Diagramm.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartDataPoint : IChartDataPoint
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Bubble3D](../../aspose.words.drawing.charts/chartdatapoint/bubble3d/) { get; set; } | Gibt an, ob auf die Blasen im Blasendiagramm ein 3D-Effekt angewendet werden soll. |
| [Explosion](../../aspose.words.drawing.charts/chartdatapoint/explosion/) { get; set; } | Gibt den Betrag an, um den der Datenpunkt von der Mitte des Kreisdiagramms verschoben werden soll. Kann negativ sein. Negativ bedeutet, dass die Eigenschaft nicht festgelegt ist und keine Explosion angewendet werden soll. Gilt nur für Kreisdiagramme. |
| [Format](../../aspose.words.drawing.charts/chartdatapoint/format/) { get; } | Bietet Zugriff auf die Füll- und Linienformatierung dieses Datenpunkts. |
| [Index](../../aspose.words.drawing.charts/chartdatapoint/index/) { get; } | Index des Datenpunkts, auf den dieses Objekt die Formatierung anwendet. |
| [InvertIfNegative](../../aspose.words.drawing.charts/chartdatapoint/invertifnegative/) { get; set; } | Gibt an, ob das übergeordnete Element seine Farben invertieren soll, wenn der Wert negativ ist. |
| [Marker](../../aspose.words.drawing.charts/chartdatapoint/marker/) { get; } | Gibt die Datenmarkierung des Diagramms an. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapoint/clearformat/)() | Löscht das Format dieses Datenpunkts. Die Eigenschaften werden auf die in der übergeordneten Reihe definierten Standardwerte gesetzt. |

## Bemerkungen

In einer Serie, die`ChartDataPoint` Objekt ist ein Mitglied der[`ChartDataPointCollection`](../chartdatapointcollection/) . Die[`ChartDataPointCollection`](../chartdatapointcollection/) enthält eine`ChartDataPoint` Objekt für jeden Punkt.

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

* interface [IChartDataPoint](../ichartdatapoint/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
