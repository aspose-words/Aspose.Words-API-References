---
title: ChartDataLabelCollection.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Orientation ChartDataLabelCollection pour personnaliser facilement l'orientation du texte de vos étiquettes de données, améliorant ainsi la clarté et l'impact de votre graphique.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/orientation/
---
## ChartDataLabelCollection.Orientation property

Obtient ou définit l'orientation du texte des étiquettes de données de la série entière.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Remarques

La valeur par défaut estHorizontal .

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

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
