---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words für .NET
description: Passen Sie die Drehung der AxisTickLabels für optimale Lesbarkeit an. Passen Sie die Winkel der Teilstrichbeschriftungen in Grad an, um die Übersichtlichkeit und Optik Ihres Diagramms zu verbessern.
type: docs
weight: 70
url: /de/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Ruft die Drehung der Teilstrichbeschriftungen in Grad ab oder legt sie fest.

```csharp
public int Rotation { get; set; }
```

## Bemerkungen

Der zulässige Wertebereich liegt zwischen -180 und 180 (einschließlich). Der Standardwert ist 0.

## Beispiele

Zeigt, wie die Ausrichtung und Drehung der Achsenmarkierungsbeschriftungen geändert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Säulendiagramm einfügen.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Ausrichtung und Drehung der Achsenmarkierungsbeschriftung festlegen.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Siehe auch

* class [AxisTickLabels](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
