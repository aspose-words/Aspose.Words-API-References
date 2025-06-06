---
title: ChartXValueCollection Class
linktitle: ChartXValueCollection
articleTitle: ChartXValueCollection
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartXValueCollection, votre solution pour gérer efficacement les collections de valeurs X dans les séries de graphiques.
type: docs
weight: 1170
url: /fr/net/aspose.words.drawing.charts/chartxvaluecollection/
---
## ChartXValueCollection class

Représente une collection de valeurs X pour une série de graphiques.

```csharp
public class ChartXValueCollection : IEnumerable<ChartXValue>
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartxvaluecollection/count/) { get; } | Obtient le nombre d'éléments dans cette collection. |
| [FormatCode](../../aspose.words.drawing.charts/chartxvaluecollection/formatcode/) { get; set; } | Obtient ou définit le code de format appliqué aux valeurs X. |
| [Item](../../aspose.words.drawing.charts/chartxvaluecollection/item/) { get; set; } | Obtient ou définit la valeur X à l'index spécifié. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartxvaluecollection/getenumerator/)() | Renvoie un objet énumérateur. |

## Remarques

Tous les éléments de la collection autres que**nul** doit avoir le même[`ValueType`](../chartxvalue/valuetype/).

La collection permet uniquement de modifier les valeurs X. Pour ajouter ou insérer de nouvelles valeurs à une série de graphiques, ou pour supprimer des valeurs, utilisez les méthodes appropriées du[`ChartSeries`](../chartseries/) la classe peut être utilisée.

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
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartXValue](../chartxvalue/)
* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
