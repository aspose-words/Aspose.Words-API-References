---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartSeriesType énumération. Spécifie un type de série de graphiques en C#.
type: docs
weight: 800
url: /fr/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

Spécifie un type de série de graphiques.

```csharp
public enum ChartSeriesType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Area | `0` | Représente une série de graphiques en aires. |
| AreaStacked | `1` | Représente une série de graphiques à zones empilées. |
| AreaPercentStacked | `2` | Représente une série de graphiques à zones empilées à 100 %. |
| Area3D | `3` | Représente une série de graphiques en aires 3D. |
| Area3DStacked | `4` | Représente une série de graphiques à zones empilées 3D. |
| Area3DPercentStacked | `5` | Représente une série de graphiques 3D à zones empilées à 100 %. |
| Bar | `6` | Représente une série de graphiques à barres. |
| BarStacked | `7` | Représente une série de graphiques à barres empilées. |
| BarPercentStacked | `8` | Représente une série de graphiques à barres empilées à 100 %. |
| Bar3D | `9` | Représente une série de graphiques à barres 3D. |
| Bar3DStacked | `10` | Représente une série de graphiques à barres empilées 3D. |
| Bar3DPercentStacked | `11` | Représente une série de graphiques à barres empilées à 100 % en 3D. |
| Bubble | `12` | Représente une série de graphiques à bulles. |
| Bubble3D | `13` | Représente une série de graphiques à bulles 3D. |
| Column | `14` | Représente une série de graphiques à colonnes. |
| ColumnStacked | `15` | Représente une série de graphiques à colonnes empilées. |
| ColumnPercentStacked | `16` | Représente une série d'histogrammes empilés à 100 %. |
| Column3D | `17` | Représente une série de graphiques à colonnes 3D. |
| Column3DStacked | `18` | Représente une série de graphiques à colonnes empilées 3D. |
| Column3DPercentStacked | `19` | Représente une série d'histogrammes empilés à 100 % en 3D. |
| Column3DClustered | `20` | Représente une série d'histogrammes groupés 3D. |
| Doughnut | `21` | Représente une série de graphiques en anneau. |
| Line | `22` | Représente une série de graphiques linéaires. |
| LineStacked | `23` | Représente une série de graphiques en courbes empilées. |
| LinePercentStacked | `24` | Représente une série de graphiques en courbes empilées à 100 %. |
| Line3D | `25` | Représente une série de graphiques linéaires 3D. |
| Pie | `26` | Représente une série de diagrammes circulaires. |
| Pie3D | `27` | Représente une série de diagrammes circulaires 3D. |
| PieOfBar | `28` | Représente une série de graphiques à secteurs ou à barres. |
| PieOfPie | `29` | Représente une série de graphiques à secteurs. |
| Radar | `30` | Représente une série de cartes radar. |
| Scatter | `31` | Représente une série de graphiques à nuages de points. |
| Stock | `32` | Représente une série de graphiques boursiers. |
| Surface | `33` | Représente une série de graphiques Surface. |
| Surface3D | `34` | Représente une série de graphiques de surface 3D. |
| Treemap | `35` | Représente une série de graphiques Treemap. |
| Sunburst | `36` | Représente une série de graphiques Sunburst. |
| Histogram | `37` | Représente une série de graphiques histogrammes. |
| Pareto | `38` | Représente une série de graphiques Pareto. |
| ParetoLine | `39` | Représente une série de graphiques Pareto Line. |
| BoxAndWhisker | `40` | Représente une série de graphiques Box et Whisker. |
| Waterfall | `41` | Représente une série de graphiques en cascade. |
| Funnel | `42` | Représente une série de graphiques en entonnoir. |
| RegionMap | `43` | Représente une série de graphiques de cartes de région. |

## Exemples

Montre comment

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// Supprime toutes les séries du type Column.
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
