---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Drawing.ShapeTextOrientation-uppräkningen för att enkelt styra textorientering i former, vilket förbättrar dokumentdesignen och läsbarheten.
type: docs
weight: 1680
url: /sv/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Anger textens orientering i former.

```csharp
public enum ShapeTextOrientation
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Horizontal | `0` | Texten är ordnad horisontellt (l-tb). |
| Downward | `1` | Texten roteras 90 grader åt höger för att visas uppifrån och ned (tb-rl). |
| Upward | `2` | Texten roteras 90 grader åt vänster för att visas nerifrån och upp (bt-lr). |
| VerticalFarEast | `3` | Tecken från Fjärran Östern visas vertikalt, annan text roteras 90 grader åt höger för att visas uppifrån och ned (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Tecken från Fjärran Östern visas vertikalt, annan text roteras 90 grader åt höger för att visas uppifrån och ned vertikalt, sedan från vänster till höger horisontellt (tb-lr-v). |
| WordArtVertical | `5` | Texten är vertikal, med en bokstav ovanpå den andra. |
| WordArtVerticalRightToLeft | `6` | Texten är vertikal, med en bokstav ovanpå den andra, sedan från höger till vänster horisontellt. |

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

* namnutrymme [Aspose.Words.Drawing](../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../)
