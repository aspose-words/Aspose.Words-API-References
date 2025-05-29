---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.ShapeTextOrientation, um die Textausrichtung in Formen einfach zu steuern und so das Design und die Lesbarkeit Ihres Dokuments zu verbessern.
type: docs
weight: 1680
url: /de/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Gibt die Ausrichtung von Text in Formen an.

```csharp
public enum ShapeTextOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | `0` | Der Text ist horizontal angeordnet (lr-tb). |
| Downward | `1` | Der Text wird um 90 Grad nach rechts gedreht, um von oben nach unten (tb-rl) angezeigt zu werden. |
| Upward | `2` | Der Text wird um 90 Grad nach links gedreht, um von unten nach oben (bt-lr) angezeigt zu werden. |
| VerticalFarEast | `3` | Fernöstliche Zeichen werden vertikal angezeigt, anderer Text wird um 90 Grad nach rechts gedreht, um von oben nach unten angezeigt zu werden (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Fernöstliche Zeichen werden vertikal angezeigt, anderer Text wird um 90 Grad nach rechts gedreht, um vertikal von oben nach unten und dann horizontal von links nach rechts (tb-lr-v) angezeigt zu werden. |
| WordArtVertical | `5` | Der Text ist vertikal, mit einem Buchstaben über dem anderen. |
| WordArtVerticalRightToLeft | `6` | Der Text ist vertikal, mit einem Buchstaben über dem anderen, dann horizontal von rechts nach links. |

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

* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
