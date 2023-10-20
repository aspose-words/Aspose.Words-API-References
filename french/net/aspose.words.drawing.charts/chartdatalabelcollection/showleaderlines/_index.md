---
title: ChartDataLabelCollection.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: Aspose.Words pour .NET
description: ChartDataLabelCollection ShowLeaderLines propriété. Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. La valeur par défaut estFAUX  en C#.
type: docs
weight: 100
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. La valeur par défaut est`FAUX` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## Remarques

S'applique uniquement aux diagrammes circulaires. Les lignes de repère créent une connexion visuelle entre une étiquette de données et son point de données correspondant.

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle en utilisant the [`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) propriété.

## Exemples

Montre comment utiliser les étiquettes de données d’un graphique à secteurs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Efface la série de données de démonstration du graphique pour commencer avec un graphique propre.
chart.Series.Clear();

// Insère une série de graphiques personnalisés avec un nom de catégorie pour chacun des secteurs et leur tableau de fréquence.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Active les étiquettes de données qui afficheront à la fois le pourcentage et la fréquence de chaque secteur, et modifieront leur apparence.
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
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
