---
title: Chart.Axes
second_title: Référence de l'API Aspose.Words pour .NET
description: Chart propriété. Obtient une collection de tous les axes de ce graphique.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chart/axes/
---
## Chart.Axes property

Obtient une collection de tous les axes de ce graphique.

```csharp
public ChartAxisCollection Axes { get; }
```

### Exemples

Montre comment travailler avec la collection d'axes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;            

// Masquer les lignes principales du quadrillage sur les axes Y primaire et secondaire.
foreach (ChartAxis axis in chart.Axes)
{
    if (axis.Type == ChartAxisType.Value)
        axis.HasMajorGridlines = false;
}

doc.Save(ArtifactsDir + "Charts.AxisCollection.docx");
```

### Voir également

* class [ChartAxisCollection](../../chartaxiscollection/)
* class [Chart](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../chart/)
* Assemblée [Aspose.Words](../../../)


