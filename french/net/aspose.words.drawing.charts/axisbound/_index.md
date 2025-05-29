---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.Charts.AxisBound, votre solution pour définir les limites de valeurs des axes dans les graphiques pour une visualisation précise des données.
type: docs
weight: 750
url: /fr/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Représente la limite minimale ou maximale des valeurs de l'axe.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public sealed class AxisBound
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Crée une nouvelle instance indiquant que la limite de l'axe doit être déterminée automatiquement par une application de traitement de texte. |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | Crée une limite d'axe représentée sous forme de valeur datetime. |
| [AxisBound](axisbound/#constructor_1)(*double*) | Crée une limite d'axe représentée sous la forme d'un nombre. |

## Propriétés

| Nom | La description |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Renvoie un indicateur indiquant que la limite de l'axe doit être déterminée automatiquement. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Renvoie la valeur numérique de la limite de l'axe. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Renvoie la valeur de la limite de l'axe représentée sous forme de datetime. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Sert de fonction de hachage pour ce type. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |

## Remarques

La limite peut être spécifiée sous forme de valeur numérique, de date/heure ou de valeur « auto » spéciale.

Les instances de cette classe sont immuables.

## Exemples

Montre comment insérer un graphique avec des valeurs de date/heure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Effacez la série de données de démonstration du graphique pour démarrer avec un graphique propre.
chart.Series.Clear();

// Ajoutez une série personnalisée contenant des valeurs de date/heure pour l'axe X et des valeurs décimales respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Définissez les limites inférieures et supérieures de l'axe X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Définissez les unités principales de l'axe X sur une semaine et les unités mineures sur un jour.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Définir les propriétés de l'axe Y pour les valeurs décimales.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabels.Position = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
