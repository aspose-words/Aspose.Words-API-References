---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.ChartXValue, votre solution pour définir les valeurs X dans les séries de graphiques, améliorant ainsi la visualisation des données sans effort.
type: docs
weight: 1160
url: /fr/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

Représente une valeur X pour une série de graphiques.

```csharp
public class ChartXValue
```

## Propriétés

| Nom | La description |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | Obtient la valeur datetime stockée. |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | Obtient la valeur numérique stockée. |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | Obtient la valeur multiniveau stockée. |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | Obtient la valeur de la chaîne stockée. |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | Obtient la valeur de temps stockée. |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | Obtient le type de la valeur X stockée dans l'objet. |

## Méthodes

| Nom | La description |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | Crée un`ChartXValue` exemple de laDateTime type. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | Crée un`ChartXValue` exemple de laDouble type. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | Crée un`ChartXValue` exemple de laMultilevel type. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | Crée un`ChartXValue` exemple de laString type. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | Crée un`ChartXValue` exemple de laTime type. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | Obtient un indicateur indiquant si l'objet spécifié est égal à l'objet de valeur X actuel. |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | Obtient un code de hachage pour l'objet de valeur X actuel. |

## Remarques

Cette classe contient un certain nombre de méthodes statiques permettant de créer une valeur X d'un type particulier. The [`ValueType`](./valuetype/) la propriété vous permet de déterminer le type d'une valeur X existante.

Toutes les valeurs X non nulles d'une série de graphiques doivent être identiques[`ChartXValueType`](../chartxvaluetype/) taper.

## Exemples

Montre comment remplir des séries de graphiques avec des données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// Effacer les valeurs X et Y de la première série.
series1.ClearValues();

// Remplir la série avec des données.
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// Effacer les valeurs X et Y de la deuxième série.
series2.Clear();

// Remplir la série avec des données.
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
