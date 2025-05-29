---
title: ChartLegend.Overlay
linktitle: Overlay
articleTitle: Overlay
second_title: .NET için Aspose.Words
description: Kontrol grafik öğesi, ChartLegend Overlay özelliğiyle örtüşüyor. Daha net içgörüler için özelleştirilebilir efsane ayarlarıyla veri görselleştirmenizi geliştirin.
type: docs
weight: 40
url: /tr/net/aspose.words.drawing.charts/chartlegend/overlay/
---
## ChartLegend.Overlay property

Diğer grafik öğelerinin efsaneyle örtüşmesine izin verilip verilmeyeceğini belirler. Varsayılan değer`YANLIŞ` .

```csharp
public bool Overlay { get; set; }
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

* class [ChartLegend](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
