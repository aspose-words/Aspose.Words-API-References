---
title: IChartDataPoint.Bubble3D
second_title: Aspose.Words for .NET API Referansı
description: IChartDataPoint mülk. Kabarcık grafiğindeki baloncuklara 3 boyutlu efektin uygulanması gerekip gerekmediğini belirtir.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.charts/ichartdatapoint/bubble3d/
---
## IChartDataPoint.Bubble3D property

Kabarcık grafiğindeki baloncuklara 3 boyutlu efektin uygulanması gerekip gerekmediğini belirtir.

```csharp
public bool Bubble3D { get; set; }
```

### Örnekler

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

* interface [IChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* toplantı [Aspose.Words](../../../)


