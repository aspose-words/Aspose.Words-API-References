---
title: ChartDataLabelCollection.ShowCategoryName
linktitle: ShowCategoryName
articleTitle: ShowCategoryName
second_title: Aspose.Words pour .NET
description: ChartDataLabelCollection ShowCategoryName propriété. Permet de spécifier si le nom de la catégorie doit être affiché pour les étiquettes de données de toute la série. La valeur par défaut estFAUX  en C#.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/showcategoryname/
---
## ChartDataLabelCollection.ShowCategoryName property

Permet de spécifier si le nom de la catégorie doit être affiché pour les étiquettes de données de toute la série. La valeur par défaut est`FAUX` .

```csharp
public bool ShowCategoryName { get; set; }
```

## Remarques

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant the [`ShowCategoryName`](../../chartdatalabel/showcategoryname/) propriété.

## Exemples

Montre comment utiliser les étiquettes de données d’un graphique à bulles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Bubble, 500, 300).Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Ajoutez une série personnalisée avec les coordonnées X/Y et le diamètre de chacune des bulles.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { 2.9, 3.5, 1.1, 4.0, 4.0 },
    new[] { 1.9, 8.5, 2.1, 6.0, 1.5 },
    new[] { 9.0, 4.5, 2.5, 8.0, 5.0 });

// Active les étiquettes de données, puis modifie leur apparence.
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
