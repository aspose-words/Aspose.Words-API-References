---
title: AxisTickLabels Class
linktitle: AxisTickLabels
articleTitle: AxisTickLabels
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.AxisTickLabels, conçue pour améliorer les étiquettes de graduation des axes de votre graphique avec des propriétés personnalisables pour une meilleure visualisation des données.
type: docs
weight: 840
url: /fr/net/aspose.words.drawing.charts/axisticklabels/
---
## AxisTickLabels class

Représente les propriétés des étiquettes de graduation des axes.

```csharp
public class AxisTickLabels
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Alignment](../../aspose.words.drawing.charts/axisticklabels/alignment/) { get; set; } | Obtient ou définit l'alignement du texte des étiquettes de graduation des axes. |
| [Font](../../aspose.words.drawing.charts/axisticklabels/font/) { get; } | Donne accès au formatage de police des étiquettes de graduation. |
| [IsAutoSpacing](../../aspose.words.drawing.charts/axisticklabels/isautospacing/) { get; set; } | Obtient ou définit un indicateur indiquant s'il faut utiliser l'intervalle automatique pour dessiner les étiquettes de graduation. |
| [Offset](../../aspose.words.drawing.charts/axisticklabels/offset/) { get; set; } | Obtient ou définit la distance des étiquettes de graduation par rapport à l'axe. |
| [Orientation](../../aspose.words.drawing.charts/axisticklabels/orientation/) { get; set; } | Obtient ou définit l'orientation du texte de l'étiquette de graduation. |
| [Position](../../aspose.words.drawing.charts/axisticklabels/position/) { get; set; } | Obtient ou définit la position des étiquettes de graduation sur l'axe. |
| [Rotation](../../aspose.words.drawing.charts/axisticklabels/rotation/) { get; set; } | Obtient ou définit la rotation des étiquettes de graduation en degrés. |
| [Spacing](../../aspose.words.drawing.charts/axisticklabels/spacing/) { get; set; } | Obtient ou définit l'intervalle auquel les étiquettes de graduation sont dessinées. |

## Exemples

Montre comment insérer un graphique et modifier l'apparence de ses axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// Effacez la série de données de démonstration du graphique pour démarrer avec un graphique propre.
chart.Series.Clear();

// Insérer une série de graphiques avec des catégories pour l'axe X et des valeurs numériques respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 640, 320, 280, 120, 150 });

// Les axes du graphique disposent de diverses options qui peuvent modifier leur apparence,
// comme leur direction, les graduations des unités majeures/mineures et les graduations.
ChartAxis xAxis = chart.AxisX;
xAxis.CategoryType = AxisCategoryType.Category;
xAxis.Crosses = AxisCrosses.Minimum;
xAxis.ReverseOrder = false;
xAxis.MajorTickMark = AxisTickMark.Inside;
xAxis.MinorTickMark = AxisTickMark.Cross;
xAxis.MajorUnit = 10.0d;
xAxis.MinorUnit = 15.0d;
xAxis.TickLabels.Offset = 50;
xAxis.TickLabels.Position = AxisTickLabelPosition.Low;
xAxis.TickLabels.IsAutoSpacing = false;
xAxis.TickMarkSpacing = 1;

Assert.AreEqual(doc, xAxis.Document);

ChartAxis yAxis = chart.AxisY;
yAxis.CategoryType = AxisCategoryType.Automatic;
yAxis.Crosses = AxisCrosses.Maximum;
yAxis.ReverseOrder = true;
yAxis.MajorTickMark = AxisTickMark.Inside;
yAxis.MinorTickMark = AxisTickMark.Cross;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 20.0d;
yAxis.TickLabels.Position = AxisTickLabelPosition.NextToAxis;
yAxis.TickLabels.Alignment = ParagraphAlignment.Center;
yAxis.TickLabels.Font.Color = Color.Red;
yAxis.TickLabels.Spacing = 1;

// Les graphiques à colonnes n'ont pas d'axe Z.
Assert.Null(chart.AxisZ);

doc.Save(ArtifactsDir + "Charts.AxisProperties.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
