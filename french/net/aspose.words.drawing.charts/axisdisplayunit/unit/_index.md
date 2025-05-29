---
title: AxisDisplayUnit.Unit
linktitle: Unit
articleTitle: Unit
second_title: Aspose.Words pour .NET
description: Découvrez la propriété AxisDisplayUnit pour personnaliser facilement la mise à l'échelle de l'unité d'affichage avec des valeurs prédéfinies pour une visualisation améliorée des données.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/axisdisplayunit/unit/
---
## AxisDisplayUnit.Unit property

Obtient ou définit la valeur de mise à l'échelle des unités d'affichage comme l'une des valeurs prédéfinies.

```csharp
public AxisBuiltInUnit Unit { get; set; }
```

## Remarques

La valeur par défaut estNone . LeCustom et Percentage les valeurs ne sont pas disponibles dans certains types de graphiques ; see [`AxisBuiltInUnit`](../../axisbuiltinunit/) pour plus d'informations.

## Exemples

Montre comment manipuler les graduations et les valeurs affichées d'un axe de graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 450, 250);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);

// Définissez les graduations mineures de l'axe Y pour qu'elles pointent loin de la zone de tracé,
// et les graduations principales pour traverser l'axe.
ChartAxis axis = chart.AxisY;
axis.MajorTickMark = AxisTickMark.Cross;
axis.MinorTickMark = AxisTickMark.Outside;

// Définissez l'axe Y pour afficher une graduation majeure toutes les 10 unités et une graduation mineure toutes les 1 unité.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Définissez les limites de l'axe Y sur -10 et 20.
// Cet axe Y affichera désormais 4 graduations principales et 27 graduations mineures.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Pour l'axe des X, définissez les graduations principales toutes les 10 unités,
// chaque graduation mineure à 2,5 unités.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configurez les deux types de graduations pour qu'elles apparaissent à l'intérieur de la zone de tracé du graphique.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Définissez les limites de l'axe X de sorte que l'axe X s'étende sur 5 graduations principales et 12 graduations mineures.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabels.Alignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabels.Spacing);
Assert.AreEqual(doc, axis.DisplayUnit.Document);

// Définissez les étiquettes de graduation pour afficher leur valeur en millions.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Nous pouvons définir une valeur plus spécifique par laquelle les étiquettes de graduation afficheront leurs valeurs.
// Cette déclaration est équivalente à celle ci-dessus.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Voir également

* enum [AxisBuiltInUnit](../../axisbuiltinunit/)
* class [AxisDisplayUnit](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
