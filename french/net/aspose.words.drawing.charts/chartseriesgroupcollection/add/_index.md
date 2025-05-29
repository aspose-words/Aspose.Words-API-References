---
title: ChartSeriesGroupCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Découvrez la méthode ChartSeriesGroupCollection Add pour ajouter sans effort de nouveaux groupes de séries, améliorant ainsi vos capacités de visualisation de données.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/chartseriesgroupcollection/add/
---
## ChartSeriesGroupCollection.Add method

Ajoute un nouveau groupe de séries du type de série spécifié à cette collection.

```csharp
public ChartSeriesGroup Add(ChartSeriesType seriesType)
```

## Remarques

Les graphiques combinés peuvent contenir des groupes de séries uniquement des types suivants : aires, barres, colonnes, lignes, secteurs, nuages de points, types radar et actions (à l'exception des types de séries 3D correspondants).

## Exemples

Montre comment travailler avec l’axe secondaire du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Supprimer la série générée par défaut.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Créer un groupe de séries supplémentaire, également de type ligne.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Spécifiez l'utilisation des axes secondaires pour le nouveau groupe de séries.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Masquer l'axe X secondaire.
newSeriesGroup.AxisX.Hidden = true;
// Définir le titre de l'axe Y secondaire.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Ajouter une série au nouveau groupe de séries.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Voir également

* class [ChartSeriesGroup](../../chartseriesgroup/)
* enum [ChartSeriesType](../../chartseriestype/)
* class [ChartSeriesGroupCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
