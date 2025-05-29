---
title: ChartSeries.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: Aspose.Words pour .NET
description: Améliorez votre graphique à bulles avec ChartSeries Bubble3D ! Ajoutez de superbes effets 3D à vos bulles pour un impact visuel saisissant.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartseries/bubble3d/
---
## ChartSeries.Bubble3D property

Spécifie si les bulles du graphique à bulles doivent avoir un effet 3D appliqué.

```csharp
public bool Bubble3D { get; set; }
```

## Exemples

Montre comment utiliser les effets 3D avec les graphiques à bulles.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Appliquez une étiquette de données à chaque bulle qui affiche son diamètre.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Voir également

* class [ChartSeries](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
