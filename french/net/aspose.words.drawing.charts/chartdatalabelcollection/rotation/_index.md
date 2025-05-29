---
title: ChartDataLabelCollection.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words pour .NET
description: Ajustez la rotation de votre ChartDataLabelCollection pour une visibilité optimale. Personnalisez l'angle des étiquettes de données pour améliorer la lisibilité et l'impact de votre graphique.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/rotation/
---
## ChartDataLabelCollection.Rotation property

Obtient ou définit la rotation des étiquettes de données de la série entière en degrés.

```csharp
public int Rotation { get; set; }
```

## Remarques

La plage de valeurs acceptables s'étend de -180 à 180 inclus. La valeur par défaut est 0.

Si le[`Orientation`](../orientation/) la valeur estHorizontalLes formes d'étiquettes, si elles existent, sont pivotées avec le texte de l'étiquette. Sinon, seul le texte de l'étiquette est pivoté.

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

* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
