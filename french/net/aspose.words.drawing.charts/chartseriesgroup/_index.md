---
title: ChartSeriesGroup Class
linktitle: ChartSeriesGroup
articleTitle: ChartSeriesGroup
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartSeriesGroup, qui simplifie la gestion des propriétés des séries de graphiques pour une visualisation et une analyse des données améliorées.
type: docs
weight: 1090
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/
---
## ChartSeriesGroup class

Représente les propriétés d'un groupe de séries de graphiques, c'est-à-dire les propriétés des séries de graphiques du même type associées aux mêmes axes.

```csharp
public class ChartSeriesGroup
```

## Propriétés

| Nom | La description |
| --- | --- |
| [AxisGroup](../../aspose.words.drawing.charts/chartseriesgroup/axisgroup/) { get; set; } | Obtient ou définit le groupe d'axes auquel appartient ce groupe de séries. |
| [AxisX](../../aspose.words.drawing.charts/chartseriesgroup/axisx/) { get; } | Donne accès aux propriétés de l'axe X de ce groupe de séries. |
| [AxisY](../../aspose.words.drawing.charts/chartseriesgroup/axisy/) { get; } | Donne accès aux propriétés de l'axe Y de ce groupe de séries. |
| [BubbleScale](../../aspose.words.drawing.charts/chartseriesgroup/bubblescale/) { get; set; } | Obtient ou définit la taille des bulles en pourcentage de leur taille par défaut. |
| [DoughnutHoleSize](../../aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/) { get; set; } | Obtient ou définit la taille du trou du graphique en anneau parent sous forme de pourcentage. |
| [FirstSliceAngle](../../aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/) { get; set; } | Obtient ou définit l'angle, en degrés, de la première tranche du graphique à secteurs parent. |
| [GapWidth](../../aspose.words.drawing.charts/chartseriesgroup/gapwidth/) { get; set; } | Obtient ou définit le pourcentage de largeur d'espace entre les éléments du graphique. |
| [Overlap](../../aspose.words.drawing.charts/chartseriesgroup/overlap/) { get; set; } | Obtient ou définit le pourcentage de chevauchement des barres ou des colonnes de la série. |
| [SecondSectionSize](../../aspose.words.drawing.charts/chartseriesgroup/secondsectionsize/) { get; set; } | Obtient ou définit la taille de la section secondaire du graphique à secteurs sous forme de pourcentage. |
| [Series](../../aspose.words.drawing.charts/chartseriesgroup/series/) { get; } | Obtient une collection de séries appartenant à ce groupe de séries. |
| [SeriesType](../../aspose.words.drawing.charts/chartseriesgroup/seriestype/) { get; } | Obtient le type de série de graphiques inclus dans ce groupe. |

## Remarques

Les graphiques combinés contiennent plusieurs groupes de séries de graphiques, avec un groupe distinct pour chaque type de série.

Vous pouvez également créer un groupe de séries de graphiques pour attribuer des axes secondaires à une ou plusieurs séries de graphiques.

Pour en savoir plus, visitez le[ Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
