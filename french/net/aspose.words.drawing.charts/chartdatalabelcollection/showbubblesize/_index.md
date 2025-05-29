---
title: ChartDataLabelCollection.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ShowBubbleSize de ChartDataLabelCollection améliore vos graphiques à bulles en contrôlant la visibilité des étiquettes de données. Optimisez la présentation de vos données !
type: docs
weight: 100
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/showbubblesize/
---
## ChartDataLabelCollection.ShowBubbleSize property

Permet de spécifier si la taille des bulles doit être affichée pour les étiquettes de données de la série entière. S'applique uniquement aux graphiques à bulles. La valeur par défaut est`FAUX` .

```csharp
public bool ShowBubbleSize { get; set; }
```

## Remarques

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant le [`ShowBubbleSize`](../../chartdatalabel/showbubblesize/) propriété.

## Exemples

Montre comment travailler avec les étiquettes de données d'un graphique à bulles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Effacez la série de données de démonstration du graphique pour démarrer avec un graphique propre.
chart.Series.Clear();

 // Ajoutez une série personnalisée avec les coordonnées X/Y et le diamètre de chacune des bulles.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Activez les étiquettes de données, puis modifiez leur apparence.
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
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
