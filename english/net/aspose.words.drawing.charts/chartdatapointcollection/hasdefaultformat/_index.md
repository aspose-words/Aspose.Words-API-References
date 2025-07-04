---
title: ChartDataPointCollection.HasDefaultFormat
linktitle: HasDefaultFormat
articleTitle: HasDefaultFormat
second_title: Aspose.Words for .NET
description: Discover if the data point at a specific index in ChartDataPointCollection uses the default format. Enhance your data visualization today!
type: docs
weight: 60
url: /net/aspose.words.drawing.charts/chartdatapointcollection/hasdefaultformat/
---
## ChartDataPointCollection.HasDefaultFormat method

Gets a flag indicating whether the data point at the specified index has default format.

```csharp
public bool HasDefaultFormat(int dataPointIndex)
```

## Examples

Shows how to copy data point format.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Get the chart and series to update format.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.That(dataPoints.HasDefaultFormat(0), Is.True);
Assert.That(dataPoints.HasDefaultFormat(1), Is.False);

// Copy format of the data point with index 1 to the data point with index 2
// so that the data point 2 looks the same as the data point 1.
dataPoints.CopyFormat(0, 1);

Assert.That(dataPoints.HasDefaultFormat(0), Is.True);
Assert.That(dataPoints.HasDefaultFormat(1), Is.True);

// Copy format of the data point with index 0 to the series defaults so that all data points
// in the series that have the default format look the same as the data point 0.
series.CopyFormatFrom(1);

Assert.That(dataPoints.HasDefaultFormat(0), Is.True);
Assert.That(dataPoints.HasDefaultFormat(1), Is.True);

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### See Also

* class [ChartDataPointCollection](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
