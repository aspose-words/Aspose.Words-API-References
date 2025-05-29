---
title: IChartDataPoint.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: .NET için Aspose.Words
description: Daha ilgi çekici veri görselleştirmesi için Bubble grafiklerinizi çarpıcı 3B efektlerle geliştirmek üzere IChartDataPoint Bubble3D özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Kabarcık grafiğindeki kabarcıklara 3 boyutlu efekt uygulanıp uygulanmayacağını belirtir.

```csharp
public bool Bubble3D { get; set; }
```

## Örnekler

3D efektlerin balon grafikleriyle nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Her baloncuğa çapını gösteren bir veri etiketi uygulayın.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
    chart.Series[0].DataLabels[i].Font.Size = 12;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Ayrıca bakınız

* interface [IChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
