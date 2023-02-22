---
title: Enum AxisCrosses
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.AxisCrosses énumération. Spécifie les points de croisement possibles pour un axe.
type: docs
weight: 530
url: /fr/net/aspose.words.drawing.charts/axiscrosses/
---
## AxisCrosses enumeration

Spécifie les points de croisement possibles pour un axe.

```csharp
public enum AxisCrosses
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Automatic | `0` | L'axe des abscisses coupe au point zéro de l'axe des valeurs (si possible), ou à la valeur minimale si le minimum est supérieur à zéro, ou au maximum si le maximum est inférieur à zéro. |
| Maximum | `1` | Un axe perpendiculaire coupe à la valeur maximale de l'axe. |
| Minimum | `2` | Un axe perpendiculaire coupe à la valeur minimale de l'axe. |
| Custom | `3` | Un axe perpendiculaire coupe à la valeur spécifiée de l'axe. |

### Exemples

Montre comment insérer un graphique et modifier l'apparence de ses axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Insère une série de graphiques avec des catégories pour l'axe X et des valeurs numériques respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Les axes du graphique ont diverses options qui peuvent changer leur apparence,
// tels que leur direction, les graduations des unités majeures/mineures et les graduations.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabelOffset = 50;
xAxis.TickLabelPosition = AxisTickLabelPosition.Low;
xAxis.TickLabelSpacingIsAuto = false;
xAxis.TickMarkSpacing = 1;

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabelPosition = AxisTickLabelPosition.NextToAxis;

// Les histogrammes n'ont pas d'axe Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


