---
title: Chart.Legend
second_title: Aspose.Words for .NET API Referansı
description: Chart mülk. Grafik açıklama özelliklerine erişim sağlar.
type: docs
weight: 50
url: /tr/net/aspose.words.drawing.charts/chart/legend/
---
## Chart.Legend property

Grafik açıklama özelliklerine erişim sağlar.

```csharp
public ChartLegend Legend { get; }
```

### Örnekler

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

* class [ChartLegend](../../chartlegend/)
* class [Chart](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../chart/)
* toplantı [Aspose.Words](../../../)


