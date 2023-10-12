---
title: Chart.Legend
second_title: Référence de l'API Aspose.Words pour .NET
description: Chart propriété. Permet daccéder aux propriétés de la légende du graphique.
type: docs
weight: 50
url: /fr/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Permet d'accéder aux propriétés de la légende du graphique.

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chart/)
* Assemblée [Aspose.Words](../../../)


