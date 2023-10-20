---
title: ChartAxis.CrossesAt
linktitle: CrossesAt
articleTitle: CrossesAt
second_title: Aspose.Words pour .NET
description: ChartAxis CrossesAt propriété. Spécifie lendroit où laxe se croise sur laxe perpendiculaire en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartaxis/crossesat/
---
## ChartAxis.CrossesAt property

Spécifie l'endroit où l'axe se croise sur l'axe perpendiculaire.

```csharp
public double CrossesAt { get; set; }
```

## Remarques

La propriété n'a d'effet que si[`Crosses`](../crosses/) sont réglés surCustom. Il n'est pas pris en charge par les nouveaux graphiques MS Office 2016.

Les unités sont déterminées par le type d'axe. Lorsque l’axe est un axe des valeurs, la valeur de la propriété est un nombre décimal sur l’axe des valeurs. Lorsque l'axe est un axe de catégories de temps, la valeur est définie comme un nombre entier de jours par rapport à la date de base (30/12/1899). Pour un axe de catégorie de texte, la valeur est un numéro de catégorie entier, commençant par 1 comme première catégorie.

## Exemples

Montre comment faire croiser un axe graphique à un emplacement personnalisé.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Pour les histogrammes, l'axe Y passe à zéro par défaut,
// ce qui signifie que les colonnes de toutes les valeurs inférieures à zéro pointent vers le bas pour représenter des valeurs négatives.
// Nous pouvons définir une valeur différente pour le croisement de l'axe Y. Dans ce cas, nous le fixerons à 3.
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
