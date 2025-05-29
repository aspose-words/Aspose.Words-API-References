---
title: ChartDataPoint.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Formateigenschaft „ChartDataPoint“ Ihre Datenvisualisierung mit anpassbaren Füll- und Linienstilen für wirkungsvolle Präsentationen verbessert.
type: docs
weight: 30
url: /de/net/aspose.words.drawing.charts/chartdatapoint/format/
---
## ChartDataPoint.Format property

Bietet Zugriff auf die Füll- und Linienformatierung dieses Datenpunkts.

```csharp
public ChartFormat Format { get; }
```

## Beispiele

Zeigt, wie Sie die individuelle Formatierung für Kategorien eines Säulendiagramms festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// Standardmäßig generierte Serien löschen.
chart.Series.Clear();

// Neue Serie hinzufügen.
ChartSeries series = chart.Series.Add("Series 1",
    new[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 1, 2, 3, 4 });

// Spaltenformatierung festlegen.
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[1].Format.Fill.ForeColor = Color.Red;
dataPoints[2].Format.Fill.ForeColor = Color.Yellow;
dataPoints[3].Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.DataPointsFormatting.docx");
```

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

* class [ChartFormat](../../chartformat/)
* class [ChartDataPoint](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
