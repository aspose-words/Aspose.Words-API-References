---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words för .NET
description: Justera AxisTickLabels rotation för optimal läsbarhet. Anpassa tick-etiketternas vinklar i grader för att förbättra diagrammets tydlighet och visuella tilltal.
type: docs
weight: 70
url: /sv/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Hämtar eller ställer in rotationen av tacketiketterna i grader.

```csharp
public int Rotation { get; set; }
```

## Anmärkningar

Intervallet för acceptabla värden är från -180 till och med 180. Standardvärdet är 0.

## Exempel

Visar hur man ändrar orientering och rotation för axeltacketiketter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett kolumndiagram.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Ställ in orientering och rotation för axeltacketiketter.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Se även

* class [AxisTickLabels](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
