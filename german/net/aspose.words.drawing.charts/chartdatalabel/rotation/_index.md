---
title: ChartDataLabel.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Rotationseigenschaft von ChartDataLabel, um Beschriftungswinkel in Ihren Diagrammen einfach anzupassen. Verbessern Sie die Datenvisualisierung mit präziser Steuerung!
type: docs
weight: 110
url: /de/net/aspose.words.drawing.charts/chartdatalabel/rotation/
---
## ChartDataLabel.Rotation property

Ruft die Drehung des Etiketts in Grad ab oder legt sie fest.

```csharp
public int Rotation { get; set; }
```

## Bemerkungen

Der zulässige Wertebereich liegt zwischen -180 und 180 (einschließlich). Der Standardwert ist 0.

Wenn die[`Orientation`](../orientation/) Wert istHorizontalwird die Beschriftungsform (sofern vorhanden) zusammen mit dem Beschriftungstext gedreht. Andernfalls wird nur der Beschriftungstext gedreht.

## Beispiele

Zeigt, wie Ausrichtung und Drehung für Datenbeschriftungen geändert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Datenbeschriftungen anzeigen.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Form der Datenbeschriftung definieren.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Datenbeschriftungsausrichtung und -drehung für die gesamte Reihe festlegen.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Ausrichtung und Drehung des ersten Datenetiketts ändern.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Siehe auch

* class [ChartDataLabel](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
