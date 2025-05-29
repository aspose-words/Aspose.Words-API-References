---
title: ChartDataLabel.ShowBubbleSize
linktitle: ShowBubbleSize
articleTitle: ShowBubbleSize
second_title: .NET için Aspose.Words
description: ShowBubbleSize özelliğinin veri etiketi boyutlarını görüntüleyerek Bubble grafiklerinizi nasıl geliştirdiğini keşfedin. Görsel veri temsilinizi bugün optimize edin!
type: docs
weight: 130
url: /tr/net/aspose.words.drawing.charts/chartdatalabel/showbubblesize/
---
## ChartDataLabel.ShowBubbleSize property

Bir grafikteki veri etiketleri için kabarcık boyutunun görüntülenip görüntülenmeyeceğini belirtmeye olanak tanır. Yalnızca Kabarcık grafikleri için geçerlidir. Varsayılan değer`YANLIŞ` .

```csharp
public bool ShowBubbleSize { get; set; }
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

* class [ChartDataLabel](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
