---
title: Enum AxisScaleType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.AxisScaleType énumération. Spécifie les types déchelle possibles pour un axe.
type: docs
weight: 560
url: /fr/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

Spécifie les types d'échelle possibles pour un axe.

```csharp
public enum AxisScaleType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Linear | `0` | Mise à l'échelle linéaire. |
| Logarithmic | `1` | Mise à l'échelle logarithmique. |

### Exemples

Montre comment appliquer une mise à l’échelle logarithmique à un axe de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Insère une série avec des coordonnées X/Y pour cinq points.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// La mise à l'échelle de l'axe X est linéaire par défaut,
// affichant des valeurs incrémentées uniformément qui couvrent notre plage de valeurs X (0, 1, 2, 3...).
// Un axe linéaire n'est pas idéal pour nos valeurs Y
// puisque les points avec les valeurs Y les plus petites seront plus difficiles à lire.
// Une échelle logarithmique en base 20 (1, 20, 400, 8000...)
// répartira les points tracés, nous permettant de lire plus facilement leurs valeurs sur le graphique.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


