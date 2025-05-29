---
title: ChartSeriesCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words pour .NET
description: Accédez à la propriété d'élément ChartSeriesCollection pour récupérer sans effort un ChartSeries par index, améliorant ainsi votre expérience de visualisation des données.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/chartseriescollection/item/
---
## ChartSeriesCollection indexer

Renvoie un[`ChartSeries`](../../chartseries/) à l'index spécifié.

```csharp
public ChartSeries this[int index] { get; }
```

| Paramètre | La description |
| --- | --- |
| index | Un index de la collection. |

## Remarques

L'indice est basé sur zéro.

Les index négatifs sont autorisés et indiquent l'accès depuis l'arrière de la collection. Par exemple, -1 signifie le dernier élément, -2 signifie l'avant-dernier et ainsi de suite.

Si l'index est supérieur ou égal au nombre d'éléments dans la liste, cela renvoie une référence nulle.

Si l'index est négatif et que sa valeur absolue est supérieure au nombre d'éléments dans la liste, cela renvoie une référence nulle.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
