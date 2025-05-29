---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words für .NET
description: Passen Sie die Ausrichtung Ihrer AxisTickLabels für optimale Lesbarkeit an. Passen Sie die Textrichtung der Teilstriche einfach an, um Ihre Datenvisualisierung zu verbessern!
type: docs
weight: 50
url: /de/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Ruft die Ausrichtung des Teilstrichbeschriftungstextes ab oder legt sie fest.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Bemerkungen

Der Standardwert istHorizontal.

Beachten Sie, dass einige[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) Werte haben keinen Einfluss auf die Ausrichtung der Teilstrichbeschriftung text in Werteachsen.

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
