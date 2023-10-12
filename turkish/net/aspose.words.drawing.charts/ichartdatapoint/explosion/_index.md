---
title: IChartDataPoint.Explosion
second_title: Aspose.Words for .NET API Referansı
description: IChartDataPoint mülk. Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir negatif özelliğin ayarlanmadığı ve hiçbir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca Pasta grafikleri için geçerlidir.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.charts/ichartdatapoint/explosion/
---
## IChartDataPoint.Explosion property

Veri noktasının pastanın merkezinden ne kadar uzağa taşınacağını belirtir. Negatif olabilir, negatif, özelliğin ayarlanmadığı ve hiçbir patlamanın uygulanmaması gerektiği anlamına gelir. Yalnızca Pasta grafikleri için geçerlidir.

```csharp
public int Explosion { get; set; }
```

### Örnekler

Pasta grafiğinin dilimlerinin merkezden nasıl uzağa taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Pie, 500, 350);
Chart chart = shape.Chart;

Assert.AreEqual(1, chart.Series.Count);
Assert.AreEqual("Sales", chart.Series[0].Name);

// Bir pasta grafiğinin "Dilimleri", ilgili veri noktasının Patlama özelliği aracılığıyla merkezden bir mesafe kadar uzaklaştırılabilir.
// Pasta grafiğinin ilk kısmına bir veri noktası ekleyin ve onu merkezden 10 puan uzaklaştırın.
// Aspose.Words, eğer mevcut değilse, veri noktalarını otomatik olarak oluşturur.
ChartDataPoint dataPoint = chart.Series[0].DataPoints[0];
dataPoint.Explosion = 10;

// İkinci kısmı daha büyük bir mesafeye kaydır.
dataPoint = chart.Series[0].DataPoints[1];
dataPoint.Explosion = 40;

doc.Save(ArtifactsDir + "Charts.PieChartExplosion.docx");
```

### Ayrıca bakınız

* interface [IChartDataPoint](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../ichartdatapoint/)
* toplantı [Aspose.Words](../../../)


