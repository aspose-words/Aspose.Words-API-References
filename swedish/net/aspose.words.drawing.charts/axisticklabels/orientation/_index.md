---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words för .NET
description: Anpassa orienteringen på dina AxisTickLabels för optimal läsbarhet. Justera enkelt textriktningen på tick-etiketter för att förbättra din datavisualisering!
type: docs
weight: 50
url: /sv/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Hämtar eller anger orienteringen för texten i tick-etiketten.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Anmärkningar

Standardvärdet ärHorizontal.

Observera att vissa[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) Värden påverkar inte orienteringen av skalstämpeln text i värdeaxlar.

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
