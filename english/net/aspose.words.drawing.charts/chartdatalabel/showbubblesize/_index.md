---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words for .NET
description: Discover how the ShowBubbleSize property enhances your Bubble charts by displaying data label sizes. Optimize your visual data representation today!
type: docs
weight: 130
url: /net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is `false`.

```csharp
public bool ShowBubbleSize { get; set; }
```

## Examples

Shows how to use 3D effects with bubble charts.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.That(chart.Series.Count, Is.EqualTo(1));
Assert.That(chart.Series[0].Name, Is.EqualTo("Y-Values"));
Assert.That(chart.Series[0].Bubble3D, Is.True);

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

* class [ChartDataLabel](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
