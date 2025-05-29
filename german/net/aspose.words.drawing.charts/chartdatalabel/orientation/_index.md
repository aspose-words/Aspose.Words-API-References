---
title: ChartDataLabel.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ChartDataLabel-Ausrichtung“, um die Ausrichtung von Beschriftungstexten einfach anzupassen und so die Datenvisualisierung und Übersichtlichkeit Ihrer Diagramme zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.drawing.charts/chartdatalabel/orientation/
---
## ChartDataLabel.Orientation property

Ruft die Ausrichtung des Beschriftungstextes ab oder legt sie fest.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Bemerkungen

Der Standardwert istHorizontal .

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabel](../)
* namensraum [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Montage [Aspose.Words](../../../)
