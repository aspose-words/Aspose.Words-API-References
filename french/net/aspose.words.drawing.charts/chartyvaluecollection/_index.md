---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartYValueCollection, votre solution de référence pour gérer les valeurs Y dans les séries de graphiques de manière efficace et efficiente.
type: docs
weight: 1200
url: /fr/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

Représente une collection de valeurs Y pour une série de graphiques.

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | Obtient le nombre d'éléments dans cette collection. |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | Obtient ou définit le code de format appliqué aux valeurs Y. |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | Obtient ou définit la valeur Y à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | Renvoie un objet énumérateur. |

## Remarques

Tous les éléments de la collection autres que**nul** doit avoir le même[`ValueType`](../chartyvalue/valuetype/).

La collection permet uniquement de modifier les valeurs Y. Pour ajouter ou insérer de nouvelles valeurs à une série de graphiques, ou supprimer des valeurs, utilisez les méthodes appropriées du[`ChartSeries`](../chartseries/) la classe peut être utilisée.

## Exemples

Montre comment obtenir des données de séries de graphiques.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // Effacer le format individuel de tous les points de données.
    // Les points de données et les valeurs de données sont un à un dans les graphiques à colonnes.
    series.DataPoints[i].ClearFormat();

    // Obtenir la valeur Y.
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// Changer les couleurs des valeurs max et min.
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### Voir également

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
