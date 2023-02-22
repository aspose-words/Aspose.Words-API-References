---
title: IChartDataPoint.Bubble3D
second_title: Référence de l'API Aspose.Words pour .NET
description: IChartDataPoint propriété. Spécifie si les bulles du graphique à bulles doivent avoir un effet 3D qui leur est appliqué.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Spécifie si les bulles du graphique à bulles doivent avoir un effet 3D qui leur est appliqué.

```csharp
public bool Bubble3D { get; set; }
```

### Exemples

Montre comment utiliser des effets 3D avec des graphiques à bulles.

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
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Voir également

* interface [IChartDataPoint](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* Assemblée [Aspose.Words](../../../)


