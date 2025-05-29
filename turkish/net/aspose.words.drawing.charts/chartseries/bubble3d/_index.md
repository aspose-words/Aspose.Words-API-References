---
title: ChartSeries.Bubble3D
linktitle: Bubble3D
articleTitle: Bubble3D
second_title: .NET için Aspose.Words
description: ChartSeries Bubble3D ile Bubble grafiğinizi geliştirin! Göz alıcı bir görsel etki için baloncuklarınıza çarpıcı 3D efektler ekleyin.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/chartseries/bubble3d/
---
## ChartSeries.Bubble3D property

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

* class [ChartSeries](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
