---
title: Class ChartDataPointCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.Charts.ChartDataPointCollection klas. Stellt eine Sammlung von a darChartDataPoint .
type: docs
weight: 700
url: /de/net/aspose.words.drawing.charts/chartdatapointcollection/
---
## ChartDataPointCollection class

Stellt eine Sammlung von a dar[`ChartDataPoint`](../chartdatapoint/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Diagrammen](https://docs.aspose.com/words/net/working-with-charts/) Dokumentationsartikel.

```csharp
public class ChartDataPointCollection : IEnumerable<ChartDataPoint>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartdatapointcollection/count/) { get; } | Gibt die Anzahl zurück[`ChartDataPoint`](../chartdatapoint/) in dieser Sammlung. |
| [Item](../../aspose.words.drawing.charts/chartdatapointcollection/item/) { get; } | Gibt zurück[`ChartDataPoint`](../chartdatapoint/) für den angegebenen Index. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [ClearFormat](../../aspose.words.drawing.charts/chartdatapointcollection/clearformat/)() | Löscht das gesamte Format[`ChartDataPoint`](../chartdatapoint/) in dieser Sammlung. |
| [CopyFormat](../../aspose.words.drawing.charts/chartdatapointcollection/copyformat/)(int, int) |  |
| [GetEnumerator](../../aspose.words.drawing.charts/chartdatapointcollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück. |
| [HasDefaultFormat](../../aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/)(int) |  |

### Beispiele

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

    // Betonen Sie die Datenpunkte des Diagramms, indem Sie sie als Rautenformen erscheinen lassen.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Glätten Sie die Linie, die die erste Datenreihe darstellt.
    chart.Series[0].Smooth = true;

    // Stellen Sie sicher, dass die Farben der Datenpunkte für die erste Serie nicht invertiert werden, wenn der Wert negativ ist.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // Für ein übersichtlicheres Diagramm können wir das Format einzeln löschen.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Wir können auch eine ganze Reihe von Datenpunkten auf einmal entfernen.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Wendet eine Reihe von Datenpunkten auf eine Reihe an.
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


