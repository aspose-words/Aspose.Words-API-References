---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeriesGroup BubbleScale pour personnaliser la taille des bulles dans vos graphiques, améliorant ainsi la visualisation des données et l'engagement des utilisateurs.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Obtient ou définit la taille des bulles en pourcentage de leur taille par défaut.

```csharp
public int BubbleScale { get; set; }
```

## Remarques

S'applique uniquement aux groupes de séries duBubble et Bubble3D types.

La plage de valeurs acceptables s'étend de 0 à 300 inclus. La valeur par défaut est 100.

## Exemples

Montrez comment définir la taille des bulles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique 3D à bulles.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Définir l'échelle des bulles à 200 %.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Voir également

* class [ChartSeriesGroup](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
