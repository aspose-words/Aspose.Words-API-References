---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words för .NET
description: Upptäck hur du använder metoden ChartFormat SetDefaultFill för att enkelt återställa fyllningen i ett diagramelement till dess ursprungliga standardvärde.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Återställer fyllningen av diagramelementet till standardvärdet.

```csharp
public void SetDefaultFill()
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
