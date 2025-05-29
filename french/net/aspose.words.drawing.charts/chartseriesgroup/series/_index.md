---
title: ChartSeriesGroup.Series
linktitle: Series
articleTitle: Series
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeriesGroup Series pour accéder à une collection unique de séries associées, améliorant ainsi votre expérience de visualisation de données.
type: docs
weight: 100
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/series/
---
## ChartSeriesGroup.Series property

Obtient une collection de séries appartenant à ce groupe de séries.

```csharp
public ChartSeriesCollection Series { get; }
```

## Exemples

Montre comment travailler avec l’axe secondaire du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// Supprimer la série générée par défaut.
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// Créer un groupe de séries supplémentaire, également de type ligne.
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// Spécifiez l'utilisation des axes secondaires pour le nouveau groupe de séries.
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// Masquer l'axe X secondaire.
newSeriesGroup.AxisX.Hidden = true;
// Définir le titre de l'axe Y secondaire.
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// Ajouter une série au nouveau groupe de séries.
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### Voir également

* class [ChartSeriesCollection](../../chartseriescollection/)
* class [ChartSeriesGroup](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
