---
title: Class AxisBound
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.AxisBound classe. Représente la limite minimale ou maximale des valeurs daxe.
type: docs
weight: 500
url: /fr/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

Représente la limite minimale ou maximale des valeurs d'axe.

```csharp
public sealed class AxisBound
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | Crée une nouvelle instance indiquant que la limite d'axe doit être déterminée automatiquement par une application de traitement de texte. |
| [AxisBound](axisbound/#constructor_2)(DateTime) | Crée une limite d'axe représentée sous forme de valeur datetime. |
| [AxisBound](axisbound/#constructor_1)(double) | Crée une limite d'axe représentée par un nombre. |

## Propriétés

| Nom | La description |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | Renvoie un indicateur indiquant que la limite d'axe doit être déterminée automatiquement. |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | Renvoie la valeur numérique de l'axe lié. |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | Renvoie la valeur de l'axe lié représenté sous la forme datetime. |

## Méthodes

| Nom | La description |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(object) | Détermine si l'objet spécifié est égal en valeur à l'objet actuel. |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | Sert de fonction de hachage pour ce type. |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | Renvoie une chaîne conviviale qui affiche la valeur de cet objet. |

### Remarques

Bound peut être spécifié sous la forme d'un nombre, d'une date/heure ou d'une valeur "auto" spéciale.

Les instances de cette classe sont immuables.

### Exemples

Montre comment insérer un graphique avec des valeurs de date/heure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Ajoutez une série personnalisée contenant des valeurs de date/heure pour l'axe X et des valeurs décimales respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Définit les limites inférieure et supérieure pour l'axe X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Définit les unités principales de l'axe X sur une semaine et les unités secondaires sur un jour.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// Définit les propriétés de l'axe Y pour les valeurs décimales.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


