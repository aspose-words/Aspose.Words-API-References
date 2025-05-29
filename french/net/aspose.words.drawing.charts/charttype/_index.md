---
title: ChartType Enum
linktitle: ChartType
articleTitle: ChartType
second_title: Aspose.Words pour .NET
description: Explorez l'énumération Aspose.Words.Drawing.Charts.ChartType pour découvrir différents types de graphiques et améliorer sans effort la visualisation des données de votre document.
type: docs
weight: 1150
url: /fr/net/aspose.words.drawing.charts/charttype/
---
## ChartType enumeration

Spécifie le type d'un graphique.

```csharp
public enum ChartType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Area | `0` | Graphique en aires. |
| AreaStacked | `1` | Graphique en aires empilées. |
| AreaPercentStacked | `2` | Graphique en aires empilées à 100 %. |
| Area3D | `3` | Graphique en aires 3D. |
| Area3DStacked | `4` | Graphique à aires empilées 3D. |
| Area3DPercentStacked | `5` | Graphique à aires empilées 3D à 100 %. |
| Bar | `6` | Graphique à barres. |
| BarStacked | `7` | Graphique à barres empilées. |
| BarPercentStacked | `8` | Graphique à barres empilées à 100 %. |
| Bar3D | `9` | Graphique à barres 3D. |
| Bar3DStacked | `10` | Graphique à barres empilées 3D. |
| Bar3DPercentStacked | `11` | Graphique à barres empilées 3D à 100 %. |
| Bubble | `12` | Graphique à bulles. |
| Bubble3D | `13` | Graphique à bulles 3D. |
| Column | `14` | Graphique à colonnes. |
| ColumnStacked | `15` | Graphique à colonnes empilées. |
| ColumnPercentStacked | `16` | Graphique à colonnes empilées à 100 %. |
| Column3D | `17` | Graphique à colonnes 3D. |
| Column3DStacked | `18` | Graphique à colonnes empilées 3D. |
| Column3DPercentStacked | `19` | Graphique à colonnes empilées 3D à 100 %. |
| Column3DClustered | `20` | Graphique à colonnes groupées 3D. |
| Doughnut | `21` | Graphique en anneau. |
| Line | `22` | Graphique linéaire. |
| LineStacked | `23` | Graphique à lignes empilées. |
| LinePercentStacked | `24` | Graphique à lignes empilées à 100 %. |
| Line3D | `25` | Graphique linéaire 3D. |
| Pie | `26` | Graphique à secteurs. |
| Pie3D | `27` | Graphique à secteurs 3D. |
| PieOfBar | `28` | Graphique à secteurs ou à barres. |
| PieOfPie | `29` | Graphique à secteurs. |
| Radar | `30` | Carte radar. |
| Scatter | `31` | Graphique en nuage de points. |
| Stock | `32` | Graphique boursier. |
| Surface | `33` | Carte de surface. |
| Surface3D | `34` | Carte de surface 3D. |
| Treemap | `35` | Graphique arborescent. |
| Sunburst | `36` | Carte Sunburst. |
| Histogram | `37` | Graphique à histogramme. |
| Pareto | `38` | Diagramme de Pareto. |
| BoxAndWhisker | `39` | Diagramme en boîte et à moustaches. |
| Waterfall | `40` | Graphique en cascade. |
| Funnel | `41` | Graphique en entonnoir. |

## Exemples

Montre comment créer un type approprié de série de graphiques pour un type de graphique.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Il existe plusieurs façons de remplir la collection de séries d'un graphique.
    // Différents schémas de séries sont destinés à différents types de graphiques.
    // 1 - Graphique à colonnes avec colonnes regroupées et cerclées le long de l'axe des X par catégorie :
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insérer deux séries de valeurs décimales contenant une valeur pour chaque catégorie respective.
    // Ce graphique à colonnes comportera trois groupes, chacun avec deux colonnes.
    chart.Series.Add("Series 1", categories, new[] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new[] { 64.2, 79.5, 94.0 });

    // Les catégories sont distribuées le long de l'axe X et les valeurs sont distribuées le long de l'axe Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Graphique en aires avec dates réparties le long de l'axe des X :
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insérer une série avec une valeur décimale pour chaque date respective.
    // Les dates seront distribuées le long d'un axe X linéaire,
    // et les valeurs ajoutées à cette série créeront des points de données.
    chart.Series.Add("Series 1", dates, new[] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Nuage de points 2D :
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Chaque série aura besoin de deux tableaux décimaux de longueur égale.
    // Le premier tableau contient les valeurs X et le second contient les valeurs Y correspondantes
    // des points de données sur le graphique du graphique.
    chart.Series.Add("Series 1",
        new[] { 3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6 },
        new[] { 3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9 });
    chart.Series.Add("Series 2",
        new[] { 2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3 },
        new[] { 7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6 });

    Assert.AreEqual(ChartAxisType.Value, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 4 - Graphique à bulles :
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Chaque série aura besoin de trois tableaux décimaux de longueur égale.
    // Le premier tableau contient les valeurs X, le second contient les valeurs Y correspondantes,
    // et le troisième contient les diamètres de chacun des points de données du graphique.
    chart.Series.Add("Series 1",
        new[] { 1.1, 5.0, 9.8 },
        new[] { 1.2, 4.9, 9.9 },
        new[] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insérez un graphique à l'aide d'un générateur de documents d'un ChartType, d'une largeur et d'une hauteur spécifiés, et supprimez ses données de démonstration.
/// </summary>
private static Chart AppendChart(DocumentBuilder builder, ChartType chartType, double width, double height)
{
    Shape chartShape = builder.InsertChart(chartType, width, height);
    Chart chart = chartShape.Chart;
    chart.Series.Clear();
    return chart;
}
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
