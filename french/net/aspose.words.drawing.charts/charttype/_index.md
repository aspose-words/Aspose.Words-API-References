---
title: ChartType
second_title: Référence de l'API Aspose.Words pour .NET
description: Spécifie le type dun graphique.
type: docs
weight: 760
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
| AreaPercentStacked | `2` | 100 % de graphique en aires empilées. |
| Area3D | `3` | Graphique en aires 3D. |
| Area3DStacked | `4` | Graphique en aires empilées 3D. |
| Area3DPercentStacked | `5` | Graphique 3D 100 % de zones empilées. |
| Bar | `6` | Diagramme à barres. |
| BarStacked | `7` | Diagramme à barres empilées. |
| BarPercentStacked | `8` | Graphique à barres empilées 100 %. |
| Bar3D | `9` | Diagramme à barres 3D. |
| Bar3DStacked | `10` | Graphique à barres empilées 3D. |
| Bar3DPercentStacked | `11` | Graphique à barres empilées 100 % 3D. |
| Bubble | `12` | Graphique à bulles. |
| Bubble3D | `13` | Graphique à bulles 3D. |
| Column | `14` | Diagramme à colonnes. |
| ColumnStacked | `15` | Diagramme à colonnes empilées. |
| ColumnPercentStacked | `16` | 100 % d'histogrammes empilés. |
| Column3D | `17` | Histogramme 3D. |
| Column3DStacked | `18` | Diagramme à colonnes empilées 3D. |
| Column3DPercentStacked | `19` | 3D 100 % histogramme empilé. |
| Column3DClustered | `20` | Diagramme à colonnes groupées 3D. |
| Doughnut | `21` | Graphique en anneau. |
| Line | `22` | Graphique linéaire. |
| LineStacked | `23` | Graphique en courbes empilées. |
| LinePercentStacked | `24` | Graphique en courbes empilées 100 %. |
| Line3D | `25` | Graphique en courbes 3D. |
| Pie | `26` | Graphique circulaire. |
| Pie3D | `27` | Graphique circulaire 3D. |
| PieOfBar | `28` | Pie of Bar chart. |
| PieOfPie | `29` | Pie of Pie chart. |
| Radar | `30` | Carte radar. |
| Scatter | `31` | Nuage de points. |
| Stock | `32` | Graphique boursier. |
| Surface | `33` | Graphique en surface. |
| Surface3D | `34` | Graphique de surface 3D. |

### Exemples

Montre comment créer un type de série de graphiques approprié pour un type de graphique.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Il existe plusieurs façons de remplir la collection de séries d'un graphique.
    // Différents schémas de série sont destinés à différents types de graphiques.
    // 1 - Diagramme à colonnes avec colonnes regroupées et regroupées le long de l'axe X par catégorie :
    Chart chart = AppendChart(builder, ChartType.Column, 500, 300);

    string[] categories = { "Category 1", "Category 2", "Category 3" };

    // Insère deux séries de valeurs décimales contenant une valeur pour chaque catégorie respective.
    // Ce graphique à colonnes aura trois groupes, chacun avec deux colonnes.
    chart.Series.Add("Series 1", categories, new [] { 76.6, 82.1, 91.6 });
    chart.Series.Add("Series 2", categories, new [] { 64.2, 79.5, 94.0 });

    // Les catégories sont distribuées le long de l'axe X et les valeurs sont distribuées le long de l'axe Y.
    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 2 - Graphique en aires avec des dates réparties sur l'axe des abscisses :
    chart = AppendChart(builder, ChartType.Area, 500, 300);

    DateTime[] dates = { new DateTime(2014, 3, 31),
        new DateTime(2017, 1, 23),
        new DateTime(2017, 6, 18),
        new DateTime(2019, 11, 22),
        new DateTime(2020, 9, 7)
    };

    // Insère une série avec une valeur décimale pour chaque date respective.
    // Les dates seront distribuées le long d'un axe X linéaire,
    // et les valeurs ajoutées à cette série créeront des points de données.
    chart.Series.Add("Series 1", dates, new [] { 15.8, 21.5, 22.9, 28.7, 33.1 });

    Assert.AreEqual(ChartAxisType.Category, chart.AxisX.Type);
    Assert.AreEqual(ChartAxisType.Value, chart.AxisY.Type);

    // 3 - Nuage de points 2D :
    chart = AppendChart(builder, ChartType.Scatter, 500, 300);

    // Chaque série aura besoin de deux tableaux décimaux de longueur égale.
    // Le premier tableau contient les valeurs X et le second contient les valeurs Y correspondantes
    // de points de données sur le graphique du graphique.
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
        new [] { 1.1, 5.0, 9.8 }, 
        new [] { 1.2, 4.9, 9.9 }, 
        new [] { 2.0, 4.0, 8.0 });

    doc.Save(ArtifactsDir + "Charts.ChartSeriesCollection.docx");
}

/// <summary>
/// Insérez un graphique à l'aide d'un générateur de document d'un ChartType, d'une largeur et d'une hauteur spécifiés, et supprimez ses données de démonstration.
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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
