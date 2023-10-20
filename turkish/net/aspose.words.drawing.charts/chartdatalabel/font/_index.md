---
title: ChartDataLabel.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words for .NET
description: ChartDataLabel Font mülk. Bu veri etiketinin yazı tipi formatına erişim sağlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/font/
---
## ChartDataLabel.Font property

Bu veri etiketinin yazı tipi formatına erişim sağlar.

```csharp
public Font Font { get; }
```

## Örnekler

Kabarcık grafikleriyle 3B efektlerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Çapını gösteren her baloncuğa bir veri etiketi uygulayın.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Ayrıca bakınız

* class [Font](../../../aspose.words/font/)
* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
