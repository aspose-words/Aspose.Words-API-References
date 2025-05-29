---
title: ChartSeriesCollection Class
linktitle: ChartSeriesCollection
articleTitle: ChartSeriesCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartSeriesCollection, votre solution pour gérer et personnaliser les séries de graphiques sans effort.
type: docs
weight: 1080
url: /fr/net/aspose.words.drawing.charts/chartseriescollection/
---
## ChartSeriesCollection class

Représente une collection d'un[`ChartSeries`](../chartseries/) .

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartSeriesCollection : IEnumerable<ChartSeries>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartseriescollection/count/) { get; } | Renvoie le nombre de[`ChartSeries`](../chartseries/) dans cette collection. |
| [Item](../../aspose.words.drawing.charts/chartseriescollection/item/) { get; } | Renvoie un[`ChartSeries`](../chartseries/) à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_1)(*string, double[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries aux graphiques à histogramme. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add)(*string, ChartMultilevelValue[], double[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/)à cette collection. Utilisez cette méthode pour ajouter des séries qui ont des catégories de données à plusieurs niveaux. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_4)(*string, DateTime[], double[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques de zone, radar et boursiers. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_2)(*string, double[], double[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques en nuage de points. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_5)(*string, string[], double[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques à barres, à colonnes, à courbes et à surface. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_3)(*string, double[], double[], double[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques à bulles. |
| [Add](../../aspose.words.drawing.charts/chartseriescollection/add/#add_6)(*string, string[], double[], bool[]*) | Ajoute un nouveau[`ChartSeries`](../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries aux graphiques en cascade. |
| [Clear](../../aspose.words.drawing.charts/chartseriescollection/clear/)() | Supprime tout[`ChartSeries`](../chartseries/) de cette collection. |
| [GetEnumerator](../../aspose.words.drawing.charts/chartseriescollection/getenumerator/)() | Renvoie un objet énumérateur. |
| [RemoveAt](../../aspose.words.drawing.charts/chartseriescollection/removeat/)(*int*) | Supprime un[`ChartSeries`](../chartseries/) à l'index spécifié. |

## Exemples

Montre comment ajouter et supprimer des données de série dans un graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez un graphique à colonnes qui contiendra trois séries de données de démonstration par défaut.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Chaque série comporte quatre valeurs décimales : une pour chacune des quatre catégories.
// Quatre groupes de trois colonnes représenteront ces données.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Imprimez le nom de chaque série dans le graphique.
using (IEnumerator<ChartSeries> enumerator = chart.Series.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine(enumerator.Current.Name);
    }
}

// Ce sont les noms des catégories dans le graphique.
string[] categories = { "Category 1", "Category 2", "Category 3", "Category 4" };

// Nous pouvons ajouter une série avec de nouvelles valeurs pour les catégories existantes.
// Ce graphique contiendra désormais quatre groupes de quatre colonnes.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });
// Une série de graphiques peut également être supprimée par index, comme ceci.
// Cela supprimera l'une des trois séries de démonstration fournies avec le graphique.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));
// Nous pouvons également effacer toutes les données du graphique en une seule fois avec cette méthode.
// Lors de la création d'un nouveau graphique, voici comment effacer toutes les données de démonstration
// avant de pouvoir commencer à travailler sur un graphique vierge.
chartData.Clear();
```

### Voir également

* class [ChartSeries](../chartseries/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
