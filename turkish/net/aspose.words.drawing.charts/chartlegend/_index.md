---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: .NET için Aspose.Words
description: Daha iyi veri görselleştirmesi için grafiklerinizi özelleştirilebilir gösterge özellikleriyle geliştirmek üzere Aspose.Words.Drawing.Charts.ChartLegend sınıfını keşfedin.
type: docs
weight: 1010
url: /tr/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Grafik efsanesi özelliklerini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Grafiklerle Çalışma](https://docs.aspose.com/words/net/working-with-charts/) belgeleme makalesi.

```csharp
public class ChartLegend
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegend/font/) { get; } | Efsane girişlerinin varsayılan yazı tipi biçimlendirmesine erişim sağlar. Belirli bir efsane girişi için yazı tipi biçimlendirmesini geçersiz kılmak için, kullanın[`Font`](../chartlegendentry/font/) mülk. |
| [Format](../../aspose.words.drawing.charts/chartlegend/format/) { get; } | Efsanenin dolgu ve satır biçimlendirmesine erişim sağlar. |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Ana grafiğin tüm serileri ve eğilim çizgileri için bir dizi gösterge girişi döndürür. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Diğer grafik öğelerinin efsaneyle örtüşmesine izin verilip verilmeyeceğini belirler. Varsayılan değer`YANLIŞ` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Bir grafikteki efsanenin konumunu belirtir. |

## Örnekler

Bir grafiğin açıklamasının görünümünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Grafiğin açıklamasını sağ üst köşeye taşı.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Grafik gibi diğer grafik öğelerine, açıklamanın üzerine binmelerine izin vererek daha fazla yer verin.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
