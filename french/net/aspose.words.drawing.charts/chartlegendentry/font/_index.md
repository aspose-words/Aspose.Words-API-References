---
title: ChartLegendEntry.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: Découvrez la propriété de police ChartLegendEntry pour un accès facile au formatage de police personnalisable, améliorant vos entrées de légende pour un meilleur attrait visuel.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

Donne accès à la mise en forme de la police de cette entrée de légende.

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
* class [ChartLegendEntry](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
