---
title: AxisDisplayUnit.CustomUnit
second_title: Référence de l'API Aspose.Words pour .NET
description: AxisDisplayUnit propriété. Obtient ou définit un diviseur défini par lutilisateur pour mettre à léchelle les unités daffichage sur laxe des ordonnées.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing.charts/axisdisplayunit/customunit/
---
## AxisDisplayUnit.CustomUnit property

Obtient ou définit un diviseur défini par l'utilisateur pour mettre à l'échelle les unités d'affichage sur l'axe des ordonnées.

```csharp
public double CustomUnit { get; set; }
```

### Remarques

La propriété n'est pas prise en charge par les nouveaux graphiques MS Office 2016. La valeur par défaut est 1.

La définition de cette propriété définit le[`Unit`](../unit/) propriété à Custom.

### Exemples

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

// Définissez l'axe Y pour afficher un tick majeur toutes les 10 unités et un tick mineur toutes les 1 unité.
axis.MajorUnit = 10;
axis.MinorUnit = 1;

// Définissez les limites de l'axe Y sur -10 et 20.
// Cet axe Y affichera désormais 4 graduations majeures et 27 graduations mineures.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(20);

// Pour l'axe X, définissez les graduations principales toutes les 10 unités,
// chaque graduation mineure à 2,5 unités.
axis = chart.AxisX;
axis.MajorUnit = 10;
axis.MinorUnit = 2.5;

// Configurez les deux types de graduations pour qu'elles apparaissent à l'intérieur de la zone de tracé du graphique.
axis.MajorTickMark = AxisTickMark.Inside;
axis.MinorTickMark = AxisTickMark.Inside;

// Définissez les limites de l'axe X de sorte que l'axe X s'étende sur 5 repères majeurs et 12 repères mineurs.
axis.Scaling.Minimum = new AxisBound(-10);
axis.Scaling.Maximum = new AxisBound(30);
axis.TickLabelAlignment = ParagraphAlignment.Right;

Assert.AreEqual(1, axis.TickLabelSpacing);

// Définissez les étiquettes de graduation pour afficher leur valeur en millions.
axis.DisplayUnit.Unit = AxisBuiltInUnit.Millions;

// Nous pouvons définir une valeur plus spécifique par laquelle les étiquettes de coche afficheront leurs valeurs.
// Cette instruction est équivalente à celle ci-dessus.
axis.DisplayUnit.CustomUnit = 1000000;
doc.Save(ArtifactsDir + "Charts.AxisDisplayUnit.docx");
```

### Voir également

* class [AxisDisplayUnit](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../axisdisplayunit/)
* Assemblée [Aspose.Words](../../../)


