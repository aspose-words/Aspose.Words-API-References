---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: Aspose.Words pour .NET
description: Découvrez la propriété « Légende des graphiques » pour personnaliser vos graphiques en toute simplicité. Améliorez la visualisation de vos données grâce à des options de légende personnalisées pour une meilleure compréhension !
type: docs
weight: 70
url: /fr/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Donne accès aux propriétés de la légende du graphique.

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
