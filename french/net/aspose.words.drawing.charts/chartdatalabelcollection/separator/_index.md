---
title: ChartDataLabelCollection.Separator
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartDataLabelCollection propriété. Obtient ou définit le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. La valeur par défaut est une virgule sauf pour les graphiques circulaires affichant uniquement le nom de la catégorie et le pourcentage lorsquun saut de ligne doit être utilisé à la place.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/separator/
---
## ChartDataLabelCollection.Separator property

Obtient ou définit le séparateur de chaîne utilisé pour les étiquettes de données de la série entière. La valeur par défaut est une virgule, sauf pour les graphiques circulaires affichant uniquement le nom de la catégorie et le pourcentage, lorsqu'un saut de ligne doit être utilisé à la place.

```csharp
public string Separator { get; set; }
```

### Remarques

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle à l'aide de the [`Separator`](../../chartdatalabel/separator/) propriété.

### Exemples

Montre comment utiliser les étiquettes de données d'un graphique à bulles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

 // Ajoute une série personnalisée avec les coordonnées X/Y et le diamètre de chacune des bulles.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Activer les étiquettes de données, puis modifier leur apparence.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowBubbleSize = true;
dataLabels.ShowCategoryName = true;
dataLabels.ShowSeriesName = true;
dataLabels.Separator = " & ";

doc.Save(ArtifactsDir + "Charts.DataLabelsBubbleChart.docx");
```

Montre comment utiliser les étiquettes de données d'un graphique à secteurs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Effacez la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Insère une série de graphiques personnalisés avec un nom de catégorie pour chacun des secteurs, et leur table de fréquence.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Activer les étiquettes de données qui afficheront à la fois le pourcentage et la fréquence de chaque secteur, et modifier leur apparence.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowLeaderLines = true;
dataLabels.ShowLegendKey = true;
dataLabels.ShowPercentage = true;
dataLabels.ShowValue = true;
dataLabels.Separator = "; ";

doc.Save(ArtifactsDir + "Charts.DataLabelsPieChart.docx");
```

### Voir également

* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* Assemblée [Aspose.Words](../../../)


