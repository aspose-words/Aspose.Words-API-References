---
title: ChartLegend.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: ChartLegend Position mülk. Göstergenin grafikteki konumunu belirtir. Varsayılan değerRight  C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing.charts/chartlegend/position/
---
## ChartLegend.Position property

Göstergenin grafikteki konumunu belirtir. Varsayılan değer:Right .

```csharp
public LegendPosition Position { get; set; }
```

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

* enum [LegendPosition](../../legendposition/)
* class [ChartLegend](../)
* ad alanı [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* toplantı [Aspose.Words](../../../)
