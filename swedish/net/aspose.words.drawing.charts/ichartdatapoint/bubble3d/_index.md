---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words för .NET
description: Upptäck egenskapen IChartDataPoint Bubble3D för att förbättra dina bubbeldiagram med fantastiska 3D-effekter för mer engagerande datavisualisering.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Anger om bubblorna i bubbeldiagrammet ska ha en 3D-effekt.

```csharp
public bool Bubble3D { get; set; }
```

## Exempel

Visar hur man använder 3D-effekter med bubbeldiagram.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Använd en dataetikett för varje bubbla som visar dess diameter.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Se även

* interface [IChartDataPoint](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
