---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.Charts.LegendPosition pour personnaliser facilement la position de la légende de votre graphique pour une visualisation améliorée des données.
type: docs
weight: 1230
url: /fr/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Spécifie les positions possibles pour une légende de graphique.

```csharp
public enum LegendPosition
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucune légende ne sera affichée pour le graphique. |
| Bottom | `1` | Spécifie que la légende doit être dessinée au bas du graphique. |
| Left | `2` | Spécifie que la légende doit être dessinée à gauche du graphique. |
| Right | `3` | Spécifie que la légende doit être dessinée à droite du graphique. |
| Top | `4` | Spécifie que la légende doit être dessinée en haut du graphique. |
| TopRight | `5` | Spécifie que la légende doit être dessinée en haut à droite du graphique. |

## Exemples

Montre comment modifier l'apparence de la légende d'un graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Déplacez la légende du graphique vers le coin supérieur droit.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Donnez plus d'espace aux autres éléments du graphique, tels que le graphique, en leur permettant de chevaucher la légende.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)
