---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words pour .NET
description: Explorez la propriété Chart SeriesGroups pour accéder facilement à une riche collection de groupes de séries, améliorant ainsi votre expérience de visualisation des données.
type: docs
weight: 90
url: /fr/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

Donne accès à une collection de groupes de séries de ce graphique.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
