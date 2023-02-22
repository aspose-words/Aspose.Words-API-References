---
title: ChartDataLabel.ShowBubbleSize
second_title: Aspose.Words for .NET API Referansı
description: ChartDataLabel mülk. Bir grafikteki veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Yalnızca Kabarcık çizelgeleri için geçerlidir. Varsayılan değer yanlıştır.
type: docs
weight: 60
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Bir grafikteki veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirlemeye izin verir. Yalnızca Kabarcık çizelgeleri için geçerlidir. Varsayılan değer yanlıştır.

```csharp
public bool ShowBubbleSize { get; set; }
```

### Örnekler

Kabarcık grafiklerle 3B efektlerin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Bubble3D, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Y-Values", chart.Series[0].Name);
Assert.True(chart.Series[0].Bubble3D);

// Çapını gösteren her balona bir veri etiketi uygulayın.
for (int i = 0; i < 3; i++)
{
    chart.Series[0].HasDataLabels = true;
    chart.Series[0].DataLabels[i].ShowBubbleSize = true;
}

doc.Save(ArtifactsDir + "Charts.Bubble3D.docx");
```

### Ayrıca bakınız

* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chartdatalabel/)
* toplantı [Aspose.Words](../../../)


