---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: .NET için Aspose.Words
description: Grafiklerinizdeki kabarcık boyutlarını özelleştirmek, veri görselleştirmesini ve kullanıcı etkileşimini geliştirmek için ChartSeriesGroup BubbleScale özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak alır veya ayarlar.

```csharp
public int BubbleScale { get; set; }
```

## Notlar

Yalnızca seri gruplarına uygulanırBubble ve Bubble3D türleri.

Kabul edilebilir değerler aralığı 0 ile 300 arasındadır. Varsayılan değer 100'dür.

## Örnekler

Baloncukların boyutunun nasıl ayarlanacağını göster.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 3D balon grafiği ekle.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// Kabarcık ölçeğini %200'e ayarlayın.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### Ayrıca bakınız

* class [ChartSeriesGroup](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
