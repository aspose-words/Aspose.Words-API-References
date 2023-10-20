---
title: AxisTickMark Enum
linktitle: AxisTickMark
articleTitle: AxisTickMark
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.AxisTickMark énumération. Spécifie les positions possibles pour les graduations en C#.
type: docs
weight: 590
url: /fr/net/aspose.words.drawing.charts/axistickmark/
---
## AxisTickMark enumeration

Spécifie les positions possibles pour les graduations.

```csharp
public enum AxisTickMark
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Cross | `0` | Spécifie que les graduations doivent traverser l'axe. |
| Inside | `1` | Spécifie que les graduations doivent se trouver à l'intérieur de la zone de tracé. |
| Outside | `2` | Spécifie que les graduations doivent être en dehors de la zone de tracé. |
| None | `3` | Spécifie qu'il ne doit y avoir aucune graduation. |

## Exemples

Montre comment insérer un graphique avec des valeurs de date/heure.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Ajoutez une série personnalisée contenant des valeurs de date/heure pour l'axe X et des valeurs décimales respectives pour l'axe Y.
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// Définit les limites inférieure et supérieure de l'axe X.
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// Définit les unités principales de l'axe X sur une semaine et les unités mineures sur un jour.
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// Définir les propriétés de l'axe Y pour les valeurs décimales.
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
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
