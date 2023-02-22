---
title: ChartAxis.AxisBetweenCategories
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartAxis propriété. Obtient ou définit un indicateur indiquant si laxe des valeurs croise laxe des catégories entre les catégories.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartaxis/axisbetweencategories/
---
## ChartAxis.AxisBetweenCategories property

Obtient ou définit un indicateur indiquant si l'axe des valeurs croise l'axe des catégories entre les catégories.

```csharp
public bool AxisBetweenCategories { get; set; }
```

### Remarques

La propriété n'a d'effet que pour les axes de valeurs. Il n'est pas pris en charge par les nouveaux graphiques MS Office 2016.

### Exemples

Montre comment faire croiser un axe de graphique à un emplacement personnalisé.

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
// ce qui signifie que les colonnes pour toutes les valeurs inférieures à zéro pointent vers le bas pour représenter les valeurs négatives.
// Nous pouvons définir une valeur différente pour le croisement de l'axe Y. Dans ce cas, nous le mettrons à 3.
ChartAxis axis = chart.AxisX;
axis.Crosses = AxisCrosses.Custom;
axis.CrossesAt = 3;
axis.AxisBetweenCategories = true;

doc.Save(ArtifactsDir + "Charts.AxisCross.docx");
```

### Voir également

* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartaxis/)
* Assemblée [Aspose.Words](../../../)


