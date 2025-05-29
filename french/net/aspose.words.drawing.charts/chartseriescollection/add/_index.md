---
title: ChartSeriesCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words pour .NET
description: Améliorez facilement vos graphiques grâce à la méthode d'ajout ChartSeriesCollection. Ajoutez facilement de nouvelles séries à vos graphiques à barres, à colonnes, à courbes et à surfaces pour des visuels dynamiques.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing.charts/chartseriescollection/add/
---
## Add(*string, string[], double[]*) {#add_5}

Ajoute un nouveau[`ChartSeries`](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques à barres, à colonnes, à courbes et à surface.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values)
```

### Return_Value

Ajouté récemment[`ChartSeries`](../../chartseries/) objet.

## Exemples

Montre comment créer un diagramme de Pareto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un diagramme de Pareto.
Shape shape = builder.InsertChart(ChartType.Pareto, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Best-Selling Car";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
chart.Series.Add(
    "Best-Selling Car",
    new string[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
    new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

doc.Save(ArtifactsDir + "Charts.Pareto.docx");
```

Montre comment créer un graphique en entonnoir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique en entonnoir.
Shape shape = builder.InsertChart(ChartType.Funnel, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Population by Age Group";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
ChartSeries series = chart.Series.Add(
    "Population by Age Group",
    new string[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
    new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
string decimalSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyDecimalSeparator;
series.DataLabels.NumberFormat.FormatCode = $"0{decimalSeparator}0%";

doc.Save(ArtifactsDir + "Charts.Funnel.docx");
```

Montre comment créer un graphique en boîte et à moustaches.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique en boîte et à moustaches.
Shape shape = builder.InsertChart(ChartType.BoxAndWhisker, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Points by Years";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
ChartSeries series = chart.Series.Add(
    "Points by Years",
    new string[]
    {
        "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC",
        "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR",
        "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA"
    },
    new double[]
    {
        91, 80, 100, 77, 90, 104, 105, 118, 120, 101,
        114, 107, 110, 60, 79, 78, 77, 102, 101, 113,
        94, 93, 84, 71, 80, 103, 80, 94, 100, 101
    });

// Afficher les étiquettes de données.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.BoxAndWhisker.docx");
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, double[], double[]*) {#add_2}

Ajoute un nouveau[`ChartSeries`](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques en nuage de points.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues)
```

### Return_Value

Ajouté récemment[`ChartSeries`](../../chartseries/) objet.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, DateTime[], double[]*) {#add_4}

Ajoute un nouveau[`ChartSeries`](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques de zone, radar et boursiers.

```csharp
public ChartSeries Add(string seriesName, DateTime[] dates, double[] values)
```

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, double[], double[], double[]*) {#add_3}

Ajoute un nouveau[`ChartSeries`](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries à tout type de graphiques à bulles.

```csharp
public ChartSeries Add(string seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```

### Return_Value

Ajouté récemment[`ChartSeries`](../../chartseries/) objet.

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

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, ChartMultilevelValue[], double[]*) {#add}

Ajoute un nouveau[`ChartSeries`](../../chartseries/)à cette collection. Utilisez cette méthode pour ajouter des séries qui ont des catégories de données à plusieurs niveaux.

```csharp
public ChartSeries Add(string seriesName, ChartMultilevelValue[] categories, double[] values)
```

### Return_Value

Ajouté récemment[`ChartSeries`](../../chartseries/) objet.

## Exemples

Montre comment créer un graphique en forme de soleil.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique Sunburst.
Shape shape = builder.InsertChart(ChartType.Sunburst, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Sales";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
ChartSeries series = chart.Series.Add(
    "Sales",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Sales - Europe", "UK", "London Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Liverpool Dep."),
        new ChartMultilevelValue("Sales - Europe", "UK", "Manchester Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Paris Dep."),
        new ChartMultilevelValue("Sales - Europe", "France", "Lyon Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Denver Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Seattle Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Detroit Dep."),
        new ChartMultilevelValue("Sales - NA", "USA", "Houston Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Toronto Dep."),
        new ChartMultilevelValue("Sales - NA", "Canada", "Montreal Dep."),
        new ChartMultilevelValue("Sales - Oceania", "Australia", "Sydney Dep."),
        new ChartMultilevelValue("Sales - Oceania", "New Zealand", "Auckland Dep.")
    },
    new double[] { 1236, 851, 536, 468, 179, 527, 799, 1148, 921, 457, 482, 761, 694 });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
series.DataLabels.ShowValue = false;
series.DataLabels.ShowCategoryName = true;

doc.Save(ArtifactsDir + "Charts.Sunburst.docx");
```

Montre comment créer un graphique arborescent.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique Treemap.
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// Afficher les étiquettes de données.
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### Voir également

* class [ChartSeries](../../chartseries/)
* class [ChartMultilevelValue](../../chartmultilevelvalue/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, double[]*) {#add_1}

Ajoute un nouveau[`ChartSeries`](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries aux graphiques à histogramme.

```csharp
public ChartSeries Add(string seriesName, double[] xValues)
```

### Return_Value

Ajouté récemment[`ChartSeries`](../../chartseries/) objet.

## Remarques

Pour les types de graphiques autres que l'histogramme, cette méthode ajoute une série avec des valeurs Y vides.

## Exemples

Montre comment créer un histogramme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique d'histogramme.
Shape shape = builder.InsertChart(ChartType.Histogram, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "Avg Temperature since 1991";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
chart.Series.Add(
    "Avg Temperature",
    new double[]
    {
        51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4,
        53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7,
        56.3, 55.9, 55.6
    });

doc.Save(ArtifactsDir + "Charts.Histogram.docx");
```

### Voir également

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)

---

## Add(*string, string[], double[], bool[]*) {#add_6}

Ajoute un nouveau[`ChartSeries`](../../chartseries/) à cette collection. Utilisez cette méthode pour ajouter des séries aux graphiques en cascade.

```csharp
public ChartSeries Add(string seriesName, string[] categories, double[] values, bool[] isSubtotal)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| seriesName | String | Un nom de série à ajouter. |
| categories | String[] | Noms de catégories pour l'axe X. |
| values | Double[] | Valeurs de l'axe Y. |
| isSubtotal | Boolean[] | Valeurs indiquant si la valeur Y correspondante est un sous-total. |

### Return_Value

Ajouté récemment[`ChartSeries`](../../chartseries/) objet.

## Remarques

Pour les types de graphiques autres que Waterfall,*isSubtotal* les valeurs sont ignorées.

## Exemples

Montre comment créer un graphique en cascade.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique en cascade.
Shape shape = builder.InsertChart(ChartType.Waterfall, 450, 450);
Chart chart = shape.Chart;
chart.Title.Text = "New Zealand GDP";

// Supprimer la série générée par défaut.
chart.Series.Clear();

// Ajouter une série.
ChartSeries series = chart.Series.Add(
    "New Zealand GDP",
    new string[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
    new double[] { 100, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
    new bool[] { true, false, false, true, false, false, true });

// Afficher les étiquettes de données.
series.HasDataLabels = true;

doc.Save(ArtifactsDir + "Charts.Waterfall.docx");
```

### Voir également

* class [ChartSeries](../../chartseries/)
* class [ChartSeriesCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
