---
title: ChartDataPointCollection Class
linktitle: ChartDataPointCollection
articleTitle: ChartDataPointCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Drawing.Charts.ChartDataPointCollection, Ihren Schlüssel zur mühelosen Verwaltung von ChartDataPoint-Sammlungen für eine verbesserte Datenvisualisierung.
type: docs
weight: 980
url: /de/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Stellt eine Sammlung von[`ChartDataPoint`](../chartdatapoint/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | Gibt die Anzahl der[`ChartDataPoint`](../chartdatapoint/) in dieser Sammlung. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Rückgaben[`ChartDataPoint`](../chartdatapoint/) für den angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Löscht das Format aller[`ChartDataPoint`](../chartdatapoint/) in dieser Sammlung. |
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(*int, int*) | Kopiert das Format vom Quelldatenpunkt zum Zieldatenpunkt. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(*int*) | Ruft ein Flag ab, das angibt, ob der Datenpunkt am angegebenen Index das Standardformat hat. |

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

* class [ChartDataPoint](../chartdatapoint/)
* namensraum [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../)
