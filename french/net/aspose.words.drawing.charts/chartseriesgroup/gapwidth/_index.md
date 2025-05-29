---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeriesGroup GapWidth pour ajuster facilement le pourcentage d'écart entre les éléments du graphique pour une visualisation améliorée des données.
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

Obtient ou définit le pourcentage de largeur d'espace entre les éléments du graphique.

```csharp
public int GapWidth { get; set; }
```

## Remarques

S'applique uniquement aux groupes de séries de types barre, colonne, secteur de barre, secteur de secteur, histogramme, boîte et moustache, cascade et entonnoir.

La plage de valeurs acceptables s'étend de 0 à 500 inclus. Pour les groupes de séries à barres/colonnes, la propriété représente l'espace entre les groupes de barres en pourcentage de leur largeur. Pour les graphiques à secteurs et à barres , il s'agit de l'espace entre les sections principale et secondaire du graphique.

## Exemples

Montrez comment configurer la largeur de l'espace et le chevauchement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Définir la largeur de l'espacement des colonnes et le chevauchement.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### Voir également

* class [ChartSeriesGroup](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
