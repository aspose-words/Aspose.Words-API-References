---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words für .NET
description: Ermitteln Sie, ob ein Format mit der Eigenschaft „ChartFormat IsDefined“ definiert ist. Schalten Sie noch heute die nahtlose Formatierungskontrolle für Ihre Diagramme frei!
type: docs
weight: 20
url: /de/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

Ruft ein Flag ab, das angibt, ob ein Format definiert ist.

```csharp
public bool IsDefined { get; }
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
