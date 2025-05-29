---
title: ChartAxis.HasMajorGridlines
linktitle: HasMajorGridlines
articleTitle: HasMajorGridlines
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartAxis HasMajorGridlines pour gérer facilement les principales lignes de grille de vos graphiques, améliorant ainsi la visualisation et la clarté des données.
type: docs
weight: 90
url: /fr/net/aspose.words.drawing.charts/chartaxis/hasmajorgridlines/
---
## ChartAxis.HasMajorGridlines property

Obtient ou définit un indicateur indiquant si l'axe possède des lignes de grille principales.

```csharp
public bool HasMajorGridlines { get; set; }
```

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

* class [ChartAxis](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
