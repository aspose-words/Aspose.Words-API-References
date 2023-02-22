---
title: ChartAxis.MajorUnit
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartAxis propriété. Renvoie ou définit la distance entre les graduations principales.
type: docs
weight: 100
url: /fr/net/aspose.words.drawing.charts/chartaxis/majorunit/
---
## ChartAxis.MajorUnit property

Renvoie ou définit la distance entre les graduations principales.

```csharp
public double MajorUnit { get; set; }
```

### Remarques

La plage valide d'une valeur est supérieure à zéro. La propriété a un effet pour la catégorie de temps et les axes de valeur .

La définition de cette propriété définit le[`MajorUnitIsAuto`](../majorunitisauto/) propriété à **faux**.

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

* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartaxis/)
* Assemblée [Aspose.Words](../../../)


