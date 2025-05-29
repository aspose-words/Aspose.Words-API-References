---
title: ChartSeriesGroupCollection Class
linktitle: ChartSeriesGroupCollection
articleTitle: ChartSeriesGroupCollection
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.ChartSeriesGroupCollection, votre solution de référence pour gérer et organiser les objets ChartSeriesGroup sans effort.
type: docs
weight: 1100
url: /fr/net/aspose.words.drawing.charts/chartseriesgroupcollection/
---
## ChartSeriesGroupCollection class

Représente une collection de[`ChartSeriesGroup`](../chartseriesgroup/) objets.

```csharp
public class ChartSeriesGroupCollection : IEnumerable<ChartSeriesGroup>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriesgroupcollection/count/) { get; } | Renvoie le nombre de groupes de séries dans cette collection. |
| [Item](../../aspose.words.drawing.charts/chartseriesgroupcollection/item/) { get; } | Renvoie un[`ChartSeriesGroup`](../chartseriesgroup/) à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriesgroupcollection/add/)(*[ChartSeriesType](../chartseriestype/)*) | Ajoute un nouveau groupe de séries du type de série spécifié à cette collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriesgroupcollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriesgroupcollection/removeat/)(*int*) | Supprime un groupe de séries à l'index spécifié. Toutes les séries enfants seront supprimées du graphique. |

## Remarques

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) Article de documentation .

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

* class [ChartSeriesGroup](../chartseriesgroup/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
