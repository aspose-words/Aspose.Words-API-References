---
title: ChartAxisType Enum
linktitle: ChartAxisType
articleTitle: ChartAxisType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.Charts.ChartAxisType pour définir facilement les types d'axes de graphique et améliorer la visualisation des données de votre document.
type: docs
weight: 920
url: /fr/net/aspose.words.drawing.charts/chartaxistype/
---
## ChartAxisType enumeration

Spécifie le type d'axe du graphique.

```csharp
public enum ChartAxisType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Category | `0` | Axe des catégories d'un graphique. |
| Series | `1` | Axe des séries d'un graphique. |
| Value | `2` | Axe des valeurs d'un graphique. |

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
