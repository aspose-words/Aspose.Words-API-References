---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.ChartLegendEntry pour créer des légendes de graphiques dynamiques. Améliorez la visualisation de vos données grâce à une intégration et une personnalisation fluides.
type: docs
weight: 1020
url: /fr/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

Représente une entrée de légende de graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article de documentation.

```csharp
public class ChartLegendEntry
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | Donne accès à la mise en forme de la police de cette entrée de légende. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | Obtient ou définit une valeur indiquant si cette entrée est masquée dans la légende du graphique. La valeur par défaut est**FAUX** . |

## Remarques

Une entrée de légende correspond à une série de graphiques ou à une ligne de tendance spécifique.

Le texte de l'entrée correspond au nom de la série ou de la courbe de tendance. Il n'est pas modifiable.

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

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
