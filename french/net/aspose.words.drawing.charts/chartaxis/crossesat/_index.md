---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartAxis CrossesAt pour définir facilement des points d'intersection sur l'axe perpendiculaire de votre graphique pour une visualisation améliorée des données.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Spécifie où sur l'axe perpendiculaire l'axe croise.

```csharp
public double CrossesAt { get; set; }
```

## Remarques

La propriété n'a d'effet que si[`Crosses`](../crosses/) sont réglés surCustom. Il n'est pas pris en charge par les nouveaux graphiques MS Office 2016.

Les unités sont déterminées par le type d'axe. Lorsqu'il s'agit d'un axe de valeurs, la valeur de la propriété est un nombre décimal sur l'axe des valeurs. Lorsqu'il s'agit d'un axe de catégories temporelles, la valeur est définie comme un nombre entier de jours par rapport à la date de base (30/12/1899). Pour un axe de catégories textuelles, la valeur est un numéro de catégorie entier, commençant par 1 comme première catégorie.

## Exemples

Montre comment faire en sorte qu'un axe de graphique se croise à un emplacement personnalisé.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Pour les graphiques à colonnes, l'axe Y se croise à zéro par défaut,
// ce qui signifie que les colonnes pour toutes les valeurs inférieures à zéro pointent vers le bas pour représenter les valeurs négatives.
// Nous pouvons définir une valeur différente pour le croisement de l'axe Y. Dans ce cas, nous la définirons à 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Voir également

* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
