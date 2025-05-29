---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ChartDataLabelCollection Orientation för att enkelt anpassa textorienteringen för dina dataetiketter, vilket förbättrar diagrammets tydlighet och effekt.
type: docs
weight: 60
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

Hämtar eller ställer in textorienteringen för dataetiketterna i hela serien.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Anmärkningar

Standardvärdet ärHorizontal .

## Exempel

Visar hur man ändrar orientering och rotation för dataetiketter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Visa dataetiketter.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Definiera formen på dataetiketten.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Ange dataetikettens orientering och rotation för hela serien.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Ändra orientering och rotation för den första dataetiketten.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Se även

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
