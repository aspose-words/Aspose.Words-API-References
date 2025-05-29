---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.ChartDataLabelPosition pour personnaliser facilement les étiquettes de données de votre graphique pour une clarté et une présentation améliorées.
type: docs
weight: 960
url: /fr/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

Spécifie la position d'une étiquette de données de graphique.

```csharp
public enum ChartDataLabelPosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Center | `0` | Spécifie qu'une étiquette de données doit être affichée centrée sur un marqueur de données. |
| Left | `1` | Spécifie qu'une étiquette de données doit être affichée à gauche d'un marqueur de données. |
| Right | `2` | Spécifie qu'une étiquette de données doit être affichée à droite d'un marqueur de données. |
| Above | `3` | Spécifie qu'une étiquette de données doit être affichée au-dessus d'un marqueur de données. |
| Below | `4` | Spécifie qu'une étiquette de données doit être affichée sous un marqueur de données. |
| InsideBase | `5` | Spécifie qu'une étiquette de données doit être affichée à l'intérieur de la base d'un marqueur de données. |
| InsideEnd | `6` | Spécifie qu'une étiquette de données doit être affichée à l'intérieur de la fin d'un marqueur de données. |
| OutsideEnd | `7` | Spécifie qu'une étiquette de données doit être affichée à l'extérieur de la fin d'un marqueur de données. |
| BestFit | `8` | Spécifie qu'une étiquette de données doit être affichée dans la position la plus appropriée. |

## Remarques

Tous les types de séries ne permettent pas de spécifier la position des étiquettes. Et celles qui le permettent ne prennent pas en charge toutes les valeurs.

## Exemples

Montre comment définir la position de l'étiquette de données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique à colonnes.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Supprimer la série générée par défaut.
seriesColl.Clear();

// Ajouter une série.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Afficher les étiquettes de données et définir la couleur de la police.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Définir la position de l'étiquette de données.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
