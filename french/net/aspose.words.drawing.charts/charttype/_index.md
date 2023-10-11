---
title: Enum ChartType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartType énumération. Spécifie le type dun graphique.
type: docs
weight: 830
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
| AreaStacked | `1` | Graphique à aires empilées. |
| AreaPercentStacked | `2` | Graphique à zones empilées à 100 %. |
| Area3D | `3` | Carte de zone 3D. |
| Area3DStacked | `4` | Graphique à zones empilées 3D. |
| Area3DPercentStacked | `5` | Graphique 3D à zones empilées à 100 %. |
| Bar | `6` | Graphique à barres. |
| BarStacked | `7` | Graphique à barres empilées. |
| BarPercentStacked | `8` | Graphique à barres empilées à 100 %. |
| Bar3D | `9` | Graphique à barres 3D. |
| Bar3DStacked | `10` | Graphique à barres empilées 3D. |
| Bar3DPercentStacked | `11` | Graphique à barres empilées 100 % 3D. |
| Bubble | `12` | Graphique à bulles. |
| Bubble3D | `13` | Graphique à bulles 3D. |
| Column | `14` | Diagramme à colonnes. |
| ColumnStacked | `15` | Diagramme à colonnes empilées. |
| ColumnPercentStacked | `16` | Graphique à colonnes empilées à 100 %. |
| Column3D | `17` | Graphique à colonnes 3D. |
| Column3DStacked | `18` | Graphique à colonnes empilées 3D. |
| Column3DPercentStacked | `19` | Graphique à colonnes empilées 100 % 3D. |
| Column3DClustered | `20` | Diagramme à colonnes groupées 3D. |
| Doughnut | `21` | Graphique en beignet. |
| Line | `22` | Graphique linéaire. |
| LineStacked | `23` | Graphique en courbes empilées. |
| LinePercentStacked | `24` | Graphique en courbes empilées à 100 %. |
| Line3D | `25` | Graphique linéaire 3D. |
| Pie | `26` | Diagramme circulaire. |
| Pie3D | `27` | Diagramme circulaire 3D. |
| PieOfBar | `28` | Graphique à secteurs ou à barres. |
| PieOfPie | `29` | Graphique à secteurs. |
| Radar | `30` | Carte radar. |
| Scatter | `31` | Nuage de points. |
| Stock | `32` | Graphique boursier. |
| Surface | `33` | Graphique de surface. |
| Surface3D | `34` | Graphique de surface 3D. |

### Exemples

Montre comment créer un type approprié de série de graphiques pour un type de graphique.

```csharp
public void ChartSeriesCollection()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Il existe plusieurs façons de remplir la collection de séries d'un graphique.
    // Différents schémas de séries sont destinés à différents types de graphiques.
    // 1 - Diagramme à colonnes avec des colonnes regroupées et regroupées le long de l'axe X par catégorie :
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insère deux séries de valeurs décimales contenant une valeur pour chaque catégorie respective.
    // Cet histogramme aura trois groupes, chacun avec deux colonnes.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Les catégories sont distribuées le long de l'axe X et les valeurs sont distribuées le long de l'axe Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Graphique en aires avec dates réparties le long de l'axe X :
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insère une série avec une valeur décimale pour chaque date respective.
    // Les dates seront réparties le long d'un axe X linéaire,
    // et les valeurs ajoutées à cette série créeront des points de données.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Nuage de points 2D :
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

    // 4 - Graphique à bulles :
    chart = AppendChart(builder, ChartType.Bubble, 500, 300);

    // Chaque série aura besoin de trois tableaux décimaux de longueur égale.
    // Le premier tableau contient les valeurs X, le second contient les valeurs Y correspondantes,
    // et le troisième contient les diamètres de chacun des points de données du graphique.
    chart.Series.Add("Series 1", 
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insère un graphique à l'aide d'un générateur de documents d'un ChartType, d'une largeur et d'une hauteur spécifiés, et supprime ses données de démonstration.
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


