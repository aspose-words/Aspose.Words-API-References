---
title: ChartLegend Class
linktitle: ChartLegend
articleTitle: ChartLegend
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.Charts.ChartLegend sınıf. Grafik açıklama özelliklerini temsil eder C#'da.
type: docs
weight: 720
url: /tr/net/aspose.words.drawing.charts/chartlegend/
---
## ChartLegend class

Grafik açıklama özelliklerini temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Grafiklerle Çalışmak](https://docs.aspose.com/words/net/working-with-charts/) dokümantasyon makalesi.

```csharp
public class ChartLegend
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [LegendEntries](../../aspose.words.drawing.charts/chartlegend/legendentries/) { get; } | Ana grafiğin tüm serileri ve trend çizgileri için gösterge girişlerinin bir koleksiyonunu döndürür. |
| [Overlay](../../aspose.words.drawing.charts/chartlegend/overlay/) { get; set; } | Diğer grafik öğelerinin göstergelerle çakışmasına izin verilip verilmeyeceğini belirler. Varsayılan değer:`YANLIŞ` . |
| [Position](../../aspose.words.drawing.charts/chartlegend/position/) { get; set; } | Göstergenin grafikteki konumunu belirtir. Varsayılan değer:Right . |

## Örnekler

Bir grafiğin göstergesinin görünümünün nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 300);
Chart chart = shape.Chart;

Assert.AreEqual(3, chart.Series.Count);
Assert.AreEqual("Series 1", chart.Series[0].Name);
Assert.AreEqual("Series 2", chart.Series[1].Name);
Assert.AreEqual("Series 3", chart.Series[2].Name);

// Grafiğin açıklamasını sağ üst köşeye taşıyın.
ChartLegend legend = chart.Legend;
legend.Position = LegendPosition.TopRight;

// Grafik gibi diğer grafik öğelerinin göstergeyle örtüşmesine izin vererek daha fazla alan verin.
legend.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartLegend.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../)
