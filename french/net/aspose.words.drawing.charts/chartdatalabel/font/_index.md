---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Police ChartDataLabel pour personnaliser facilement la mise en forme de la police de votre étiquette de données pour un attrait visuel et une clarté améliorés.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Donne accès au formatage de police de cette étiquette de données.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* espace de noms [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* Assemblée [Aspose.Words](../../../)
