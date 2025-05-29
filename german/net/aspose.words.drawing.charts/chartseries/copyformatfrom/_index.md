---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „ChartSeries CopyFormatFrom“, um Datenpunktformate mühelos nach Index zu replizieren und so die Effizienz und Konsistenz Ihrer Diagrammerstellung zu verbessern.
type: docs
weight: 190
url: /de/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

Kopiert das Standarddatenpunktformat vom Datenpunkt mit dem angegebenen Index.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## Beispiele

Zeigt, wie das Datenpunktformat kopiert wird.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// Holen Sie sich das Diagramm und die Reihe, um das Format zu aktualisieren.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// Kopiere das Format des Datenpunkts mit Index 1 in den Datenpunkt mit Index 2
// sodass Datenpunkt 2 genauso aussieht wie Datenpunkt 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// Kopiere das Format des Datenpunkts mit Index 0 in die Serienvorgaben, sodass alle Datenpunkte
// in der Reihe mit dem Standardformat sehen sie genauso aus wie der Datenpunkt 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### Siehe auch

* class [ChartSeries](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
