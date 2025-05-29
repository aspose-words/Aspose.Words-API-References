---
title: ShapeTextOrientation Enum
linktitle: ShapeTextOrientation
articleTitle: ShapeTextOrientation
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.ShapeTextOrientation pour contrôler facilement l'orientation du texte dans les formes, améliorant ainsi la conception et la lisibilité de votre document.
type: docs
weight: 1680
url: /fr/net/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enumeration

Spécifie l'orientation du texte dans les formes.

```csharp
public enum ShapeTextOrientation
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Horizontal | `0` | Le texte est disposé horizontalement (lr-tb). |
| Downward | `1` | Le texte est tourné de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl). |
| Upward | `2` | Le texte est tourné de 90 degrés vers la gauche pour apparaître de bas en haut (bt-lr). |
| VerticalFarEast | `3` | Les caractères d'Extrême-Orient apparaissent verticalement, les autres textes sont tournés de 90 degrés vers la droite pour apparaître de haut en bas (tb-rl-v). |
| VerticalRotatedFarEast | `4` | Les caractères d'Extrême-Orient apparaissent verticalement, les autres textes sont tournés de 90 degrés vers la droite pour apparaître de haut en bas verticalement, puis de gauche à droite horizontalement (tb-lr-v). |
| WordArtVertical | `5` | Le texte est vertical, avec une lettre sur l'autre. |
| WordArtVerticalRightToLeft | `6` | Le texte est vertical, avec une lettre sur l'autre, puis de droite à gauche horizontalement. |

## Exemples

Montre comment modifier l'orientation et la rotation des étiquettes de données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
ChartSeries series = shape.Chart.Series[0];
ChartDataLabelCollection dataLabels = series.DataLabels;

// Afficher les étiquettes de données.
series.HasDataLabels = true;
dataLabels.ShowValue = true;
dataLabels.ShowCategoryName = true;

// Définir la forme de l'étiquette de données.
dataLabels.Format.ShapeType = ChartShapeType.UpArrow;
dataLabels.Format.Stroke.Fill.Solid(Color.DarkBlue);

// Définir l'orientation et la rotation des étiquettes de données pour toute la série.
dataLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
dataLabels.Rotation = -45;

// Modifier l'orientation et la rotation de la première étiquette de données.
dataLabels[0].Orientation = ShapeTextOrientation.Horizontal;
dataLabels[0].Rotation = 45;

doc.Save(ArtifactsDir + "Charts.LabelOrientationRotation.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
