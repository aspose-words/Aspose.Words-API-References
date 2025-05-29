---
title: IChartDataPoint.Explosion
linktitle: Explosion
articleTitle: Explosion
second_title: .NET için Aspose.Words
description: Pasta grafikleri için IChartDataPoint Explosion özelliğini keşfedin. Veri noktası konumlandırmasını hassasiyetle kontrol edin—görsel veri hikayenizi bugün geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif özelliğin ayarlanmadığı ve herhangi bir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca pasta grafikleri için geçerlidir.

```csharp
public int Explosion { get; set; }
```

## Örnekler

Bir pasta grafiğinin dilimlerinin merkezden nasıl uzaklaştırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Bir pasta grafiğinin "dilimleri", ilgili veri noktasının Patlama niteliği aracılığıyla merkezden belirli bir mesafe kadar uzaklaştırılabilir.
// Pasta grafiğinin ilk kısmına bir veri noktası ekleyin ve onu merkezden 10 puan uzaklaştırın.
// Aspose.Words, veri noktaları yoksa bunları otomatik olarak oluşturur.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// İkinci kısmı daha büyük bir mesafeye kaydır.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Ayrıca bakınız

* interface [IChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
