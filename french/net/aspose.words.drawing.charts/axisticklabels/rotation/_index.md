---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words pour .NET
description: Ajustez la rotation des étiquettes AxisTickLabels pour une lisibilité optimale. Personnalisez l'angle des étiquettes de graduation en degrés pour améliorer la clarté et l'attrait visuel de votre graphique.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

Obtient ou définit la rotation des étiquettes de graduation en degrés.

```csharp
public int Rotation { get; set; }
```

## Remarques

La plage de valeurs acceptables s'étend de -180 à 180 inclus. La valeur par défaut est 0.

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

* class [AxisTickLabels](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
