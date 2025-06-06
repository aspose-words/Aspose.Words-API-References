---
title: ChartDataLabelCollection.ShowLeaderLines
linktitle: ShowLeaderLines
articleTitle: ShowLeaderLines
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ShowLeaderLines de ChartDataLabelCollection pour améliorer vos visualisations de données. Contrôlez facilement les lignes de repère pour une vision plus claire !
type: docs
weight: 130
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/showleaderlines/
---
## ChartDataLabelCollection.ShowLeaderLines property

Permet de spécifier si les lignes de repère des étiquettes de données doivent être affichées pour les étiquettes de données de la série entière. La valeur par défaut est`FAUX` .

```csharp
public bool ShowLeaderLines { get; set; }
```

## Remarques

S'applique uniquement aux graphiques à secteurs. Les lignes de repère créent une connexion visuelle entre une étiquette de données et son point de données correspondant.

La valeur définie pour cette propriété peut être remplacée pour une étiquette de données individuelle à l'aide de the [`ShowLeaderLines`](../../chartdatalabel/showleaderlines/) propriété.

## Exemples

Montre comment travailler avec les étiquettes de données d'un graphique à secteurs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Chart chart = builder.InsertChart(ChartType.Pie, 500, 300).Chart;

// Effacez la série de données de démonstration du graphique pour démarrer avec un graphique propre.
chart.Series.Clear();

// Insérer une série de graphiques personnalisés avec un nom de catégorie pour chacun des secteurs et leur tableau de fréquences.
ChartSeries series = chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel" },
    new[] { 2.7, 3.2, 0.8 });

// Activez les étiquettes de données qui afficheront à la fois le pourcentage et la fréquence de chaque secteur, et modifiez leur apparence.
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
