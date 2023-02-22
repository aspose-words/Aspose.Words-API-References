---
title: ChartDataLabelCollection.ShowBubbleSize
second_title: Référence de l'API Aspose.Words pour .NET
description: ChartDataLabelCollection propriété. Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de toute la série. Sapplique uniquement aux graphiques à bulles. La valeur par défaut est faux .
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/
---
## ChartDataLabelCollection.ShowBubbleSize property

Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de toute la série. S'applique uniquement aux graphiques à bulles. La valeur par défaut est **faux** .

```csharp
public bool ShowBubbleSize { get; set; }
```

### Remarques

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle à l'aide de the [`ShowBubbleSize`](../../chartdatalabel/showbubblesize/) propriété.

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

### Voir également

* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chartdatalabelcollection/)
* Assemblée [Aspose.Words](../../../)


