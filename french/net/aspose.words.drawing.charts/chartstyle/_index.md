---
title: ChartStyle Enum
linktitle: ChartStyle
articleTitle: ChartStyle
second_title: Aspose.Words pour .NET
description: Appliquez des styles de graphiques prédéfinis dans Aspose.Words. Améliorez vos visuels avec l'énumération ChartStyle pour une mise en forme professionnelle de vos documents.
type: docs
weight: 1130
url: /fr/net/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enumeration

Spécifie les styles prédéfinis d'un graphique.

```csharp
public enum ChartStyle
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Normal | `0` | Représente le style de graphique par défaut. |
| Muted | `1` | Un style aux couleurs douces. |
| Saturated | `2` | Un style avec des couleurs plus saturées. |
| Shaded | `3` | Un style avec des points de données ombrés. |
| Flat | `4` | Un style avec des points de données plats sans dégradé. |
| Shadowed | `5` | Un style avec des points de données ayant une ombre. |
| Gradient | `6` | Un style avec remplissage dégradé de points de données. |
| Original | `7` | Un style avec une apparence originale d'un graphique. |
| Transparent1 | `8` | Un style avec des points de données transparents. |
| Transparent2 | `9` | Un style avec des points de données transparents. |
| Outline | `10` | Un style avec des points de données n'ayant pas de remplissage, mais seulement un contour. |
| OutlineBlack | `11` | Un style avec un arrière-plan de graphique noir, dans lequel les points de données n'ont pas de remplissage, mais seulement un contour. |
| Black | `12` | Un style avec un arrière-plan de graphique noir. |
| Grey | `13` | Un style avec un arrière-plan de graphique dégradé gris. |
| Blue | `14` | Un style avec un arrière-plan de graphique bleu. |
| ShadedPlot | `15` | Un style dans lequel la zone de tracé est ombrée. |

## Exemples

Montre comment définir et obtenir le style du graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérer un graphique dans le style Noir.
builder.InsertChart(ChartType.Column, 400, 250, ChartStyle.Black);

doc.Save(ArtifactsDir + "Charts.SetChartStyle.docx");

doc = new Document(ArtifactsDir + "Charts.SetChartStyle.docx");

// Obtenir un graphique à mettre à jour.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Chart chart = shape.Chart;

// Obtenir le style du graphique.
Assert.AreEqual(ChartStyle.Black, chart.Style);
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
