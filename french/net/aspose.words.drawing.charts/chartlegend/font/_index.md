---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: Personnalisez facilement les polices de votre ChartLegend ! Accédez à la mise en forme par défaut et remplacez facilement des entrées de légende spécifiques pour un rendu soigné.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

Donne accès au formatage de police par défaut des entrées de légende. Pour remplacer le formatage de police d'une entrée de légende spécifique, utilisez l'option[`Font`](../../chartlegendentry/font/) propriété.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
