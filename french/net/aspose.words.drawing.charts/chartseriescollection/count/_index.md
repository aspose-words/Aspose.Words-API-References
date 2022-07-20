---
title: Count
second_title: Référence de l'API Aspose.Words pour .NET
description: Renvoie le nombre deChartSeriesaspose.words.drawing.charts/chartseries dans cette collection.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartseriescollection/count/
---
## ChartSeriesCollection.Count property

Renvoie le nombre de[`ChartSeries`](../../chartseries) dans cette collection.

```csharp
public int Count { get; }
```

### Exemples

Montre comment ajouter et supprimer des données de série dans un graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère un histogramme qui contiendra trois séries de données de démonstration par défaut.
Shape chartShape = builder.InsertChart(ChartType.Column, 400, 300);
Chart chart = chartShape.Chart;

// Chaque série a quatre valeurs décimales : une pour chacune des quatre catégories.
// Quatre clusters de trois colonnes représenteront ces données.
ChartSeriesCollection chartData = chart.Series;

Assert.AreEqual(3, chartData.Count);

// Affiche le nom de chaque série dans le graphique.
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
// Ce graphique contiendra désormais quatre clusters de quatre colonnes.
chart.Series.Add("Series 4", categories, new[] { 4.4, 7.0, 3.5, 2.1 });

// Une série de graphiques peut également être supprimée par index, comme ceci.
// Cela supprimera l'une des trois séries de démonstration fournies avec le graphique.
chartData.RemoveAt(2);

Assert.False(chartData.Any(s => s.Name == "Series 3"));

// Nous pouvons également effacer toutes les données du graphique à la fois avec cette méthode.
// Lors de la création d'un nouveau graphique, c'est le moyen d'effacer toutes les données de démonstration
// avant de pouvoir commencer à travailler sur un graphique vide.
chartData.Clear();
```

### Voir également

* class [ChartSeriesCollection](../../chartseriescollection)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartseriescollection)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->