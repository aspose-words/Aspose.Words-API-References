---
title: Font
second_title: Aspose.Words for .NET API Reference
description: ChartDataLabel property. Provides access to the font formatting of this data label in C#.
type: docs
weight: 10
url: /net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Provides access to the font formatting of this data label.

```csharp
public Font Font { get; }
```

## Examples

Shows how to use 3D effects with bubble charts.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Apply a data label to each bubble that displays its diameter.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### See Also

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* namespace [Aspose.Words.Drawing.Charts](../../chartdatalabel/)
* assembly [Aspose.Words](../../../)
