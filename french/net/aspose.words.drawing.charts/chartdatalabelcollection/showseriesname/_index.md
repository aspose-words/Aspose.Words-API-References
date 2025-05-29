---
title: ChartDataLabelCollection.ShowSeriesName
linktitle: ShowSeriesName
articleTitle: ShowSeriesName
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShowSeriesName de ChartDataLabelCollection et contrôlez facilement la visibilité des noms de séries dans vos étiquettes de données. Améliorez vos graphiques dès aujourd'hui !
type: docs
weight: 160
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/showseriesname/
---
## ChartDataLabelCollection.ShowSeriesName property

Renvoie ou définit une valeur booléenne pour indiquer le comportement d'affichage du nom de la série pour les étiquettes de données de la série entière. `vrai` pour afficher le nom de la série ;`FAUX` pour masquer. Par défaut`FAUX` .

```csharp
public bool ShowSeriesName { get; set; }
```

## Remarques

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant le [`ShowSeriesName`](../../chartdatalabel/showseriesname/) propriété.

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
