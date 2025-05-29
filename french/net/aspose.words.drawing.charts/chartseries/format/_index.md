---
title: ChartSeries.Format
linktitle: Format
articleTitle: Format
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Format ChartSeries pour un accès sans effort aux styles de remplissage et de ligne personnalisables, améliorant ainsi votre expérience de visualisation des données.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing.charts/chartseries/format/
---
## ChartSeries.Format property

Donne accès au remplissage et au formatage des lignes de la série.

```csharp
public ChartFormat Format { get; }
```

## Exemples

Semez comment définir la couleur de la série.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Supprimer la série générée par défaut.
seriesColl.Clear();

// Créer un tableau de noms de catégories.
string[] categories = new[] { "Category 1", "Category 2" };

// Ajout d'une nouvelle série. Les tableaux de valeurs et de catégories doivent avoir la même taille.
ChartSeries series1 = seriesColl.Add("Series 1", categories, new double[] { 1, 2 });
ChartSeries series2 = seriesColl.Add("Series 2", categories, new double[] { 3, 4 });
ChartSeries series3 = seriesColl.Add("Series 3", categories, new double[] { 5, 6 });

// Définir la couleur de la série.
series1.Format.Fill.ForeColor = Color.Red;
series2.Format.Fill.ForeColor = Color.Yellow;
series3.Format.Fill.ForeColor = Color.Blue;

doc.Save(ArtifactsDir + "Charts.SeriesColor.docx");
```

### Voir également

* class [ChartFormat](../../chartformat/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
