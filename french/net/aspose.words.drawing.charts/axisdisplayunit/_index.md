---
title: AxisDisplayUnit Class
linktitle: AxisDisplayUnit
articleTitle: AxisDisplayUnit
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.AxisDisplayUnit classe. Donne accès aux options de mise à léchelle des unités daffichage pour laxe des valeurs en C#.
type: docs
weight: 550
url: /fr/net/aspose.words.drawing.charts/axisdisplayunit/
---
## AxisDisplayUnit class

Donne accès aux options de mise à l'échelle des unités d'affichage pour l'axe des valeurs.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class AxisDisplayUnit
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [AxisDisplayUnit](axisdisplayunit/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [CustomUnit](../../aspose.words.drawing.charts/axisdisplayunit/customunit/) { get; set; } | Obtient ou définit un diviseur défini par l'utilisateur pour mettre à l'échelle les unités d'affichage sur l'axe des valeurs. |
| [Document](../../aspose.words.drawing.charts/axisdisplayunit/document/) { get; } | Renvoie le document auquel appartient le titulaire du titre. |
| [Unit](../../aspose.words.drawing.charts/axisdisplayunit/unit/) { get; set; } | Obtient ou définit la valeur de mise à l'échelle des unités d'affichage comme l'une des valeurs prédéfinies. |

## Exemples

Montre comment manipuler les graduations et les valeurs affichées d’un axe de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Définit les graduations mineures de l'axe Y pour qu'elles pointent à l'opposé de la zone de tracé,
// et les graduations principales pour traverser l'axe.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Définissez l'axe Y pour afficher un tick majeur toutes les 10 unités et un tick mineur toutes les 1 unité.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Définit les limites de l'axe Y sur -10 et 20.
// Cet axe Y affichera désormais 4 graduations majeures et 27 graduations mineures.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Pour l'axe X, définissez les graduations principales toutes les 10 unités,
// chaque graduation mineure à 2,5 unités.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configure les deux types de graduations pour qu'elles apparaissent à l'intérieur de la zone de tracé du graphique.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Définissez les limites de l'axe X de sorte que l'axe X s'étende sur 5 graduations principales et 12 graduations mineures.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Définit les étiquettes de graduation pour afficher leur valeur en millions.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Nous pouvons définir une valeur plus spécifique par laquelle les étiquettes de ticks afficheront leurs valeurs.
// Cette instruction est équivalente à celle ci-dessus.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
