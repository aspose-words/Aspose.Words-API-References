---
title: ChartDataPointCollection.CopyFormat
linktitle: CopyFormat
articleTitle: CopyFormat
second_title: Aspose.Words for .NET
description: Effortlessly copy formatting between data points with the ChartDataPointCollection CopyFormat method. Enhance your data visualization today!
type: docs
weight: 40
url: /net/aspose.words.drawing.charts/chartdatapointcollection/copyformat/
---
## ChartDataPointCollection.CopyFormat method

Copies format from the source data point to the destination data point.

```csharp
public void CopyFormat(int sourceIndex, int destinationIndex)
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
