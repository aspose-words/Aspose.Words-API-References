---
title: ChartAxis.Crosses
linktitle: Crosses
articleTitle: Crosses
second_title: Aspose.Words pour .NET
description: Découvrez comment ChartAxis améliore la visualisation des données en définissant des intersections d'axes pour des informations plus claires et des présentations plus percutantes.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartaxis/crosses/
---
## ChartAxis.Crosses property

Spécifie comment cet axe croise l'axe perpendiculaire.

```csharp
public AxisCrosses Crosses { get; set; }
```

## Remarques

La valeur par défaut estAutomatic.

La propriété n'est pas prise en charge par les nouveaux graphiques MS Office 2016.

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

* enum [AxisCrosses](../../axiscrosses/)
* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
