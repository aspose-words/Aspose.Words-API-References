---
title: ChartDataLabelCollection.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words för .NET
description: Justera rotationen på din ChartDataLabelCollection för optimal synlighet. Anpassa dataetikettvinklarna för att förbättra diagrammets läsbarhet och effekt.
type: docs
weight: 80
url: /sv/net/aspose.words.drawing.charts/chartdatalabelcollection/rotation/
---
## ChartDataLabelCollection.Rotation property

Hämtar eller ställer in rotationen av dataetiketterna för hela serien i grader.

```csharp
public int Rotation { get; set; }
```

## Anmärkningar

Intervallet för acceptabla värden är från -180 till och med 180. Standardvärdet är 0.

Om[`Orientation`](../orientation/) värdet ärHorizontal, etikettformer, om de finns, roteras tillsammans med etiketttexten. Annars roteras endast etiketttexten.

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

* class [ChartDataLabelCollection](../)
* namnutrymme [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* hopsättning [Aspose.Words](../../../)
