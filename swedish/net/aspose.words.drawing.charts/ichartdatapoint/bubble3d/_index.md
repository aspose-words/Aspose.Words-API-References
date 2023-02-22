---
title: IChartDataPoint.Bubble3D
second_title: Aspose.Words för .NET API Referens
description: IChartDataPoint fast egendom. Anger om bubblorna i bubbeldiagrammet ska ha en 3Deffekt på dem.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Anger om bubblorna i bubbeldiagrammet ska ha en 3D-effekt på dem.

```csharp
public bool Bubble3D { get; set; }
```

### Exempel

Visar hur man använder 3D-effekter med bubbeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Applicera en dataetikett på varje bubbla som visar dess diameter.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Se även

* interface [IChartDataPoint](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* hopsättning [Aspose.Words](../../../)


