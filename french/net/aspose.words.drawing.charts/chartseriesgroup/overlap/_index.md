---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeriesGroup Overlap pour ajuster facilement le pourcentage de chevauchement de vos barres ou colonnes de série pour une visualisation améliorée des données.
type: docs
weight: 80
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

Obtient ou définit le pourcentage de chevauchement des barres ou des colonnes de la série.

```csharp
public int Overlap { get; set; }
```

## Remarques

S'applique aux groupes de séries de tous les types de barres et de colonnes.

La plage de valeurs acceptables s'étend de -100 à 100 inclus. Une valeur de 0 indique qu'il n'y a pas d'espace entre les barres/colonnes. Si la valeur est de -100, la distance entre les barres/colonnes est égale à leur largeur. Une valeur de 100 signifie que les barres/colonnes se chevauchent complètement.

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
