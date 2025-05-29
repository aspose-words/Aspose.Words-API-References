---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ChartSeries LegendEntry pour accéder et personnaliser facilement les entrées de légende de vos graphiques, améliorant ainsi la visualisation de vos données.
type: docs
weight: 90
url: /fr/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

Obtient une entrée de légende pour cette série de graphiques.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## Exemples

Montre comment travailler avec une police de légende.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// Définir la taille de police par défaut pour toutes les entrées de légende.
chartLegend.Font.Size = 14;
// Modifier la police pour une entrée de légende spécifique.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// Obtenir l'entrée de légende pour la série de graphiques.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### Voir également

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
