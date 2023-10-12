---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words for .NET
description: ChartFormat IsDefined property. Gets a flag indicating whether any format is defined in C#.
type: docs
weight: 20
url: /net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Gets a flag indicating whether any format is defined.

```csharp
public bool IsDefined { get; }
```

## Examples

Shows how to reset the fill to the default value defined in the series.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);            

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### See Also

* class [ChartFormat](../)
* namespace [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* assembly [Aspose.Words](../../../)
