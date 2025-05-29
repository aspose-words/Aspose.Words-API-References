---
title: Chart.Legend
linktitle: Legend
articleTitle: Legend
second_title: .NET için Aspose.Words
description: Grafiklerinizi zahmetsizce özelleştirmek için Grafik Efsanesi özelliğini keşfedin. Daha iyi içgörüler için özelleştirilmiş efsane seçenekleriyle veri görselleştirmeyi geliştirin!
type: docs
weight: 70
url: /tr/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Grafik efsanesi özelliklerine erişim sağlar.

```csharp
public ChartLegend Legend { get; }
```

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
