---
title: MarkerSymbol Enum
linktitle: MarkerSymbol
articleTitle: MarkerSymbol
second_title: Aspose.Words för .NET
description: Aspose.Words.Drawing.Charts.MarkerSymbol uppräkning. Anger markörsymbolstil i C#.
type: docs
weight: 920
url: /sv/net/aspose.words.drawing.charts/markersymbol/
---
## MarkerSymbol enumeration

Anger markörsymbolstil.

```csharp
public enum MarkerSymbol
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Default | `0` | Anger att en standardmarkörsymbol ska ritas vid varje datapunkt. |
| Circle | `1` | Anger att en cirkel ska ritas vid varje datapunkt. |
| Dash | `2` | Anger att ett streck ska ritas vid varje datapunkt. |
| Diamond | `3` | Anger att en diamant ska dras vid varje datapunkt. |
| Dot | `4` | Anger att en punkt ska ritas vid varje datapunkt. |
| None | `5` | Anger att ingenting ska ritas vid varje datapunkt. |
| Picture | `6` | Anger att en bild ska ritas vid varje datapunkt. |
| Plus | `7` | Anger att ett plus ska dras vid varje datapunkt. |
| Square | `8` | Anger att en kvadrat ska ritas vid varje datapunkt. |
| Star | `9` | Anger att en stjärna ska ritas vid varje datapunkt. |
| Triangle | `10` | Anger att en triangel ska ritas vid varje datapunkt. |
| X | `11` | Anger att ett X ska ritas vid varje datapunkt. |

## Exempel

Visar hur man arbetar med datapunkter på ett linjediagram.

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

    // Framhäv diagrammets datapunkter genom att få dem att visas som diamantformer.
    foreach (ChartSeries series in chart.Series) 
        ApplyDataPoints(series, 4, MarkerSymbol.Diamond, 15);

    // Jämna ut linjen som representerar den första dataserien.
    chart.Series[0].Smooth = true;

    // Kontrollera att datapunkter för den första serien inte kommer att invertera sina färger om värdet är negativt.
    using (IEnumerator<ChartDataPoint> enumerator = chart.Series[0].DataPoints.GetEnumerator())
    {
        while (enumerator.MoveNext())
        {
            Assert.False(enumerator.Current.InvertIfNegative);
        }
    }

    // För en renare graf kan vi rensa format individuellt.
    chart.Series[1].DataPoints[2].ClearFormat();

    // Vi kan också ta bort en hel serie datapunkter på en gång.
    chart.Series[2].DataPoints.ClearFormat();

    doc.Save(ArtifactsDir + "Charts.ChartDataPoint.docx");
}

/// <summary>
/// Tillämpar ett antal datapunkter på en serie.
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

### Se även

* namnutrymme [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../)
