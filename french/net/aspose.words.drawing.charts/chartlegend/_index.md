---
title: Class ChartLegend
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Drawing.Charts.ChartLegend classe. Représente les propriétés de la légende du graphique.
type: docs
weight: 720
url: /fr/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Représente les propriétés de la légende du graphique.

Pour en savoir plus, visitez le[Travailler avec des graphiques](https://docs.aspose.com/words/net/working-with-charts/) article documentaire.

```csharp
public class ChartLegend
```

## Propriétés

| Nom | La description |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Renvoie une collection d'entrées de légende pour toutes les séries et courbes de tendance du graphique parent. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Détermine si d'autres éléments du graphique doivent pouvoir chevaucher la légende. La valeur par défaut est`FAUX` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Spécifie la position de la légende sur un graphique. La valeur par défaut estRight . |

### Exemples

Montre comment modifier l’apparence de la légende d’un graphique.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Déplace la légende du graphique vers le coin supérieur droit.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Donnez plus d'espace aux autres éléments du graphique, tels que le graphique, en leur permettant de chevaucher la légende.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../)


