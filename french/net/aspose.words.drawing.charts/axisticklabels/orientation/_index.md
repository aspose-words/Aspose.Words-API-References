---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words pour .NET
description: Personnalisez l'orientation de vos étiquettes AxisTickLabels pour une lisibilité optimale. Ajustez facilement l'orientation du texte des étiquettes de graduation pour améliorer la visualisation de vos données !
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

Obtient ou définit l'orientation du texte de l'étiquette de graduation.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## Remarques

La valeur par défaut estHorizontal.

Notez que certains[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) les valeurs n'affectent pas l'orientation de l'étiquette de graduation text dans les axes de valeurs.

## Exemples

Montre comment modifier l'orientation et la rotation des étiquettes de graduation des axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique à colonnes.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// Définir l'orientation et la rotation de l'étiquette de graduation de l'axe.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### Voir également

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
