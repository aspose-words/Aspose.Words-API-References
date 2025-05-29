---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Methode „SetDefaultFill“ von ChartFormat die Füllung Ihres Diagrammelements mühelos auf den ursprünglichen Standardwert zurücksetzen.
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

Setzt die Füllung des Diagrammelements auf den Standardwert zurück.

```csharp
public void SetDefaultFill()
```

## Beispiele

Zeigt, wie die Füllung auf den in der Serie definierten Standardwert zurückgesetzt wird.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### Siehe auch

* class [ChartFormat](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
