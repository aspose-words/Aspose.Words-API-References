---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words för .NET
description: Upptäck om ett format är definierat med egenskapen ChartFormat IsDefined. Lås upp sömlös formateringskontroll för dina diagram idag!
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Hämtar en flagga som anger om något format är definierat.

```csharp
public bool IsDefined { get; }
```

## Exempel

Visar hur man återställer fyllningen till standardvärdet som definierats i serien.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Se även

* class [ChartFormat](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
