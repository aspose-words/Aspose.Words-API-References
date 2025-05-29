---
title: AxisGroup Enum
linktitle: AxisGroup
articleTitle: AxisGroup
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.Charts.AxisGroup, votre clé pour gérer efficacement les groupes d'axes de graphiques pour une visualisation améliorée des données.
type: docs
weight: 800
url: /fr/net/aspose.words.drawing.charts/axisgroup/
---
## AxisGroup enumeration

Représente un type de groupe d'axes de graphique.

```csharp
public enum AxisGroup
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Primary | `0` | Spécifie le groupe d'axes principal. |
| Secondary | `1` | Spécifie le groupe d'axes secondaires. |

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
