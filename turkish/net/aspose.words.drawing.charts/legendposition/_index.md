---
title: LegendPosition Enum
linktitle: LegendPosition
articleTitle: LegendPosition
second_title: .NET için Aspose.Words
description: Gelişmiş veri görselleştirmesi için grafik efsanenizin konumunu kolayca özelleştirmek üzere Aspose.Words.Drawing.Charts.LegendPosition enum'unu keşfedin.
type: docs
weight: 1230
url: /tr/net/aspose.words.drawing.charts/legendposition/
---
## LegendPosition enumeration

Bir grafik efsanesi için olası konumları belirtir.

```csharp
public enum LegendPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Grafik için herhangi bir açıklama gösterilmeyecek. |
| Bottom | `1` | Efsanenin grafiğin en altına çizileceğini belirtir. |
| Left | `2` | Efsanenin grafiğin soluna çizileceğini belirtir. |
| Right | `3` | Efsanenin grafiğin sağ tarafına çizileceğini belirtir. |
| Top | `4` | Efsanenin grafiğin en üstüne çizileceğini belirtir. |
| TopRight | `5` | Efsanenin grafiğin sağ üst köşesine çizileceğini belirtir. |

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
