---
title: AxisScaling.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: Découvrez la propriété AxisScaling Type pour personnaliser facilement l'échelle de vos axes. Améliorez la visualisation de vos données grâce à des paramètres flexibles pour une clarté optimale.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

Obtient ou définit le type de mise à l'échelle de l'axe.

```csharp
public AxisScaleType Type { get; set; }
```

## Remarques

LeLinearla valeur est la seule autorisée dans les nouveaux graphiques MS Office 2016.

## Exemples

Montre comment appliquer une mise à l’échelle logarithmique à un axe de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Effacez la série de données de démonstration du graphique pour démarrer avec un graphique propre.
chart.Series.Clear();

// Insérer une série avec des coordonnées X/Y pour cinq points.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// La mise à l'échelle de l'axe X est linéaire par défaut,
// affichage de valeurs incrémentées uniformément qui couvrent notre plage de valeurs X (0, 1, 2, 3...).
// Un axe linéaire n'est pas idéal pour nos valeurs Y
// car les points avec les valeurs Y les plus petites seront plus difficiles à lire.
// Une échelle logarithmique avec une base de 20 (1, 20, 400, 8000...)
// répartira les points tracés, nous permettant de lire plus facilement leurs valeurs sur le graphique.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Voir également

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
