---
title: ChartDataLabelCollection.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Position de ChartDataLabelCollection pour personnaliser facilement les positions de vos étiquettes de données pour une visualisation et une clarté améliorées des données.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chartdatalabelcollection/position/
---
## ChartDataLabelCollection.Position property

Obtient ou définit la position des étiquettes de données.

```csharp
public ChartDataLabelPosition Position { get; set; }
```

## Remarques

La position peut être définie pour les étiquettes de données des types de séries de graphiques suivants :

-Bar ,Column , Histogram ,Pareto , Waterfall ; valeurs autorisées :Center , InsideBase ,InsideEnd et OutsideEnd;

-BarStacked ,BarPercentStacked , ColumnStacked ,ColumnPercentStacked ; valeurs allowed :Center ,InsideBase etInsideEnd;

-Bubble ,Bubble3D , Line ,LineStacked , LinePercentStacked ,Scatter , Stock ; valeurs autorisées :Center , Left ,Right , Above etBelow;

-Pie ,Pie3D , PieOfBar ,PieOfPie ; valeurs autorisées : Center ,InsideEnd , OutsideEnd etBestFit;

-BoxAndWhisker ; valeurs autorisées : Left ,Right , Above etBelow.

## Exemples

Montre comment définir la position de l'étiquette de données.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique à colonnes.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// Supprimer la série générée par défaut.
seriesColl.Clear();

// Ajouter une série.
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// Afficher les étiquettes de données et définir la couleur de la police.
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// Définir la position de l'étiquette de données.
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### Voir également

* enum [ChartDataLabelPosition](../../chartdatalabelposition/)
* class [ChartDataLabelCollection](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
